
# Assembler

## Instructions

### ADC - Add with carry

Adds two values with carry

Sets CARRY flag if result larger than 8 bits

```asm
    adc reg, imm8/reg
```

### ADD - Add

Adds two values without carry

Sets CARRY flag if result larger than 8 bits

```asm
    add reg, imm8/reg
```

### ADD16 - Add 16-bit

Add value to 16-bit value

1st and 2nd are a 16-bit value

3rd is an 8-bit value

```asm
    add16 reg, reg, imm8/reg
```

3rd is an 16-bit value

```asm
    add16 reg, reg, imm16
```

3rd and 4th are a 16-bit value

```asm
    add16 reg, reg, imm8/reg, imm8/reg
```

### AND - Bitwise and

Perform bitwise AND operation on register with a value

```asm
    and reg, imm8/reg
```

### CALL
### CLB
### CLC
### CLE
### CLF - Clear flags

Clears the flags register (F)

```asm
    clf
```

### CLL
### CMP - Compare

Compare register to value

Sets LESS flag if 1st is less than 2nd
Sets EQUAL flag

```asm
    cmp reg, imm8/reg
```

### DEC - Decrement

Decrements value in a register

Ignores BORROW flag by clearing flags first

```asm
    dec reg
```

### DEC16 - Decrement 16-bit

Decrements value in a register

1st and 2nd are a 16-bit value

```asm
    inc reg, reg
```

### EQ16 - Check 16-bit equal

Check if 2 16-bit values are equal

Sets EQUAL flag

1st and 2nd are a 16-bit value

3rd is an 8-bit value

```asm
    eq16 reg, reg, imm8/reg
```

3rd and 4th are a 16-bit value

```asm
    eq16 reg, reg, imm8/reg, imm8/reg
```

### FDEC - Decrement with flags

Decrements value in a register

Without clearing the BORROW flag

```asm
    fdec reg
```

### HALT - Halt program

Sets the HALT status register

```asm
    halt
```

### INB - Inbound byte

Load value from device into register

2nd arg is device id

```asm
    inb reg, imm8/reg
```

### INC - Increment

Increments value in a register

```asm
    inc reg
```

### INC16 - Increment 16-bit

Increments value in a register

1st and 2nd are a 16-bit value

```asm
    inc reg, reg
```

### JB
### JC
### JEQ
### JGE
### JGT
### JLE
### JLT
### JMP
### JMS
### JNB
### JNC
### JNE
### JNZ - Jump if not zero

Jump if value does NOT equal zero

Jumps to location in HL

```asm
    jnz imm8/reg
```

### JZ
### LDA - Load address

Load adress or 16-bit value into HL

```asm
    lda imm16
```

### LW - Load word

Load value from memory to register

```asm
    lw reg, imm16/HL
```

### LW16
### MW - Move word

Move value into register

```asm
    mw reg, imm8/reg
```

### MW16
### NAND
### NOR - Bitwise nor

Perform bitwise NOR operation on register with value

```asm
    nor reg, imm8/reg
```

### NOT
### OR - Bitwise or

Perform bitwise OR operation on register with value

```asm
    or reg, imm8/reg
```

### OUTB - Outbound byte

Send a value from register to device

1st arg is device id

```asm
    outb imm8/reg, reg
```

```asm
    outb imm8/reg, imm8/reg
```

### POP - Pop off stack

Pop value from the top of the stack

Decrement the stack pointer (SP)

Put value into register

```asm
    pop reg
```

### POPA
### PUSH - Push onto Stack

Push value on top of the stack

Increment the stack pointer (SP)

```asm
    push imm8/reg
```

### PUSHA
### RET
### SBB - Subtract with borrow

Subtract value and borrow from register

```asm
    sbb reg, imm8/reg
```

### SIGN
### SIGN16
### STB
### STC
### STE
### STL
### SUB - Subtract

Subtract value from register

```asm
    sub reg, imm8/reg
```

### SUB16 - Subtract 16-bit

Subtract value from 16-bit value

1st and 2nd are a 16-bit value

3rd is an 8-bit value

```asm
    sub16 reg, reg, imm8/reg
```

3rd is an 16-bit value

```asm
    sub16 reg, reg, imm16
```

3rd and 4th are a 16-bit value

```asm
    sub16 reg, reg, imm8/reg, imm8/reg
```

### SW - Store word

Store value in memory

```asm
    sw imm16/HL, reg
```

### SW16
### XNOR
### XOR
