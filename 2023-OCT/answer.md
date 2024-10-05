# AACS3064 OCT 2023 Answers

[Link to the paper](https://eprints.tarc.edu.my/26849/1/AACS3064.pdf)

- [Question 1](#question-1)
- [Question 2](#question-2)
- [Question 3](#question-3)
- [Question 4](#question-4)

## Answers

### Question 1

a) i)

- Convert each digit to binary representation

  - F<sub>16</sub> => 1111<sub>2</sub>
  - D<sub>16</sub> => 1101<sub>2</sub>
  - A<sub>16</sub> => 1010<sub>2</sub>
  - C<sub>16</sub> => 1100<sub>2</sub>

- FD.AC<sub>16</sub> = 1111 1101 . 1010 1100<sub>2</sub>

- Group digits into triplets => 011 111 101 . 101 011<sub>2</sub>

- Convert each triplet into octal representation

  - 011<sub>2</sub> => 3<sub>8</sub>
  - 111<sub>2</sub> => 7<sub>8</sub>
  - 101<sub>2</sub> => 5<sub>8</sub>
  - 101<sub>2</sub> => 5<sub>8</sub>
  - 011<sub>2</sub> => 3<sub>8</sub>

- Answer: 375.53<sub>8</sub>

ii)

- Separate into integer component [1234] and decimal component [0.56]
- Integer component

  1234 ÷ 16 = 77 remainder 2

  77 ÷ 16 = 4 remainder 13 (D)

  4 ÷ 16 = 0 remainder 4

  4D2<sub>16</sub>

- Decimal component

  0.56 × 16 = 8 + 0.96
  
  0.96 × 16 = 15(F) + 0.36
  
  0.36 × 16 = 5 + 0.76
  
  0.76 × 16 = 12(C) + 0.16
  
  0.16 × 16 = 2 + 0.56

  8F5C2<sub>16</sub>

- Answer: 4D2.8F5C2...<sub>16</sub>

iii) 

4 × 5<sup>1</sup> + 1 × 5<sup>0</sup> + 4 × 5<sup>-1</sup> + 2 × 5<sup>-2</sup>

= 20 + 1 + 0.8 + 0.08

= 21.88<sub>10</sub>

iv)

- Group digits into quadruplets => 0110 1010 . 1010<sub>2</sub>
- Convert each number into hexadecimal representation
  - 0110<sub>2</sub> = 6<sub>16</sub>
  - 1010<sub>2</sub> = A<sub>16</sub>
  - 1010<sub>2</sub> = A<sub>16</sub>

Answer: 6A.A<sub>16</sub>

b)

- Convert numbers into binary representation
  - -127<sub>10</sub> = -0111 1111<sub>2</sub>

    127 ÷ 2 = 63 remainder 1
    
    63  ÷ 2 = 31 remainder 1
    
    31  ÷ 2 = 15 remainder 1
    
    15  ÷ 2 = 7 remainder 1
    
    7  ÷ 2 = 3 remainder 1
    
    3  ÷ 2 = 1 remainder 1
    
    1  ÷ 2 = 0 remainder 1

  - -1<sub>10</sub> = -0000 0001<sub>2</sub>

    1  ÷ 2 = 0 remainder 1

- Apply two's complement onto the negative numbers
  - -127<sub>10</sub>
    - Flip all bits : 0111 1111 => 1000 0000
    - Add one: 1000 0000 + 1 = 1000 0001
  - -1<sub>10</sub>
    - Flip all bits : 0000 0001 => 1111 1110
    - Add one: 1111 1110 + 1 = 1111 1111

- Add the numbers
  ```
       1000 0001
   +   1111 1111
  ---------------
     1 1000 0000
  ```

  Carry is ignored. Answer : 1000 0000

- Verify the answer

  -127<sub>10</sub> + (-1<sub>10</sub>) = -128<sub>10</sub>

  For the binary value calculated above, apply two's complement to get the decimal representation
  
  - Flip all bits : 1000 0000 => 0111 1111
  - Add one : 1000 0000

    1 × 2<sup>7</sup> = 128<sub>10</sub>

  - Prepend negative sign : -128<sub>10</sub>

- The answer is within the 8 bit binary representable range, hence the answer is valid. The answer produces carry, but it doesn't overflow.

c) i)

- Provide zero exponent : -0.0099999 × 10<sup>0</sup>
- Adjust the exponent: 0.99999 × 10<sup>-2</sup>
- Get the exponent in excess-50 notation
  50 + (-2) = 48
- Get the mantissa: 99999
- Get the sign: Negative => 9

Answer: 9 48 99999

ii)

- Multiply the mantissa
  0.12345 × 0.54321 = 0.067059 = 0.67059 × 10<sup>-1</sup>
- Add the exponent and minus 50
  48 + 49 - 50 = 47
- Adjust back the excess-50 exponent and add it to the result
  47 - 50 = -3
  
  -1 + (-3) = -4
  
  0.67059 × 10<sup>-4</sup>
- Multiply the mantissa with exponent
  0.000067059  
- Get the sign
  (+) × (-) = (-)

Answer: -0.000067059

d)

- Separate the number into integer component [87<sub>10</sub>] and decimal component [0.125<sub>10</sub>]
- Convert each to binary representation
  - 87<sub>10</sub> = 101 0111<sub>2</sub>

    87 ÷ 2 = 43 remainder 1
    
    43  ÷ 2 = 21 remainder 1
    
    21  ÷ 2 = 10 remainder 1
    
    10  ÷ 2 = 5 remainder 0
    
    5  ÷ 2 = 2 remainder 1
    
    2  ÷ 2 = 1 remainder 0
    
    1  ÷ 2 = 0 remainder 1

  - 0.125<sub>10</sub> = 0.001<sub>2</sub>

    0.125 × 2 = 0 + 0.25
    0.25 × 2 = 0 + 0.5
    0.5 × 2 = 1 + 0.0

- Combine the values: + 101 0111.001<sub>2</sub>
- Provide zero exponent : 101 0111.001 × 2<sub>0</sub>
- Adjust the exponent : 1.0101 1100 1 × 2<sub>6</sub>
- Get the mantissa (23 bits) : 0101 1100 1000 0000 0000 000
- Find the exponent in excess-127
  127 + 6 = 133
- Convert exponent to binary
  
  133 ÷ 2 = 66 remainder 1
    
  66  ÷ 2 = 33 remainder 0
    
  33  ÷ 2 = 16 remainder 1
    
  16  ÷ 2 = 8 remainder 0
    
  8  ÷ 2 = 4 remainder 0
    
  4  ÷ 2 = 2 remainder 0
    
  2  ÷ 2 = 1 remainder 0

  1 ÷ 2 = 0 remainder 1

  Exponent: 1000 0101<sub>2</sub>

- Get the sign

  Positive => 0

Answer: 0 1000 0101 0101 1100 1000 0000 0000 000<sub>2</sub>

# Question 2
