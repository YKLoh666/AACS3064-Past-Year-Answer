# AACS3064 JAN 2024 Answers

[Link to the paper](https://eprints.tarc.edu.my/27898/1/AACS3064.pdf)

- [Question 1](#question-1)
- [Question 2](#question-2)
- [Question 3](#question-3)
- [Question 4](#question-4)

## Answers

### Question 1

a) i)

- Convert each digit to binary representation

  - 1<sub>16</sub> => 0001<sub>2</sub>
  - 2<sub>16</sub> => 0010<sub>2</sub>
  - 4<sub>16</sub> => 0100<sub>2</sub>
  - 7<sub>16</sub> => 0111<sub>2</sub>
  - C<sub>16</sub> => 1100<sub>2</sub>

- 12.47C<sub>16</sub> = 0001 0010 . 0100 0111 1100<sub>2</sub>

- Group digits into triplets => 010 010 . 010 001 111 100<sub>2</sub>

- Convert each triplet into octal representation

  - 010<sub>2</sub> => 2<sub>8</sub>
  - 010<sub>2</sub> => 2<sub>8</sub>
  - 010<sub>2</sub> => 2<sub>8</sub>
  - 001<sub>2</sub> => 1<sub>8</sub>
  - 111<sub>2</sub> => 7<sub>8</sub>
  - 100<sub>2</sub> => 4<sub>8</sub>

- Answer: 22.2174<sub>8</sub>

ii)

- Separate into integer component [98] and decimal component [0.75]
- Integer component

  98 ÷ 16 = 6 remainder 2

  6 ÷ 16 = 0 remainder 6

  62<sub>16</sub>

- Decimal component

  0.75 × 16 = 12(C) + 0.0

  C<sub>16</sub>

- Answer: 62.C<sub>16</sub>

iii)

4 × 6<sup>1</sup> + 5 × 6<sup>0</sup> + 3 × 6<sup>-1</sup>

= 24 + 5 + 0.5 

= 29.5<sub>10</sub>

iv)

- Group digits into quadruplets => 0110 . 1100 <sub>2</sub>

- Convert each quadruplet into hexadecimal representation

  - 0110<sub>2</sub> = 5<sub>16</sub>
  - 1100<sub>2</sub> = 12 (C<sub>16</sub>)
 
- Answer: 5.C<sub>16</sub>

v) Number invalid, because octal number only consists of digits ranging from 0 to 7, but the number has digit of 8

b) i)

- Convert each number into binary representation

    55 ÷ 2 = 27 remainder 1

    27 ÷ 2 = 13 remainder 1
    
    13 ÷ 2 = 6 remainder 1

    6 ÷ 2 = 3 remainder 0

    3 ÷ 2 = 1 remainder 1

    1 ÷ 2 = 0 remainder 1

  - 55<sub>10</sub> = -0011 0111<sub>2</sub>

- Apply two's complement onto the values

  - Flip all bits: 0011 0111 => 1100 1000
  - Add one: 1100 1000 + 1 => 1100 1001
 
- Add the values

  ```
       1100 1001
   +   1100 1001
  ---------------
     1 1001 0010
  ```

  Carry is ignored. Answer => 1001 0010<sub>2</sub>

ii)

  -55<sub>10</sub> + (-55<sub>10</sub>) = -110<sub>10</sub>

- Apply two's complement on the answer in 1) b) i)

  - Flip all bits: 1001 0010 => 0110 1101
  - Add one: 0110 1101 + 1 => 0110 1110
 
- Convert to decimal

   1 × 2<sup>6</sup> + 1 × 2<sup>5</sup> + 1 × 2<sup>3</sup> + 1 × 2<sup>2</sup> + 1 × 2<sup>1</sup>

  = 64 + 32 + 8 + 4 + 2
  = 110

- Prepend the negative sign: -110<sub>10</sub>

iii) The answer produced a carry but did not overflow.

C) i)

- Get the sign
  - 9 => Negative (-)
- Get the exponent
  - 49 - 51 = -2
  - exponent => 10<sup>-2</sup>
- Get the mantissa
  - 0.88888
- Combine the result => -0.88888 × 10<sup>-2</sup>
- Adjust the exponent => -0.0088888

ii)

- Match the exponent

  ```
     0 51 024680
   + 0 51 08642
  --------------
  ```

- Add the mantissa

  0.024680 + 0.08642 = 0.1111 × 10<sup>10</sup> (no exponent adjustment needed)

- Get the mantissa and prepend the sign and exponent => 0 51 11110

iii)

- Provide zero exponent
  - 1010.0101 × 2<sup>0</sup>
- Adjust the exponent
  - 1.0100101 × 2<sup>3</sup>
- Get the exponent in excess-127
  - 127 + 3 = 130
- Convert the exponent to binary

  130 ÷ 2 = 65 remainder 0

  65 ÷ 2 = 32 remainder 1
    
  32 ÷ 2 = 16 remainder 0

  16 ÷ 2 = 8 remainder 0

  8 ÷ 2 = 4 remainder 0

  4 ÷ 2 = 2 remainder 0
    
  2 ÷ 2 = 1 remainder 0

  1 ÷ 2 = 0 remainder 1

  Exponent in binary (Excess-127) = 1000 0010

- Get the mantissa (23 bits)
  - 0100 1010 0000 0000 0000 000
- Get the sign
  - Positive => 0
- Answer: 0 1000 0010 0100 1010 0000 0000 0000 000<sub>2</sub>

### Question 2

a)

PC -> MAR ; MAR = 34

MDR -> IR ; IR = 156

IR<sub>[address]</sub> -> MAR ; MAR = 56

MDR -> A ; A = 12

PC + 1 -> PC ; PC = 35

PC -> MAR ; MAR = 35

MDR -> IR ; IR = 257

IR<sub>[address]</sub> -> MAR ; MAR = 57

MDR + A -> A; A = 34 + 12 = 46

PC + 1 -> PC ; PC = 36

PC -> MAR ; MAR = 36

MDR -> IR ; IR = 356

IR<sub>[address]</sub> -> MAR ; MAR = 56

A -> MDR ; MDR = 46

PC + 1 -> PC ; PC = 37

b)

- RISC perform tasks with registers-oriented instructions. This can reduce memory access by allowing the register to hold the task-relevant data.
- RISC uses instruction words with fixed length and format. This can ease instruction decoding and make pipelining possible.
- RISC has limited address mode. A reduced number of address modes simplifies the implementation and speeds up instruction executions.
- RISC consists of a large bank of registers. An increased number of registers allows more data to be held, reducing memory access to increase speed.

c) i) Instruction Register (IR)

ii)Memory Address Register (MAR)

### Question 3

a) i) 

```assembly
- A 1234:100
MOV AX, 5
MOV DL, 4
DIV DL
```

ii) AH holds the remainder and AL holds the quotient

b) i) (Segment Address) × 16 + (Offset Address)

ii) 

- CS:IP
  - Get the 20-bit representation of segment address
    
    3456 H => 34560 H
    
  - Add the offset
    
    ```
       34560 H
     +  AB1F H
    -----------
       3F07F H
    ```
    
  - Answer: 3F07F H
- SS:BP
  - Get the 20-bit representation of segment address
    
    1357 H => 13570 H
    
  - Add the offset
    
    ```
       13570 H
     +  3829 H
    -----------
       16D99 H
    ```
    
  - Answer: 16D99 H

c)

- Interrupt can act as an external event notifier. The CPU doesn't need to perform polling, freeing up processing power.
- Interrupt can be used as a completion signal. The computer can be notified when the device is done performing a task and proceed with the consecutive tasks.
- Interrupt can be used as a means for CPU allocation. CPU can multitask by having multiple programs running, and shifting its attention from program to program through interrupts.
- Interrupt can serve as an abnormal event indicator. CPU can quickly respond to abnormal events such as power failure and illegal operations.

d)

- Use of multiprocessor. Using multiple processors increases the system throughput by enabling more powerful parallel processing.
- Increase CPU clock speed. A CPU with a higher clock speed can speed up the machine cycle which increases the system's single-thread performance.
- Larger memory capacity. A larger RAM capacity reduces disk access, which increases the speed of performing memory-intensive tasks.

### Question 4

a)

- Line 5: CL = 24h, DL = 63h
- Line 6: BL = 44h
- Line 7: CL = 23h
- Line 8: DL = C6h
- Line 9: AL = BBh

b)

> Only need to write the code pieces, the full code is for those who want to test this out

```assembly
.MODEL SMALL
.STACK 100H
.DATA

OPTION DB ?

; (i) ---------------------------------
PROMPT DB "Enter an option (1 or 2): $"
ERROR DB "Wrong option$"
; (i) ---------------------------------

.CODE

MAIN PROC FAR

; (ii) --------------------------------
MOV AX, @DATA
MOV DS, AX
; (ii) --------------------------------

; (iii) -------------------------------
MOV AH, 09H
LEA DX, PROMPT
INT 21H
; (iii) -------------------------------

; (iv) --------------------------------
MOV AH, 01H
INT 21H
MOV OPTION, AL
; (iv) --------------------------------

; (v) ---------------------------------
MOV DL, 0DH
MOV AH, 02H
INT 21H

MOV DL, 0AH
MOV AH, 02H
INT 21H
; (v) ---------------------------------

; (vi) --------------------------------
CMP OPTION, "1"
JE show_digit
CMP OPTION, "2"
JE show_alpha
JMP wrong_option
; (vi) --------------------------------

; (vii) -------------------------------
show_digit:
  MOV CX, 10
  MOV DL, "0"
  MOV AH, 02H
  L1:
    INT 21H
    INC DL
    LOOP L1
; (vii) -------------------------------
  JMP terminate

; (viii) ------------------------------
show_alpha:
  MOV CX, 10
  MOV DL, "A"
  MOV AH, 02H
  L2:
    INT 21H
    INC DL
    LOOP L2
; (viii) ------------------------------
  JMP terminate

; (ix) --------------------------------
wrong_option:
  MOV AH, 09H
  LEA DX, ERROR
  INT 21H
; (ix) --------------------------------

terminate:
; (x) --------------------------------
  MOV AX, 4C00H
  INT 21H
; (x) --------------------------------

MAIN ENDP

END MAIN
```
