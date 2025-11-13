
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

Hexadecimal (or hex) is a system with base 16. The 16 digits used in the hexadecimal system and their equivalent value in binary and in denary systems are shown in the following table.

<p align="center">
<img src="/images/illustrations/Hextable.png" width="50%" height="auto">
</p>

It can be noted from the above table that each nibble (a group of 4 bits) can be represented with 1 digit in the hexadecimal system. It is very convenient to write in numbers in hex compared to the binary system. It is helpful for programmers coding in low-level languages. Instead of 4 bits, it is enough if they type a single character. The memory location in a computer is also stated in hexadecimal form. This makes the address more readable. Consider a memory address A3F581. Is represented in binary, it would be:
1010| 0011| 1111| 0101| 0100| 0001

### Converting Binary to hexadecimal

Binary numbers can be easily converted into a hexadecimal number. Starting from right to left, the binary numbers are split into groups of 4 bits. If the group has less than 4 bits, zeros are added to the left. Each nibble is then converted to its equivalent hexadecimal number.
Let us convert 10111011001010 to hexadecimal.

<p align="center">
<img src="/images/illustrations/binarytohex.png" width="50%" height="auto">
</p>

### Converting hexadecimal to binary

Hexadecimal numbers are converted to binary by finding the 4-bit code and writing the nibbles together.
Let us convert 9AF into binary

<p align="center">
<img src="/images/illustrations/hextobinary.png" width="50%" height="auto">
</p>

### Converting denary to hexadecimal

To convert a denary number to hexadecimal, the number is converted to binary first. Then, the binary number is converted to the hexadecimal system.
Let us consider converting the number 14. The binary form is 1110, which is E in the hexadecimal system.
Let us consider the denary number 131. 

<p align="center">
<img src="/images/illustrations/denarytohex.png" width="50%" height="auto">
</p>

### Converting hexadecimal to denary

Hexadecimal numbers can be converted to the denary system by using the place values. Let us consider converting hexadecimal number 7AF into the denary system. The place value is in the powers of 16. The value of each digit is multiplied with the place value and the values are added to find the denary equivalent.

<p align="center">
<img src="/images/illustrations/hextodenary.png" width="50%" height="auto">
</p>

  
### Watch Video below for a demo:
<iframe width="560" height="315" src="https://www.youtube.com/embed/duBPL-3hreI?si=KL0tYF_lhMC8IWps" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

## Application of the hexadecimal system

The hexadecimal system is a convenient form to represent information compared to binary. A nibble is represented in one digit of the hex system.  A few applications of the hex system are explained below:

### Colours
Hexadecimal numbers are used to represent colours in various software tools. A colour is represented in #RRGGBB format. RR, GG and BB represent the hex number of red, green and blue colours. A pure blue colour is #0000FF, white is #FFFFFFF and black is #0000000. Using this method, 256 variants of each colour can be made, making a total of 256 reds ×256 greens ×256 blues. A shade of yellow is represented in hex format as #FEF65B.
<p align="center">
<img src="/images/illustrations/Hexcolours.png" width="50%" height="auto">
</p>

### RGB Colour model
Colours can also be represented using the RGB colour model. This system is similar to the hex system but each colour has a value between 0 to 255. Hence, a shade of pink represented in hex format as #FEF65B has an R value of 254, G value of 246 and B value of 91.

<p align="center">
<img src="/images/illustrations/hexrgb.png" width="50%" height="auto">
</p>

### Errors
Error messages contain a hex number that represents the memory location of the error. This information is very useful to programmers. The error can be easily rectified by verifying the code in that particular location. The contents of part of a memory helps the programmer to solve many problems. The process in which the contents of memory is displayed or stored in a storage drive in case of a system crash is called a memory dump. An example of a memory dump is shown in the figure below.

<p align="center">
<img src="/images/illustrations/hexerrors.png" width="50%" height="auto">
</p>

Using this information, a programmer can identify the exact location where the error lies. Compared to binary, this is easier to understand. The binary form of DEF6B2C3 is: 11011110111101101011001011000011.
Even though using the hexadecimal system improves readability of errors, the programmer must have knowledge about the computer architecture to interpret the results.


### MAC Addresses

A media access control address refers to the number that uniquely identifies a device on the Internet. This is the address of the network interface card (NIC). A MAC address is made up of 48 bits, which are shown as a six-group of hexadecimal digits. 
NN-NN-NN-DD-DD-DD or NN: NN: NN: DD: DD: DD

The first half of the address represents the identification number of the manufacturer and the second half of the number represents the serial number of the device. For example: 00: 14: 22: 34: AC: 4F refers to a device made by Dell with a serial number of 34AC4F.

There are two types of MAC address: Universally Administered MAC Address (UAA) and Locally Administered MAC Address (LAA). 
The UAA is set by manufacturer and is most commonly used. This address is not changed most of the times. In case the UAA of a device is changed, it is important to make sure that the UAA is unique.  

A user or organisation may change their UAA due to:
Some software applications used on mainframe systems requires the systems to use a MAC address that follows a strict format. To ensure that all devices have MAC address that obey this format, it may be changed.

A router or firewall may allow MAC addresses with certain format only. In order to bypass them, MAC address of device may be changed.
Some networks may restrict certain MAC addresses. In order to use the network, certain devices may have their MAC addresses changed. 


### URL

Hexadecimal values are used to represent web addresses or URL (Uniform Resource Locator). The ASCII codes are used to represent the web address. For example:
www.google.com becomes: (using the ASCII codes)

<p align="center">
<img src="/images/illustrations/hexurl.png" width="50%" height="auto">
</p>

The percentage (%) symbol denotes that hexadecimal values are used. Hexadecimal values are used to represent addresses of files and web pages to improve security.  A user is protected from accessing a fake website when he is asked to use a hexadecimal URL rather than a URL with letters that could be misleading. 


### Assembly code and machine code

Machine code and assembly code can be used to refer the computer memory directly. Use of hexadecimal numbers makes low-level language coding easier, faster and reduces errors compared to the binary system. For example: An assembly code instruction ADD is translated to machine code as 0100, which is equivalent to 4 in hexadecimal. It is enough for the programmer to type a single digit ‘4’ compared to four digits ‘0100’.

### Hypertext Markup Language (HTML)
HTML is a markup language, widely used in developing web pages. It is used to define the attributes of text such as colour. Tags are used to define objects in a web-page. For example: The tag <p> is used to define a paragraph. The tag </p> represents its end. The contents between the two are codes. 
Earlier in this section, we have learnt how hexadecimal codes are used to represent colours. These codes are also used in html to define objects.

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

### Representing negative numbers

Signed integers can be either positive or negative. An extra bit is used to represent the sign of a number in binary representation. In the case of signed numbers, the leftmost bit is used to represent the sign and is called the sign bit. 0 represents a positive number and 1 represents a negative number. The rest of the bits represent the magnitude of the number. Consider the 8-bit binary number 10001101.

<p align="center">
<img src="/images/illustrations/signedbit1.png" width="50%" height="auto">
</p>

The smallest number that can be represented using 8 bits is 11111111 (-127) and the largest number is 01111111 (+127). Similarly, the signed number can be represented in 32-bits, 64-bits and so on.
Finding two’s complement is an alternate method to represent negative numbers. This method is used by most computers to perform mathematical operations.
Let us consider an example of representing -5. The binary value of 5 is 101. The leftmost bit is added to represent the positive sign. +5 is 0101. Each bit is inverted and, hence, the 0101 becomes 1010. 1 is added to this number. 1010 + 1=1011. A few examples of representing binary numbers using two’s complement are given in the table below:

<p align="center">
<img src="/images/illustrations/signedbit2.png" width="50%" height="auto">
</p>

### Steps to convert signed denary numbers to two’s complement:
- Convert the positive form number to binary.
- Invert the bits, i.e., 1 to 0 and 0 to 1
- Add 1.
  
For example:
Converting -17 to its two’s complement form.

<p align="center">
<img src="/images/illustrations/converttonegative.png" width="50%" height="auto">
</p>

### Steps to convert two’s complement number to denary:
- Subtract 1.
- Invert the bits, i.e., 1 to 0 and 0 to 1
- Convert the binary number to denary and add a negative symbol.
  
Converting the negative two’s complement number obtained previously.

<p align="center">
<img src="/images/illustrations/sumtwocomplement.png" width="50%" height="auto">
</p>

### Sum of numbers: Using two's complement

Let us consider adding -4 and 3 using two’s complement.
<p align="center">
<img src="/images/illustrations/convertbackpositive.png" width="50%" height="auto">
</p>

Converting the sum 1111 into denary number,
-8+4+2+1=-1




### Watch Video below:
<iframe width="560" height="315" src="https://www.youtube.com/embed/PhNzIphrP80?si=GninTLBNGUqNgyV-" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
