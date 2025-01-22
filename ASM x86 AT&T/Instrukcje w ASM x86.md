- `movl $1, %eax` - 
- `int $0x80` - 

Quick System Call Review: To recap - Operating System features are
accessed through system calls. These are invoked by setting up the
registers in a special way and issuing the instruction int $0x80. Linux
knows which system call we want to access by what we stored in the
%eax register. Each system call has other requirements as to what needs to
be stored in the other registers. System call number 1 is the exit system
call, which requires the status code to be placed in %ebx.