# h1 ff

1. write-ahead logging: The changes are first recorded in the log, which must be written to stable storage, before the changes are written to the database; all modifications are written to a log before they are applied.


    The purpose of this can be illustrated by an example. Imagine a program that is in the middle of performing some operation when the machine it is running on loses power. Upon restart, that program might need to know whether the operation it was performing succeeded, succeeded partially, or failed.
    
    (1). succeeded: the program wants to write data ```hello```, if it successfully writes ```hello``` to a buffer(still in the middle of perfoming this operation) before the power goes off, then when it resumes, it will compare to what was in the log, writing ```hello```, which means it will do nothing, since it already write ```hello```(keep things as they are).
    
    (2). succeeded partially: before the power goes off, the program only write ```hell```(no ```o``` at the end), then when it resumes, it will compare the log, and complete what it had started.
    
    (3). failed: before the power goes off, the program write ```dog``` which is wrong, then when the program restarts, it will compare the log, and found out that it was supposed to write ```hello```, but it wrote ```dog```,(which is wrong), therefore, it needs to undo what it had started(already written ```dog```), and start writing the correct ```hello``` from the begining. 
    
    If a write-ahead log is used, the program can check this log and compare what it was supposed to be doing when it unexpectedly lost power to what was actually done. On the basis of this comparison, the program could decide to undo what it had started, complete what it had started, or keep things as they are.
    
    