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
3. [**The Design of a Practical The Design System of a for Practical System for Fault-Tolerant Virtual Machines Fault-Tolerant Virtual Machines**](https://github.com/iofu728/PaperRead/blob/master/paper/System/Distribution/vm-ft.pdf) [SIGOPS 2010] _Daniel J Scales, Michael Nelson, Ganesh Venkitachalam_
   - replicating Fault-tolerant
   - no-deterministic State-Machine
   - Primary - Backup
   - Fault-tolerant Protocol: logging channel
     - Primary send Backup first and then output
     - UDP heartbeat
     - maybe have double output
       - TCP discard and Disk idempotent
   - split-brain: both primary and backup crush
     - an atomic test-and-set
     - shared storage
   - bounce buffers
     - FT avoids this problem by not copying into **guest memory** while the primary or backup is executing.
     - FT first copies the network packet or disk block into a private **"bounce buffer"** that the primary cannot access.
     - When this first copy completes, the FT hypervisor interrupts the primary so that it is not executing.
     - FT records the **point at which it interrupted the primary** (as with any interrupt).
     - Then FT **copies the bounce buffer into the primary's memory**, and after that allows the primary to continue executing.
     - FT sends the data to the backup on the log channel.
     - The backup's FT interrupts the backup at the same instruction as the primary was interrupted, copies the data into the backup's memory while the backup is into executing, and then resumes the backup.
4. [**In Search of an Understandable Consensus Algorithm**](https://github.com//iofu728/PaperRead/blob/master/paper/System/Distribution/raft-extended.pdf) [USENIX ATC 2014] _Diego Ongaro, John K. Ousterhout_
   - Consensus algorithm for managing a replicated log.
   - Split Brain, Majority Voting, Understandability.
     - Strong leader
     - Leader election
       - election timeout
         - randomize election timeouts
       - need contain all votes committed
       - more than half votes(odd)
       - first-come-first-serves
       - votes to the term bigger candidates
     - Log replication
       - Log Matching Property
       - slow not impact
     - Safety: non-Byzantine
       - Leader Completeness Property
       - idempotent
       - boradcast time << election Timeout << MTBF
     - Membership changes
   - State Machine
   - Term as a logical clock.
   - Communicate using RPCs.
     - RequestVote RPCs
     - AppendEntries RPCs
     - transferring snapshot RPCs
