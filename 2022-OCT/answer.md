# AACS3064 OCT 2022 Answers

[Link to the paper](https://eprints.tarc.edu.my/28544/1/AACS3064.pdf)

- [Question 1](#question-1)
- [Question 2](#question-2)
- [Question 3](#question-3)
- [Question 4](#question-4)

## Answers

### Question 1

a) i)

- Convert each digit to binary representation
  - 4<sub>8</sub> = 100<sub>2</sub>
  - 7<sub>8</sub> = 111<sub>2</sub>
  - 6<sub>8</sub> = 110<sub>2</sub>
  - In binary: 100 111 110<sub>2</sub>
- Group digits into quadruplets: 0001 0011 1110<sub>2</sub>
- Convert each quadruplet into the hexadecimal representation
  - 0001<sub>2</sub> = 1<sub>16</sub>
  - 0011<sub>2</sub> = 3<sub>16</sub>
  - 1110<sub>2</sub> = E<sub>16</sub>
- Answer: 13E<sub>16</sub>

ii)

1 × 2<sup>7</sup> + 1 × 2<sup>6</sup> + 1 × 2<sup>3</sup> + 1 × 2<sup>2</sup> + 1 × 2<sup>0</sup>

= 128 + 64 + 8 + 4 + 1

= 205<sub>10</sub>

iii)

1396 ÷ 8 = 174 remainder 4

174 ÷ 8 = 21 remainder 6

21 ÷ 8 = 2 remainder 5

2 ÷ 8 = 0 remainder 2

Answer: 2564<sub>8</sub>

iv)

- Group digits into quadruples: 1011 0101 . 0001 0110<sub>2</sub>
- Convert each quadruple to its hexadecimal digit
  - 1011<sub>2</sub> = B<sub>16</sub>
  - 0101<sub>2</sub> = 5<sub>16</sub>
  - 0001<sub>2</sub> = 1<sub>16</sub>
  - 0110<sub>2</sub> = 6<sub>16</sub>

Answer: B5.16<sub>16</sub>

b) i) 

- Convert each of the numbers into binary representation
  - -120<sub>10</sub> = -0111 1000<sub>2</sub>

    120 ÷ 2 = 60 remainder 0

    60 ÷ 2 = 30 remainder 0

    30 ÷ 2 = 15 remainder 0

    15 ÷ 2 = 7 remainder 1
    
    7 ÷ 2 = 3 remainder 1

    3 ÷ 2 = 1 remainder 1

    1 ÷ 2 = 0 remainder 1

  - -7<sub>10</sub> = -0000 0111<sub>2</sub>
    
    7 ÷ 2 = 3 remainder 1

    3 ÷ 2 = 1 remainder 1

    1 ÷ 2 = 0 remainder 1
    
- Apply two's complements to each number
  - -120<sub>10</sub>
    - Flip all bits: 0111 1000 => 1000 0111
    - Add one: 1000 0111 + 1 = 1000 1000
  - -7<sub>10</sub>
    - Flip all bits: 0000 0111 => 1111 1000
    - Add one: 1111 1000 + 1 = 1111 1001
   
- Add the number
  ```
       1000 1000
   +   1111 1001
  ---------------
     1 1000 0001
  ```

  Ignore the carry, answer: 1000 0001

ii)

-120<sub>10</sub> + (-7<sub>10</sub>) = -127<sub>10</sub>

- Apply two's complements
  - Flip all bits: 1000 0001 => 0111 1110
  - Add one: 0111 1110 + 1 = 0111 1111
- Convert to decimal

  1 × 2<sup>6</sup> + 1 × 2<sup>5</sup> + 1 × 2<sup>4</sup> + 1 × 2<sup>3</sup> + 1 × 2<sup>2</sup> + 1 × 2<sup>1</sup> + 1 × 2<sup>0</sup>

  = 64 + 32 + 16 + 8 + 4 + 2 + 1

  = (-)127<sub>10</sub>

c) i)

- Provide 0 exponent: -6058383 × 10<sup>0</sup>
- Adjust the exponent: -0.60584 × 10<sup>7</sup>
- Find exponent in excess-50 notation
  - 50 + 7 = 57
- Mantissa: 60584
- Sign: Negative: (-) = 5

Answer: 5 57 60584

ii)

- Adjust the exponent and mantissa
  ```
     5 52 13532
   + 0 52 000074812
  --------------
  ```

- Get the result of mantissa

  -0.13532 + 0.000074812 = -0.13525 × 10<sup>0</sup>

- Sign: (-) = 5
- Exponent: 52
- Mantissa: 13525

Answer: 5 52 13525

d)

- Provide zero exponent: 111110.1011100101<sub>2</sub> × 2<sup>0</sup>
- Adjust exponent: 1.111101011100101<sub>2</sub> × 2<sup>5</sup>
- Mantissa: 1111 0101 1100 1010 0000 000
- Get exponent in excess-127
  127 + 5 = 132

  132 ÷ 2 = 66 remainder 0

  66 ÷ 2 = 33 remainder 0

  33 ÷ 2 = 16 remainder 1

  16 ÷ 2 = 8 remainder 0
    
  8 ÷ 2 = 4 remainder 0

  4 ÷ 2 = 2 remainder 0

  2 ÷ 2 = 1 remainder 0
    
  1 ÷ 2 = 0 remainder 1

  Answer: 1000 0100
- Sign: Positive = 0
- Answer: 0 1000 0100 1111 0101 1100 1010 0000 000<sub>2</sub>

### Question 2

a)

- Convert the segment address to 20-bit representation
  - BD78 H × 16 = BD780 H
- Add the offset
  ```
     BD780 H
   +  2EDC H
  -----------
     C065C H
  ```

b) Disagree, because the computer's register is a small, high-speed storage that sits between the CPU and memory to store the states of currently processing instructions. Meanwhile, the main memory is a large storage that stores the program instructions and data ready to be executed by the CPU.

c)

- The address of data needed by CPU is passed into the MAR
- MAR send the address signal to the address decoder
- The address decoder decodes the address and activates a single line that triggers the memory cell.
- The data inside the memory cell is copied into the MDR
> missed a point?

d) i) 

- PC -> MAR ; MAR = 20
- MDR -> IR ; IR = 180
- IR<sub>[address]</sub> -> MAR ; MAR = 80
- MDR -> A ; A = 8<sub>10</sub>
- PC + 1 -> PC ; 21

ii)

- PC -> MAR ; MAR = 21
- MDR -> IR ; IR = 381
- IR<sub>[address]</sub> -> MAR ; MAR = 81
- MDR + A -> A ; A = 12<sub>10</sub> + 8<sub>10</sub> = 20<sub>10</sub>
- PC + 1 -> PC ; 22

iii)

- PC -> MAR ; MAR = 22
- MDR -> IR ; IR = 280
- IR<sub>[address]</sub> -> MAR ; MAR = 80
- A -> MDR ; MDR = 20<sub>10</sub>
- PC + 1 -> PC ; 23

e) North Bridge and South Bridge

### Question 3

a) 

- The I/O module and main memory must have a physical connection. This ensures that the data can be transferred between memory and the I/O module.
- The I/O module must be able to perform read and write operations to the memory.
- The method to resolve conflict between the CPU and I/O module when they share a connection with the memory.

b) 

```
            CPU interface   Device interface
---------          --------------          ---------------
|  CPU  |----------| I/O Module |----------| I/O devices |
---------          --------------          ---------------
```

- The I/O Module serve as an interface between the CPU and I/O devices. It translates the CPU command to device-specific instruction and has the devices to perform it. The I/O module is also able to serve as a buffer for data pooling.

c)

- Advantage: Enables more data to be transmitted at the same time, which can reduce memory access.
- Disadvantage: Requires larger memory buffer register, which means need CPU with better compatibility.

d)

> this not sure what part of lecture note, so copy pasta from chatgpt

- Program Isolation: Logical addresses provide each program or process with its own virtual memory space, ensuring that **different programs cannot interfere with each other’s memory**. This isolation helps prevent memory corruption and improves system security and stability.

- Efficient Memory Management: Logical addresses allow the operating system to use techniques like **paging and segmentation**, which make more efficient use of physical memory. Programs can be larger than the available physical memory, as the OS can **swap portions of data in and out of RAM as needed**, without the program needing to know.

- Portability and Flexibility: Since logical addresses are independent of the actual physical addresses of the memory, programs can be relocated easily. This makes it possible to **load a program into different parts of physical memory without modifying the program's code**, thus providing flexibility in memory management.

### Question 4

a) i) E 100 54415220205543

ii) D 100

iii) E 104 554D54

b)

```assembly
MOV AX, Y
ADD AX, 3
SUB AX, Z
MOV X, AX
```

c) i)

```assembly
ARR DB 1,2,3,4,5
```

ii)

```assembly
TOTAL DB ?
MESSAGE DB "The total of odd numbers is: $"
```

iii)

```assembly
MOV AX, @DATA
MOV DS, AX
```

iv)

```assembly
MOV CX, 5
MOV BX, 0
L1:
  MOV AL, ARR[BX]
  AND AL, 1
  CMP AL, 1
  je odd_number
  LOOP L1
```

v)

```assembly
odd_number:
  MOV AL, ARR[BX]
  ADD TOTAL, AL
  LOOP L1
```

vi)

```assembly
LEA DX, MESSAGE
MOV AH, 09H
INT 21H
```

vii)

```assembly
MOV AX, 4C00H
INT 21H
```
