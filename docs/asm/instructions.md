
# Instructions of JDH-8 Assembler

## ADC - Add with carry

Adds two values with carry

Sets CARRY flag if result larger than 8 bits

```asm
    adc reg, imm8/reg
```

## ADD - Add

Adds two values without carry

Sets CARRY flag if result larger than 8 bits

```asm
    add reg, imm8/reg
```

## ADD16 - Add 16-bit

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

## AND - Bitwise and

Perform bitwise AND operation on register with a value

`a, b -> a && b`
`a, b -> and(a, b)`

```asm
    and reg, imm8/reg
```

## CALL
## CLB
## CLC
## CLE
## CLF - Clear flags

Clears the flags register (F)

```asm
    clf
```

## CLL
## CMP - Compare

Compare register to value

Sets LESS flag if 1st is less than 2nd
Sets EQUAL flag

```asm
    cmp reg, imm8/reg
```

## DEC - Decrement

Decrements value in a register

Ignores BORROW flag by clearing flags first

```asm
    dec reg
```

## DEC16 - Decrement 16-bit

Decrements value in a register

1st and 2nd are a 16-bit value

```asm
    inc reg, reg
```

## EQ16 - Check 16-bit equal

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

## FDEC - Decrement with flags

Decrements value in a register

Without clearing the BORROW flag

```asm
    fdec reg
```

## HALT - Halt program

Sets the HALT status register

```asm
    halt
```

## INB - Inbound byte

Load value from device into register

2nd arg is device id

```asm
    inb reg, imm8/reg
```

## INC - Increment

Increments value in a register

```asm
    inc reg
```

## INC16 - Increment 16-bit

Increments value in a register

1st and 2nd are a 16-bit value

```asm
    inc reg, reg
```

## JB
## JC
## JEQ
## JGE
## JGT
## JLE
## JLT
## JMP
## JMS
## JNB
## JNC
## JNE
## JNZ - Jump if not zero

Jump if value does NOT equal zero

Jumps to location in HL

```asm
    jnz imm8/reg
```

## JZ
## LDA - Load address

Load location adress or 16-bit value into HL

```asm
    lda imm16
```

1st and 2nd are the destination 16-bit value

```asm
    lda reg, reg, imm16
```

1st and 2nd are the 16-bit location adress value

```asm
    lda reg/imm8, reg/imm8
```

## LW - Load word

Load value from memory to register

2nd value is location adress

```asm
    lw reg, imm16/HL
```

## LW16 - Load word 16-bit

Load 16-bit value from memory to register

Low byte is loaded from the location address + 1

1st and 2nd are a 16-bit value

3rd is location address

```asm
    lw16 reg, reg, imm16/HL
```

Overides and increments HL

```asm
    lw16 reg, reg
```

## MW - Move word

Move value into register

```asm
    mw reg, imm8/reg
```

## MW16 - Move word 16-bit

Move 16-bit value from/to registers

1st and 2nd are the 16-bit destination

```asm
    mw16 reg, reg, imm16
```

3rd and 4th are a 16-bit value

```asm
    mw16 reg, reg, reg, reg
```

## NAND - Bitwise nand

Perform bitwise NAND operation on register with value

`a, b -> !(a && b)`
`a, b -> not(and(a, b))`

```asm
    nand reg, imm8/reg
```

## NOR - Bitwise nor

Perform bitwise NOR operation on register with value

`a, b -> !(a || b)`
`a, b -> not(or(a, b))`

```asm
    nor reg, imm8/reg
```

## NOT - Bitwise not

Perform bitwise OR operation on register with value

`a -> !a`
`a -> not(a)`

```asm
    not reg
```

## OR - Bitwise or

Perform bitwise OR operation on register with value

`a, b -> a || b`
`a, b -> or(a, b)`

```asm
    or reg, imm8/reg
```

## OUTB - Outbound byte

Send a value from register to device

1st arg is device id

```asm
    outb imm8/reg, reg
```

```asm
    outb imm8/reg, imm8/reg
```

## POP - Pop off stack

Pop value from the top of the stack

Decrement the stack pointer (SP)

Put value into register

```asm
    pop reg
```

## POPA
## PUSH - Push onto Stack

Push value on top of the stack

Increment the stack pointer (SP)

```asm
    push imm8/reg
```

## PUSHA
## RET
## SBB - Subtract with borrow

Subtract value and borrow from register

```asm
    sbb reg, imm8/reg
```

## SIGN - Is value signed

Sets F register if value is negative (signed bit)

```asm
    sign immg8/reg
```

## SIGN16 - Is 16-bit value signed

Sets F register if 16-bit value is negative (signed bit)

1st and 2nd arguments are a 16-bit value

```asm
    sign16 reg, reg
```

## STB
## STC
## STE
## STL
## SUB - Subtract

Subtract value from register

```asm
    sub reg, imm8/reg
```

## SUB16 - Subtract 16-bit

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

## SW - Store word

Store value in memory

```asm
    sw imm16/HL, reg
```

## SW16 - Store word 16-bit

Store 16-bit value in memory

Low byte is stoed in the location address + 1

1rd is location address

2nd and 3rd are a 16-bit value

```asm
    sw16 imm16/HL, reg, reg
```

2nd is an 8-bit constant

```asm
    sw16 imm16/HL, imm8

```

Overides and increments HL

1st and 2nd are a 16-bit value

```asm
    sw16 reg, reg
```


## XNOR - Bitwise xnor

Perform bitwise XNOR operation on register with value

`a, b -> !(!(a && b) && (a || b))`
`a, b -> !xor(a, b)`

```asm
    xnor reg, imm8/reg
```

## XOR - Bitwise xor

Perform bitwise XOR operation on register with value

`a, b -> !(a && b) && (a || b)`
`a, b -> and(nand(a, b), or(a, b))`

```asm
    xor reg, imm8/reg
```

