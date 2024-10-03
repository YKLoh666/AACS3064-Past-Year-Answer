# AACS3064 JUN 2024 Answers

[Link to the paper](https://eprints.tarc.edu.my/28544/1/AACS3064.pdf)

- [Question 1](#question-1)
- [Question 2](#question-2)
- [Question 3](#question-3)
- [Question 4](#question-4)

## Answers

### Question 1

a) i) 

888 ÷ 16 = 55 remainder 8

55 ÷ 16 = 3 remainder 7

3 ÷ 16 = 0 remainder 3

888<sub>10</sub> = 378<sub>16</sub>

ii)

1 × 16<sup>3</sup> + 2 × 16<sup>2</sup> + F × 16<sup>1</sup> + A × 16<sup>0</sup>

= 1 × 16<sup>3</sup> + 2 × 16<sup>2</sup> + 15 × 16<sup>1</sup> + 10 × 16<sup>0</sup>

= 4096 + 512 + 240 + 10

= 4858<sub>10</sub>

iii)

1 × 2<sup>3</sup> + 1 × 2<sup>2</sup> + 1 × 2<sup>1</sup> + 1 × 2<sup>0</sup>

= 8 + 4 + 2 + 1

= 15<sub>10</sub>

iv)

- Group binary into sets of 4

  - 111101<sub>2</sub> = 0011 1101<sub>2</sub>

- Convert each set into respective hexadecimal digit
  - 0011 = 3<sub>16</sub>
  - 1101 = D<sub>16</sub>

Answer = 3D<sub>16</sub>

b) i)

- Convert each number into binary representation
  - -10<sub>10</sub> = -0000 1010<sub>2</sub>

    10 ÷ 2 = 5 remainder 0

    5 ÷ 2 = 2 remainder 1
    
    2 ÷ 2 = 1 remainder 0

    1 ÷ 2 = 0 remainder 1

  - -80<sub>10</sub> = -0101 0000<sub>2</sub>

    80 ÷ 2 = 40 remainder 0

    40 ÷ 2 = 20 remainder 0
    
    20 ÷ 2 = 10 remainder 0

    10 ÷ 2 = 5 remainder 0

    5 ÷ 2 = 2 remainder 1
    
    2 ÷ 2 = 1 remainder 0

    1 ÷ 2 = 0 remainder 1

- Apply two's complement to each of the numbers
  - -0000 1010<sub>2</sub> (-10)
    - Flip all bits : 0000 1010 => 1111 0101
    - Add one : 1111 0101 + 1 = 1111 0110
  - -0101 0000<sub>2</sub> (-80)
    - Flip all bits : 0101 0000 => 1010 1111
    - Add one : 1010 1111 + 1 = 1011 0000

- Add both numbers
  ```
       1111 0110
   +   1011 0000
  ---------------
     1 1010 0110
  ```

Carry is ignored, hence answer => 1010 0110

ii)

-10<sub>10</sub> + (-80<sub>10</sub>) = -90<sub>10</sub>

- Apply two's complement to the anwser in b) i)
  - Flip all bits : 1010 0110 => 0101 1001
  - Add one : 0101 1001 + 1 = 0101 1010

- Convert back to decimal

  1 × 2<sup>6</sup> + 1 × 2<sup>4</sup> + 1 × 2<sup>3</sup> + 1 × 2<sup>1</sup>

  = 64 + 16 + 8 + 2

  = 90<sub>10</sub>

- Prepend the negative sign => -90<sub>10</sub>

c) i)

- Provide 0 exponent
  - 5888712 × 10<sup>0</sup>
- Adjust the exponent
  - 0.5888712 × 10<sup>7</sup>
- Find exponent in excess-50
  - 50 + 7 = 57
- Get mantissa
  - 5888712 rounded to 58887
- Get sign
  - Positive => 0
 
Answer: 0 57 58887

ii) 

- Change the sign of the second operand and the operation
  ```
     0 52 72212
   + 0 50 30232
  --------------
  ```

- Adjust the mantissa to match exponent
  ```
     0 52 72212
   + 0 52 0030232
  --------------
  ```

- Add the mantissa
  ```
     72212
   + 0030232
  -----------
     7251432
  ```

- Prepend back the sign and exponent (no adjustment to the exponent), and round the mantissa to 5 digit

  Answer: 0 52 72514

d)

- Provide 0 exponent
  - 1011.11110101 × 2<sup>0</sup>
- Adjust the exponent
  - 1.01111110101 × 2<sup>3</sup>
- Find the exponent in excess-127
  - 127 + 3 = 130
- Convert exponent to binary
  
  130 ÷ 2 = 65 remainder 0

  65 ÷ 2 = 32 remainder 1
    
  32 ÷ 2 = 16 remainder 0

  16 ÷ 2 = 8 remainder 0

  8 ÷ 2 = 4 remainder 0

  4 ÷ 2 = 2 remainder 0
    
  2 ÷ 2 = 1 remainder 0

  1 ÷ 2 = 0 remainder 1

  Exponent in binary (Excess-127) = 1000 0010
  
- Get mantissa
  - 0111 1110 1010 0000 0000 000
- Get sign bit
  - Positive => 0

Answer: 0 1000 0010 0111 1110 1010 0000 0000 000

### Question 2

a)

- Convert segment address to 20 bit representation
  - CF88 H => CF880 H
- Add the offset
  ```
     CF880 H
   +  3ABC H
  -----------
     D333C H
  ```

Answer: D333C H

b)

- Hardware communication components are physical electronic devices that transfer data from one place to another
  - Example: Modem, Network Card Interface (NIC)
- Software communication components, commonly known as network protocols, are predefined standard rules to coordinate and interpret the data transferred
  - Example: HyperText Transfer Protocol (HTTP)

c)

- Data bus: Carry data from components to components

- Address Bus: Carry metadata such as the recipient and destination of the data transmitted in the data bus

- Control Bus: Carry signals such as timing and component's status to coordinate communication between components.

d) i)

PC -> MAR ; MAR = 30

MDR -> IR ; IR = 180

IR<sub>[address]</sub> -> MAR ; MAR = 80

MDR -> A ; A = 10<sub>10</sub>

PC + 1 -> PC ; PC = 31

ii)

PC -> MAR ; MAR = 31

MDR -> IR ; IR = 181

IR<sub>[address]</sub> -> MAR ; MAR = 81

MDR + A -> A ; A = 10<sub>10</sub> + 20<sub>10</sub> = 30<sub>10</sub>

PC + 1 -> PC ; PC = 32

iii)

PC -> MAR ; MAR = 32

MDR -> IR ; IR = 182

IR<sub>[address]</sub> -> MAR ; MAR = 82

A -> MDR ; MDR = 30<sub>10</sub>

PC + 1 -> PC ; PC = 33

### Question 3

a) 

- Vectored Interrupt
  - Interrupt is executed by having the devices direct the processor to perform the appropriate Interrupt Service Routine (ISR).
  - Example: A printer sends an interrupt code to the CPU to signal it about the completion of printing. The CPU uses the interrupt code to look up the instruction location of the ISR in memory using the Interrupt Vector Table (IVT). The CPU then jump to the corresponding location to execute the ISR.
- Polled Interrupt
  - CPU checks the status of the devices periodically to determine if the device requires attention or service.
  - Example: The CPU checks for the keyboard status periodically. If the keyboard shows a status that requires the CPU to accept a keystroke, the CPU will pause the polling process and execute the service to carry out the task.

b) 

- The I/O module interface the communication between I/O device and CPU. The I/O module interprets device-specific commands and translates them into signals to control the computer hardware.
- The I/O module supports interrupt capability. It enables the CPU to process other tasks and only give attention to the device when it requests CPU attention through an interrupt.

c)

- A wider path for memory access. It can help to transmit data at a higher rate while reducing memory access.
- Memory interleaving divides the memory into multiple blocks with points of access. This allows the memory to be accessed simultaneously, which is beneficial for parallel processing.
- Cache memory is a memory that sits between CPU and random access memory that stores a copy of frequently used data in RAM. This memory has a smaller size but allows quicker data retrieval so the CPU can execute instructions quicker.

d)

- Multiprocessors allow faster execution of tasks through parallel processing.
- CPU with a faster clock speed can speed up the fetch execute cycle, which also increases the execution speed.
- A wider bus could allow the instruction and data to transfer at a higher rate with reduced memory and disk access.
- Increasing the amount of memory can allow it to hold more data and instruction, reducing the slower disk access and improving task execution speed.

### Question 4

a) i) `E 100 6E8088313C3D` (no space, because space is the delimiter to separates the arguments)

ii) `E 101 55`

iii) `D 100`

iv) `U 100 110`

b)

```assembly
MOV AX, Q
ADD AX, 3
MOV DX, P
SUB DX, AX
MOV O, DX
```

c)

```assembly
.MODEL SMALL
.STACK 100H
.DATA
ARR DB 1,2,3,4,5,6,7,8,9
MSG DB "Decimal value is: $"
MSG2 DB "Binary equivalent value is: $"
CRLF DB 0DH, 0AH, "$"

.CODE
.386

MAIN PROC FAR
MOV AX, @DATA
MOV DS, AX

MOV CX, 9 ; COUNTER = 9
MOV BX, 0 ; INDEX = 0

L1:

LEA DX, MSG ; PRINT MSG
MOV AH, 09H
INT 21H

MOV DL, ARR[BX] ; PRINT DECIMAL
ADD DL, 30H
MOV AH, 02H
INT 21H

LEA DX, CRLF ; PRINT NEW LINE
MOV AH, 09H
INT 21H

LEA DX, MSG2 ; PRINT MSG2
MOV AH, 09H
INT 21H

PUSH CX ; SAVE L1 COUNTER VALUE
MOV CX, 4 ; L2 COUNTER = 4, BECAUSE PRINT 4 BINARY DIGITS
L2:
MOV DL, ARR[BX] ; MOV INTO DX
SHL DX, 1 ; SHIFT LEFT ONCE
SHR DX, CL ; SHIFT RIGHT BASED ON COUNTER
AND DL, 1 ; RESERVE ONLY RIGHT MOST BIT VALUE
ADD DL, 30H ; ADD 30H TO BECOME NUMERICAL CHARACTER
MOV AH, 02H ; PRINT BINARY DIGIT
INT 21H
LOOP L2

LEA DX, CRLF ; PRINT NEW LINE
MOV AH, 09H
INT 21H

POP CX ; RESTORE L1 COUNTER VALUE
INC BX ; INCREMENT INDEX
LOOP L1

MOV AX, 4C00H ; TERMINATE PROGRAM
INT 21H
MAIN ENDP

END MAIN
```
