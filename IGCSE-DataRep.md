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

### Watch Video below:

<iframe width="560" height="315" src="https://www.youtube.com/embed/iAxeigunq3I?si=Zl2MbTtDVHOORFTf" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

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

# Lesson 4 Ligical shift 

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
