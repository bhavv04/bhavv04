```assembly
section .data
    name        db "Bhavdeep Arora", 0
    role        db "Inspiring Embedded System Security Engineer", 0
    status      db "Student At Toronto Metropolitan University (Formerly Ryerson University)", 0
    skills      db "C/C++, Assembly, Python, Rust, Linux Kernel", 0

section .text
    global _start

_start:
    ; Load developer profile
    mov eax, name
    mov ebx, role
    mov ecx, skills
    
    ; Execute main routine
    call display_info
    call show_stats
    
    ; Contact info
    push "bhavdeepsa@gmail.com"
    call contact
    
    ; Exit successfully
    mov eax, 1
    mov ebx, 0
    int 0x80

; EOF - profile.asm

```

