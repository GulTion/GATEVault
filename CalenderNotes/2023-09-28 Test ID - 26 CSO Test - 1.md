---
title: Test ID - 26 CSO Test - 1
allDay: true
date: 2023-09-28
completed: null
---
# Number System COA

## Zeal Question #ques/ZW/COA/Number_System

### **Note** #notes/COA/number_system/base_from_roots_of_ploynomial

1. Find the Base of Numbers for Quardic Equation ![[Pasted image 20230928112103.png]]
2. Find the Base of Numbers for Cubic Equation Equation ![[Pasted image 20230928112320.png]]![[Pasted image 20230928112338.png]]

### Ranges of Number Form
The range of Sign-Magnitude form is from $-(2^{n-1}-1) \space to \space (2^{n-1}-1)$ #notes/COA/number_system/range/signed_magnitude 

The range of one's complement is from $-(2^{n-1}-1) \space to \space (2^{n-1}-1)$ #notes/COA/number_system/range/ones_complement

The range of two's complement form is from $-(2^{n-1}) \space to \space (2^{n-1}-1)$ #notes/COA/number_system/range/twos_complement

# Floating Point Tricks
#ques/ZW/COA/Number_System/floating_point
![[CalenderNotes/media/Untitled.png]]
1. **Calculate the Exponent Based so Fast**

	M = 10000011
	
	subtract by 128 (remove the MSB) ⇒ 11 then add 1 ⇒ 11 + 1 ⇒ 100
	
	anwser ⇒ 4

2. **Convert Binary to Decimal so Fast**
    1. e.g. 100000011
        1. digit after the first MSB is 8 ⇒ 2^8 ⇒ 256 digit after the add the 11 ⇒ 256 + 3 ⇒ 259