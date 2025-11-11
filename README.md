
# SORTING---8051

**AIM:**

To write and execute Assembly language Program for sorting of data using 8051 keil.

**APPARATUS REQUIRED: Personal computer with Keil software**

**(i) Descending order ALGORITHM:**

1.	Initialize the register r7 with count.
2.	Get first two elements in two registers.
3.	Compare the two elements of data. If value of R0 register is low, then exchange A & R0 data else increment pointer and decrement register R7.
4.	Check R7 is zero, and then move the register R0 & A.
5.	Again increment pointer and decrement R7,
6.	Check R7 is zero. If no repeat the process from step 2.
7.	Otherwise stop the program.

**PROGRAM:**

ORG 0000H 

MOV R7,#4

LOOP1:MOV R0,#40H 

MOV R6,#04

LOOP: MOV A,@R0 

INC R0

MOV 50H,@R0 

CJNE A,50H,NEXT 

SJMP DOWN 

NEXT:JNC DOWN 

MOV @R0,A

DEC R0

MOV @R0,50H 

DOWN:DJNZ R6,LOOP 

DJNZ R7,LOOP1

END


**OUTPUT:**

**MEMORY WINDOW:**

Before execution: D:0x40H:
<BR>
<BR>
<img width="1284" height="725" alt="image" src="https://github.com/user-attachments/assets/ea260d06-8359-4e4d-8ec0-526762181a6e" />

<BR>
After execution: D:0x40H:
<BR>
<BR>
<img width="1281" height="725" alt="image" src="https://github.com/user-attachments/assets/bcfef17b-523c-4a07-82c8-0e3887093fd8" />

<BR>


**(ii)	Ascending order**
 
**ALGORITHM:**

1.	Initialize the register r7 with count.
2.	Get first two elements in two registers.
3.	Compare the two elements of data. If value of R0 register is high then exchange A & R0 data else increment pointer and decrement register R7.
4.	Check R7 is zero, and then move the register R0 & A.
5.	Again increment pointer and decrement R7,
6.	Check R7 is zero. If no repeat the process from step 2.
7.	Otherwise stop the program.

**PROGRAM:**

ORG 0000H 

MOV R7,#4

LOOP1:MOV R0,#40H

MOV R6,#04

LOOP: MOV A,@R0

INC R0

MOV 50H,@R0 

CJNE A,50H,NEXT

SJMP DOWN 

NEXT:JC DOWN

MOV @R0,A

DEC R0

MOV @R0,50H 

DOWN:DJNZ R6,LOOP 

DJNZ R7,LOOP1

END

**OUTPUT:**

**MEMORY WINDOW:** 

**Before execution:**
D:0x40H:
<BR>
<img width="1345" height="769" alt="Screenshot 2025-10-23 160055" src="https://github.com/user-attachments/assets/61d5ba22-87cf-4c95-a799-6c68f249a387" />





<BR>
<BR>
<BR>
After execution:
D:0x40H:
<BR>
<BR>
<img width="1347" height="786" alt="Screenshot 2025-10-23 160112" src="https://github.com/user-attachments/assets/0f14ae2b-62c6-403d-af40-cae7af7de3e5" />




<BR>
**Result:**

Thus the sorting of given data was done using 8051 keil and shown the output.

