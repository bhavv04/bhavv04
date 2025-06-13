```assembly
; 6502 Assembly - Developer Profile

        .org $1000

name:   .byte "Bhavdeep Arora"
stack:  .byte "C, Assembly, Python, Java, Kernel"
interest:  .byte "Embeeded System Security"
email:  .byte "bhavdeepsa@gmail.com"

start:  lda #$00        ; load accumulator with 0
        tax             ; transfer to X (commit counter)

ship:   inx             ; increment commits
        txa             ; transfer X to A
        cmp #$FF        ; compare with 255 (max 8-bit)
        beq done        ; branch if equal (overflow!)
        jmp ship        ; jump back to ship

done:   brk             ; break (we've shipped enough)

; EOF - End Of File
```
