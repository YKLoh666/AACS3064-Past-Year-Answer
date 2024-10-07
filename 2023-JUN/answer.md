# AACS3064 JUN 2023 Answers

[Link to the paper](https://eprints.tarc.edu.my/25092/1/AACS3064.pdf)

- [Question 1](#question-1)
- [Question 2](#question-2)
- [Question 3](#question-3)
- [Question 4](#question-4)

## Answers

### Question 1

a) i)

  575 ÷ 16 = 35 remainder 15 (F)

  35 ÷ 16 = 2 remainder 3

  2 ÷ 16 = 0 remainder 2

  Answer: 23F<sub>16</sub>

ii)

  3 × 16<sup>2</sup> + 3 × 16<sup>1</sup> + 3 × 16<sup>0</sup> 

= 768 + 48 + 3

= 819<sub>10</sub>

iii)

  1 × 2<sup>3</sup> + 1 × 2<sup>1</sup> + 1 × 2<sup>0</sup> + 1 × 2<sup>-3</sup>

= 8 + 2 + 1 + 0.125

= 11.125<sub>10</sub>

iv)

- Group digits into quadruples : 0011 0010<sub>2</sub>
- Convert each quadruple into hexadecimal digit

  0011<sub>2</sub> = 3<sub>16</sub>

  0010<sub>2</sub> = 2<sub>16</sub>

Answer: 32<sub>16</sub>

b) i)

- Convert each number into binary representation
  - -30<sub>10</sub> = -0001 1110<sub>2</sub>

    30 ÷ 2 = 15 remainder 0

    15 ÷ 2 = 7 remainder 1

    7 ÷ 2 = 3 remainder 1

    3 ÷ 2 = 1 remainder 1

    1 ÷ 2 = 0 remainder 1

  - -20<sub>10</sub> = -0001 0100<sub>2</sub>

    20 ÷ 2 = 10 remainder 0

    10 ÷ 2 = 5 remainder 0

    5 ÷ 2 = 2 remainder 1

    2 ÷ 2 = 1 remainder 0

    1 ÷ 2 = 0 remainder 1

- Apply two's complements to each number
  - -30<sub>10</sub>
    - Flip all bits: 0001 1110 => 1110 0001
    - Add one: 1110 0001 + 1 = 1110 0010
  - -20<sub>10</sub>
    - Flip all bits: 0001 0100 => 1110 1011
    - Add one: 1110 1011 + 1 = 1110 1100
   
- Add the numbers

  ```
       1110 0010 (-30)
   +   1110 1100 (-20)
  ---------------
     1 1100 1110
  ```

  Carry is ignored, hence answer: 1100 1110

ii)

- Apply two's complements to get number in unsigned value
  - Flip all bits: 1100 1110 => 0011 0001
  - Add one: 0011 0001 + 1 = 0011 0010
 
- Find value in decimal

  1 × 2<sub>5</sub> + 1 × 2<sub>4</sub> + 1 × 2<sub>1</sub>

= 32 + 16 + 2

= 50

- Prepend the negative sign => -50<sub>10</sub>

- -30<sub>10</sub> + (-20<sub>10</sub>) = -50<sub>10</sub>

c) i)

- Provide zero exponent: 110322811 × 10<sup>0</sup>
- Adjust the exponent: 0.110322811 × 10<sup>9</sup>
- Get the exponent in excess-50
  - 50 + 9 = 59
- Get the mantissa: 11032 (rounded to 5 digits)
- Get the sign: (+) => 0

Answer: 0 59 11032

ii)

- Convert the operation to addition by changing second operand's sign

  ```
     0 52 52892
   + 0 50 29343
  --------------
  ```

- Adjust the exponent and mantissa of second operand

  ```
     0 52 52892
   + 0 52 0029343
  --------------
  ```

- Calculate the value of mantissa

  0.52892 + 0.0029343 = 0.53185 × 10<sup>0</sup> (No exponent adjustment needed)

- Prepend the sign and exponent to get the answer: 0 52 53185

d)

- Provide zero exponent: 1001.001100011<sub>2</sub> × 2<sup>0</sup>
- Adjust the exponent: 1.001001100011<sub>2</sub> × 2<sup>3</sup>
- Get the exponent in excess-127
  - 127 + 3 = 130<sub>10</sub> = 1000 0010<sub>2</sub>

    130 ÷ 2 = 65 remainder 0

    65 ÷ 2 = 32 remainder 1

    32 ÷ 2 = 16 remainder 0

    16 ÷ 2 = 8 remainder 0

    8 ÷ 2 = 4 remainder 0
    
    4 ÷ 2 = 2 remainder 0

    2 ÷ 2 = 1 remainder 0

    1 ÷ 2 = 0 remainder 1

- Get the mantissa: 0010 0110 0011 0000 0000 000
- Get the sign: positive => 0

Answer: 0 1000 0010 0010 0110 0011 0000 0000 000<sub>2</sub>

### Question 2

a)

- Convert the segment address into 20 bits representation
  - AB44<sub>H</sub> => AB440<sub>H</sub>
- Add the offset

  ```
     AB440 H
   +  5ADC H
  -----------
     B0F1C H
  ```

Answer: B0F1C<sub>H</sub>

b)

Logical Address | Physical Address
-|-
program address that is used to represent the location of instruction/data stored | actual address that physically existed which is used by the memory to indicate the location
format dependent on the processing system | format dependent on the memory itself

c)

- There must be a means to control devices with different specifications. This can be achieved with I/O module which can translate the instruction and signals among CPU and different I/O devices
- There must be a means for I/O device to communicate with the CPU. This can be achieved with interrupt capability which can signal the CPU about the device status so CPU can decides the instruction to execute accordingly.

d) i)

PC -> MAR ; MAR : 20

MDR -> IR ; IR : 740

IR<sub>[address]</sub> -> MAR ; MAR : 40

MDR -> A ; A : 2<sub>10</sub>

PC + 1 -> PC ; PC : 21

ii)

PC -> MAR ; MAR : 21

MDR -> IR ; IR : 641

IR<sub>[address]</sub> -> MAR ; MAR : 41

A + MDR -> A ; A : 2<sub>10</sub> + 5<sub>10</sub> = 7<sub>10</sub>

PC + 1 -> PC ; PC : 22

iii)

PC -> MAR ; MAR : 22

MDR -> IR ; IR : 440

IR<sub>[address]</sub> -> MAR ; MAR : 40

A -> MDR ; MDR = 7<sub>10</sub>

PC + 1 -> PC ; PC : 23

### Question 3

a)

- Advantages of memory
  - Memory can be accessed and processed by the CPU fast. This could increase the CPU throughput.
  Memory serves as temporary data storage that stores actively used instructions and data. Reducing disk access could allow the CPU to gain performance.
  - Memory creates a smoother multitasking experience. The memory stores the context of each application, allowing the system to switch between processes quickly.
- Examples
  - RAM: when the user opens a calculator application, the instructions for arithmetic operations are stored in the RAM, which can be used when the user performs calculations.
  - ROM: it is written with system startup instruction, which will be used by the CPU to perform the computer startup routine, ensuring the system is well initialised.
 
b)

- Addition: a number can be accumulated with another number to get its sum.
  - 0011 (3) + 0100(4) = 0111 (7)
- Multiplication: a number can be multiplied by another number to get its product
  - 0010 (2) + 0011(3) = 0110 (6)
 
c)

- Fetch: The instruction referenced by the program counter is fetched from the main memory and stored in the instruction register
- Decode: The instruction is decoded and the CPU determines which operation to perform.
- Execute: the CPU carries out the operation defined by the instruction. As for arithmetic and logical operation, the Arithmetic Logic Unit performs the calculations.
- Store: The result is stored back in the main memory for future use.

d)

- Character input: The keyboard input transfers a single-byte data from the keyboard to the CPU. Example: alphabetical and numerical characters.
- Control input: The keyboard input that tells a computer to perform an instruction. Example: Ctrl + C which tells the computer to perform a copying operation

### Question 4

a) i) `E 100 1D3538415B5A`

ii) `E 102 69`

iii) `D 108`

iv) `U 100 110`

b)

```assembly
MOV AX, N
ADD AX, 8
ADD AX, M
MOV L, AX
```

c)

i)

```assembly
arr BYTE 1,2,3,4,5,6,7,8,9
```

ii)

```assembly
Messagemin DB "Minimum value is: $"
Messagemax DB "Maximum value is: $"
```

iii)

```assembly
MOV AX, @DATA
MOV DS, AX
```

iv)

```assembly
MOV DH, arr[0] ; DH stores max value, initialised with first element
MOV DL, arr[0] ; DL stores min value, initialised with first element
MOV BX, 1 ; index points to second element
MOV CX, 8 ; loop for 8 times (minus one from first element, because it doesn't need to compare)
L1:
  MOV AL, ARR[BX] ; move current element to AL
  CMP AL, DL ; compare AL with minimum value
  JL is_smaller ; jump if it is lesser
  CMP AL, DH ; compare AL with maximum value
  JG is_larger ; jump if it is larger
  JMP next_loop ; proceed to next loop if it is none of the current min/max

  is_smaller:
    MOV DL, AL ; update minimum value with current number
    JMP next_loop ; proceed to next loop

  is_larger:
    MOV DH, AL ; update maximum value with current number

  next_loop:
    INC BX ; increment index to next element
    LOOP L1 ; loop back to the start
```

v)

```assembly
is_larger:
  MOV DL, AL
  ADD DL, 30H ; change value into character
  MOV AH, 02H ; dos service to print one character
  INT 21H
  MOV max, DL ; max stores the maximum value in character
```

vi)

```assembly
LEA DX, Messagemax
MOV AH, 09H
INT 21H

MOV DL, max ; max stores the maximum value in character
MOV AH, 02H
INT 21H
```

vii)

```assembly
MOV AX, 4C00H
INT 21H
```
