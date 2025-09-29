---
title: IGCSE Computer Science
layout: page
description: About
bodyClass: page-about
---

# Lesson 1 Binary conversion (Denary to Binary/ Binary to Denary)

## Lesson Objective:
- To be able to convert decimal numbers to binary and binary numbers to decimal with accuracy
- To be able to explain the logical steps involved in binary conversion processes
- To apply binary conversion techniques to solve basic computational problems

## Key learning points

- Computers use binary to represent all data and instructions.
- Binary is a number system consisting of 1s and 0s.
- Binary can be represented by two-state electrical signals within circuits.
- A transistor that is “on” represents a 1; a transistor that is “off” represents a 0.

## Keywords

- Data - raw facts, such as numbers or text, presented without any meaning
- Binary - a number system that uses the digits 0 and 1 to represent data
- Instruction - directions on how to carry out a specific task
- Transistor - a tiny electronic switch controlled by electricity.

A computer has many electronic components that work as switches. These components have two logics as input and output: ON and OFF. A similar logic is used to represent data in binary form. ON is represented as 1, and OFF is represented as 0.  

### Place value of the denary system
The denary system has a base value of 10. It counts in multiples of 10. The number 7324 has 7 thousands, 3 hundreds, 2 tens and 4 ones. The following figure illustrates the place values in a denary system.
<p align="center">
<img src="/images/illustrations/placevaluedenary.png" width="50%" height="auto">
</p>


### Place value of the binary system
The binary numbers can also be represented using place values. The place values have a base 2. The first 8 digits are represented in the table below.
<p align="center">
<img src="/images/illustrations/placevaluebinary.png" width="50%" height="auto">
</p>

### Size of computer memory

A binary digit is referred to as a bit. A nibble consists of 4 bits. A byte consists of 8 bits. A byte is the smallest unit of memory of the computer system. The memory sizes available with computers are in multiples of 8 such as 16-bit systems, 32-bit systems, etc.

The memory sizes were originally standardised as using the base-2 representation. In this system, the prefixes kibi-, mebi-, gibi-, tebi- are used to avoid conflicts with base-10 system.

<p align="center">
<img src="/images/illustrations/newnamesize.png" width="50%" height="auto">
</p>

This representation is now used for representing the size of RAM modules only. After the standardisation of base-10 representation, the memory sizes are now represented as:

<p align="center">
<img src="/images/illustrations/base10 name.png" width="50%" height="auto">
</p>

### Converting denary to binary

<p align="center">
<img src="/images/illustrations/converting.png" width="50%" height="auto">
</p>

### Watch Video below for demo on how to convert:
<iframe width="560" height="315" src="https://www.youtube.com/embed/iAxeigunq3I?si=9RVaz_WUlWn9pzil" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


# Lesson 2 Binary addition
## Lesson Objective:
- To understand the principles of binary number representation and place value
- To be able to perform binary addition involving 1-bit and 2-bit numbers
- To know hot to apply rules for binary addition including carrying over
- To identify and explain overflow in binary arithmetic

## Key learning points
- The process of counting in binary follows the same principle as decimal.
- Binary addition can be achieved with the following facts: 0+0 = 0, 0+1 = 1, 1+1 = 10 and 1+1+1 = 11.

## Keywords
- Addition - a mathematical operation where two or more numbers are combined to find their total
- Carry - the extra value that moves to the next column when the sum of digits in a place value exceeds the basey.

### Representing numbers 
Programmers use many arithmetic operations in a program. The numbers are either represented as integers or floating point numbers. Integers are whole numbers and floating point numbers are used to represent numbers with decimal points. A 16-bit system can represent integers up to 216-1=65535. 8-bit, 16-bit, 32-bit and 64-bit are the most common bit lengths.

## Adding Binary numbers
Binary numbers are added in a column method as the denary numbers are added. Let us consider the following example of adding 0101 and 1011
<p align="center">
<img src="/images/illustrations/binaryaddition1.png" width="50%" height="auto">
</p>

When the binary digits 1 and 0 are added, the sum is 1. When both the digits are 0, the sum is 0. When both the digits are 1, the sum is 10 and 1 is carried over. 0101 and 1001 represent the denary numbers 5 and 9. The sum of 5 and 9 is 14. Convert the sum obtained to a denary number.

(8×1)+(4×1)+(2×1)+(0×1)=14


### The rules are:
- 1 + 0  = sum 1 and carry 0
- 1 + 1  = sum 0 and carry 1 
- 1 + 1 + (carry 1) = sum 1 and carry 1
- Adding three 1’s results in a sum of 1 and a carry of 1.

Another example: 
<p align="center">
<img src="/images/illustrations/binary addition 2.png" width="50%" height="auto">
</p>


### Watch Video below:

<iframe width="560" height="315" src="https://www.youtube.com/embed/iAxeigunq3I?si=Zl2MbTtDVHOORFTf" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


## Overflow error
A CPU with an 8-bit register has a capacity of up to 11111111 in binary. If an extra bit is added, it is said to be an overflow error. Consider the addition of two binary numbers 11101101 and 10000100 as shown below:

<p align="center">
<img src="/images/illustrations/overflowerror.png" width="50%" height="auto">
</p>

The sum of these two numbers is bigger than 8 bits (an extra bit than the register can hold). The computer thinks that 11101101+10000100=01110001 as it does not have space to store the extra bit. The number of bits a register can hold is called word size. Exceeding the capacity of word size in a register results in an overflow error. 



# Lesson 3 Hexadecimal

## Lesson Objective:
- To be able to explain the relationship between binary and hexadecimal number systems, including why hexadecimal is used in computing for compact representation.
- To convert binary numbers (up to 8 bits) into their equivalent hexadecimal values using grouping and place value techniques.
- To Convert hexadecimal numbers (up to 2 digits) into their equivalent binary values using place value understanding and 4-bit grouping techniques.

## Key learning points
- Hexadecimal is often used by humans instead of binary because it is easier to read and interpret and uses fewer digits.
- Hexadecimal is a base-16 number system.
- The digits used for hexadecimal are 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E and F.
  
## Keywords
- Hexadecimal - a base-16 number system that uses the digits 0-9 and the letters A, B, C, D, E and F
- Base-16 - a number system that uses 16 digits
  
### Watch Video below:
<iframe width="560" height="315" src="https://www.youtube.com/embed/duBPL-3hreI?si=KL0tYF_lhMC8IWps" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

# Lesson 4 Logical shift 

## Lesson Objective:
- To be able to perform left and right binary shifts on 8-bit binary numbers and explain their effect on the numerical value.
- To interpret how binary shifts can be used to multiply or divide binary numbers by powers of two, and identify limitations of this method
  
## Key learning points
- Binary shifting is shifting the bits to the left or to the right.
- If you shift to the left, you multiply the number by a power of 2.
- If you shift to the right, you divide the number by a power of 2.
- Overflow is when a number is too large to be stored in allocated memory.
- Underflow is when a number is too small to be processed.
  
## Keywords
- Binary shifting - when binary digits are moved left or right, multiplying or dividing them by powers of 2
- Overflow - when a number is too large to be represented in the available binary digits
- Underflow - when a number is too small to be represented in the available binary digits

### Binary shift

<p align="center">
<img src="/images/illustrations/binaryshift.png" width="50%" height="auto">
</p>

Again, it can be noted that the binary equivalent of 12 shifted to the left is the binary equivalent of 24. It can be summarised that when a denary number is multiplied by 2, its binary equivalent shifts left by 1 place. Also, multiplication by 4 results in the shift of the binary equivalent by 2 places and multiplication by 8 results in a shift of the binary equivalent by 3 places and so on.
During logical left shifts, sometimes bits might be lost. For example, multiplying 1000 0000 by 2 using a logical left shift will result in an overflow error and the result will be 0000 000. In practice, a different methodology is used to perform multiplication.
During logical right shifts, again lower significant bits might be lost resulting in a loss of precision. For example, dividing 0000 0101 (Denary number 6)  by 2 will result in 0000 0010 (denary number 2) which is incorrect.  

### Arithmetic shift

Logical shifts cannot be used for negative numbers stored in two’s- complement form. Let us consider the denary number -6. Its binary equivalent in two’s complement form is 1111 1001. Performing logical right shift, we get 0111 1100, which is equivalent to 124.  

Hence, to divide negative numbers in two’s-complement form, we use arithmetic right shifts. In this shift, all the bits are moved to right one place but the leftmost bit is kept the same.

<p align="center">
<img src="/images/illustrations/rightshift.png" width="50%" height="auto">
</p>

Arithmetic left shifts are performed similarly to logical left shifts. All bits are moved to left one place and the leftmost bit is kept as 0. -9 is multiplied by using arithmetic left shift as given below.

<p align="center">
<img src="/images/illustrations/leftshift.png" width="50%" height="auto">
</p>



### Watch Video below:
<iframe width="560" height="315" src="https://www.youtube.com/embed/Ml1zwSgfZ7g?si=v0b6X46SwUUigquI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

# Lesson 5 two's complements

## Lesson Objective:
- To be able to Explain how two’s complement is used to represent negative binary numbers and distinguish it from unsigned binary representation

  
## Key learning points

- Two’s complement allows binary representation of both positive and negative integers.
- The most significant bit (MSB) indicates the sign: 0 for positive, 1 for negative.
- To find the two’s complement of a binary number:
  - Invert all bits (one’s complement).
  - Add 1 to the result.
- Two’s complement simplifies binary arithmetic, especially subtraction.
-  Range of values for 8-bit two’s complement: −128 to +127.
  
## Keywords

- Sign Bit – The most significant bit (MSB) in two’s complement indicates the sign of the number: 0 for positive, 1 for negative.
  
### Watch Video below:
<iframe width="560" height="315" src="https://www.youtube.com/embed/PhNzIphrP80?si=GninTLBNGUqNgyV-" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
