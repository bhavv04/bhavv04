```
Bhavdeep Arora - Developer Profile
; Assembly x86-64

.section .data
    msg: .ascii "Hello World! 👋
          I'm Bhavdeep Arora, a Computer Science Student at Toronto Metropolitan University.
          Welcome to my GitHub profile! 🚀
          Feel free to explore my repositories."

.section .text
.global _start

_start:
    ; Print message
    mov $1, %rax        ; sys_write
    mov $1, %rdi        ; stdout
    mov $msg, %rsi      ; message
    mov $155, %rdx      ; message length
    syscall
    
    ; Exit
    mov $60, %rax       ; sys_exit
    mov $0, %rdi        ; status
    syscall

; Compile: as -64 profile.s -o profile.o && ld profile.o -o profile
; Run: ./profile
```
