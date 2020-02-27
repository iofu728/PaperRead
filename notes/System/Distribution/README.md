# Distribution

1. [**MapReduce: Simpliﬁed Data Processing on Large Clusters**](https://github.com/iofu728/PaperRead/blob/master/paper/System/Distribution/mapreduce.pdf) [OSDI 2004] _Jeffrey Dean and Sanjay Ghemawat_.
   - Map Reduce detail:
     1. Split input file to some blocks.
     2. Starts up 1 master, K workers which will pick M map tasks and R reduce tasks.
     3. Map worker will read contents from input split, parse key/values pairs out of input data, and pair to user-defined Map functions.
     4. Buffered the intermediate key/values pairs result in memory.
     5. Periodically load to disk, partitioned into R regions by partitioning function and pass back the location of buffered paired to master.
     6. Master will forwarding these location to reduce workers.
     7. When reduce worker is notified by master about the location, by using RPC to read the buffered data from local disk of map workers.
     8. After reading intermediate data, sort key (too large will store to disk).
     9. The ouput of Reduce function is appended to a final output file.
     10. After all worker completed, call user program.
   - fault tolerant
     - worker failure
     - master failure
     - semantics of presence of failure
   - Locality
     - to reduce network communication
   - Backup
     - to alleviate "straggler"
     - When MapReduce is close to completed, start a backup worker to the unfinished worker.
     - The task is marked as completed whenever the primary worker or the backup worker completed.
2. [**The Google File System**](https://github.com/iofu728/PaperRead/blob/master/paper/System/Distribution/gfs.pdf) [SOSP 2003] _Sanjay Ghemawat, Howard Gobioff, Shun-Tak Leung_
   - Distribution File System with huge, most appending, relaxed consistency.
   - A single master + N chunk servers(Three replica: primary and secondaries).
   - Control stream and data stream.
   - Master store chunk ID, NOT have the location of chuck which reduce the master pressure in the start or Internet error.
     - The chuck report the location using the _HeartBeat_.
   - Data flow are forwards by each machine to the "closest" machine in the network topology that has not received it.
   - Lease period and version to improve the fault tolerant.
   - Periods garbage collection.
   - Copy-on-write to reduce the copy in snapshot which use reference counts.
   - Record append at-least-once when secondaries failed.
   - Chunk check padding and duplicate records using a **predictable magic number** at the start of a valid record, or checksum.
   - Nearest replica using IP.
   - Lease mechanism make no two primary.
   - A single master is not good.
