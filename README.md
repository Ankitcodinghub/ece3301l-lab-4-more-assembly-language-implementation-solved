# ece3301l-lab-4-more-assembly-language-implementation-solved
**TO GET THIS SOLUTION VISIT:** [ECE3301L LAB 4-More Assembly language implementation Solved](https://www.ankitcodinghub.com/product/ece3301l-lab-4-more-assembly-language-implementation-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;91483&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;ECE3301L LAB 4-More Assembly language implementation Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
More Assembly language implementation

This lab will get you to implement further uses of the Assembly language by introducing you to some arithmetic, logical and branching instructions. Below is a link to a website that provides some good references to the PIC18F instructions:

http://technology.niagarac.on.ca/staff/mboldin/18F_Instruction_Set/

PART 1)

The first part is to implement a basic program to input a number from DIP switches, take its 1’s complement and display the result out to the LEDs:

</div>
</div>
<div class="layoutArea">
<div class="column">
C Code:

void main() {

char InA; char Result;

ADCON1 TRISA TRISB TRISC

while (1) {

InA InA Result PORTB

} }

Use the lab3 Part 2) as a baseline for the implementation of this part. Modify it to add the following handling:

<ol>
<li>1) &nbsp;Declare the two variables ‘InA’ and ‘Result’ as two memory locations.</li>
<li>2) &nbsp;Read the content of PORTA into register W</li>
</ol>
</div>
</div>
<div class="layoutArea">
<div class="column">
= 0x0f; = 0xff; = 0x00;

= 0xff;

= PORTA;

= InA &amp; 0x0F; = (1’s) InA;

= Result;

</div>
<div class="column">
// make sure PORT A is input // make sure PORT B is output // make sure PORT C is input

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
<ol start="3">
<li>3) &nbsp;Mask in the lower 4-bit of W with the constant 0x0F by using the instruction ANDLW.</li>
<li>4) &nbsp;Store the result into the variable InA (a memory location)</li>
<li>5) &nbsp;Perform the 1’s complement of the variable InA through the use of the
‘COMF’ instruction. Use the option to store back to W instead of memory
</li>
</ol>
(COMF InA, 0)

<ol start="6">
<li>6) &nbsp;Mask in the lower 4-bit of W using ANDLW.</li>
<li>7) &nbsp;Next, use ‘MOVWF’ to output to the variable ‘Result’.</li>
<li>8) &nbsp;Finally, use ‘MOVFF’ to get the content of ‘Result’ into ‘PORTB’.</li>
<li>9) &nbsp;Branch back to the step 2) to make the operation an infinite loop</li>
</ol>
When done, use the 4 switches connected to PORTA to set a number. Observe the result being displayed on the PORTB that should show the 1’s complement of the number specified by the DIP switches.

Make sure that the connections of the DIP switches and the LEDs are implemented such a way that the MSB (most significant bit) of the number is on the leftmost side while the LSB is on the rightmost side. Also, don’t forget that when a switch is turned ON, this means logic 0 and when it is off, the logic is 1.

PART 2)

Take the implementation in Part 1) and add the following test condition between steps 8) and step 9) above;

a) Ifthe‘Result’is0,thenPORTEbit1willbesetto1 b) Else that same bit is reset to 0.

</div>
</div>
<div class="layoutArea">
<div class="column">
void main() {

ADCON1 TRISA TRISB TRISC

while (1) {

</div>
<div class="column">
= 0x0f; = 0xff; = 0x00;

= 0xff;

= PORTA;

= InA &amp; 0x0F; = (1’s) InA;

= Result;

</div>
<div class="column">
// make sure PORT A is input // make sure PORT B is output // make sure PORT C is input

// Set PORTE bit 1 to 1 // Set PORTE bit 1 to 0

</div>
</div>
<div class="layoutArea">
<div class="column">
} }

</div>
</div>
<div class="layoutArea">
<div class="column">
InA InA Result PORTB

</div>
</div>
<div class="layoutArea">
<div class="column">
if (Zero flag == 1) PORTE = 0x02; else PORTE = 0x00;

</div>
</div>
<div class="layoutArea">
<div class="column">
In this exercise, we will add another test after the completion of the Complement operation. We need to check if the Zero (Z flag) is set through the use of the instruction

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
BZ. If Z flag is 1, BZ will force a jump to a label where PORTE bit 1 is set to 1. If Z flag is 0, the instruction just below the BZ instruction will be executed. There clear PORTE bit 1 to be 0.

When done go back to the main loop using the ‘GOTO MAIN_LOOP’ code.

To set a bit ‘x’ of a PORTy, you will use the instruction ‘BSF PORTy,x’. To clear a bit ‘x’ of a PORTy, use ‘BCF PORTy,x’.

The example below will show a typical implementation:

BZ LABEL1

( Place instruction here to clear PORTE bit 1 to 0) GOTO LABEL2

LABEL1:

(Place instruction here to set PORTE bit 1 to 1)

LABEL2:

GOTO MAIN_LOOP

When done, implement, compile and test the code on the board. Input a number such that the result displays 0 and the Z flag LED is turned on.

PART 3)

We will now implement a new operation that will add two numbers. Copy the routine developed in part 2). Add codes to read a second input from PORTC and stored it into the variable ‘InC’. Next, perform an addition between the two inputs ‘InA’ and ‘InC’ and stored the result into ‘Result’. Also, display the result into PORTB.

</div>
</div>
<div class="layoutArea">
<div class="column">
void main() {

char InA; char InC; char Result;

ADCON1 TRISA TRISB TRISC

while (1) {

</div>
<div class="column">
= 0x0f; = 0xff; = 0x00;

= 0xff;

</div>
<div class="column">
// make sure PORT A is input // make sure PORT B is output // make sure PORT C is input

</div>
</div>
<div class="layoutArea">
<div class="column">
InA

InA

InC

InC

Result

PORTB = Result;

</div>
</div>
<div class="layoutArea">
<div class="column">
=PORTA;

= InA &amp; 0x0f; = PORTC;

= InC &amp; 0x0f; = InA + InC;

</div>
</div>
</div>
<div class="page" title="Page 4">
<div class="layoutArea">
<div class="column">
} }

</div>
</div>
<div class="layoutArea">
<div class="column">
if (Zero flag == 1) Set PORTE.bit1 to 1 else Clear PORTE.bit1 to 0

</div>
</div>
<div class="layoutArea">
<div class="column">
Use the instruction ‘ADDWF f,0’ where f is the memory location that has the value to add to the register W.

When completed, set two numbers for inputs on the DIP switches and check the result shown on the 5 LEDs connected to PORTB. The fifth LED of PORTB will show the overflow of the result of the addition of two 4-bit numbers.

PART 4)

Replace the ADD operation on part 3) by doing the ‘AND’ operation with the instruction ‘ANDWF f,0’. Verify that the operation is implemented properly.

PART 5)

Replace the ADD operation on part 3) by doing the ‘OR’ operation with the instruction ‘ORWF f,0’. Verify that the operation is implemented properly.

PART 6)

One last routine is to take a 4-bit input number and convert into a BCD number which is the decimal equivalent of the input number.

To do the conversion, the input number is checked against the value 0x09. If it is greater than 9, then add a constant 0x06 to it. If it is less than 9, then no addition of the constant is needed. For example:

<ol>
<li>a) &nbsp;If input = 0x08, then output = 0x08 (no change)</li>
<li>b) &nbsp;If input = 0x0b, then output = 0x0b + 0x06 = 0x11. 0x0b has the decimal
equivalent of 11. This will the number 11 which is the decimal equivalent of

0x0b
</li>
<li>c) &nbsp;If input = 0x0d, then output = 0x0d + 0x06 = 0x13 because 0x0d is 13 in
decimal.
</li>
</ol>
To implement the operation, here are some steps:

<ol>
<li>a) &nbsp;Read the input into the variable ‘InA’</li>
<li>b) &nbsp;Load a constant 0x09 into W</li>
</ol>
</div>
</div>
</div>
<div class="page" title="Page 5">
<div class="layoutArea">
<div class="column">
c) Use the instruction CPFSGT (see reference) to compare the value in ‘InA’ against the W register (that contains 0x09). If ‘‘InA’is greater than 0x09, the next instruction below this instruction is executed. Otherwise, the next instruction is skipped:

CPFSLT InA, 1 (go here if greater or =) (go here if less)

PART 7)

Take the basic code of each of the five functions implemented above and group them into five different sets of code. Call each group by the name of the function it performs like:

SUBROUTINE_COMP: SUBROUTINE_ADD: SUBROUTINE_AND: SUBROUTINE_OR: SUBROUTINE_BCD:

At the end of each group where the instruction ‘GOTO MAIN_LOOP’ is called, replace that line by the line ‘RETURN’.

Here is a typical implementation: SUBROUTINE_ COMP:

(code from the COMP implementation) RETURN

SUBROUTINE_ ADD:

(code from the ADD implementation) RETURN

Next, start at the beginning of the program with a basic loop that will constantly check three new switches connected to PORTD bits 2 and 0. These three switches will select what function to execute as follows:

</div>
</div>
</div>
<div class="page" title="Page 6">
<div class="layoutArea">
<div class="column">
PORT D

Bit_2 Bit_1 Bit_0

0 0 0 0 0 1 0 1 0

<ol start="0">
<li>0 &nbsp;1 1</li>
<li>1 &nbsp;x x</li>
</ol>
</div>
<div class="column">
Action

1’s complement ADD operation AND operation OR operation BCD conversion

</div>
</div>
<div class="layoutArea">
<div class="column">
Use the ‘BTFSC’ instructions to do the decoding of the five tasks to jump to. Once the differentiation is done, we will have five different labels, each for each task. At each task, first use the BCF and BSF to set the three bits 5-7 of the PORTD to show what routine is being executed. For example, task ‘001’ is for the ‘ADD’ function. The LEDs connected to PORTD bits 4-6 should also show the value ‘001’. Next, use the ‘CALL’ instruction to call the respective subroutine that was created for each task. It will force the execution of the appropriate routine for that task. After the ‘CALL’ was executed, a GOTO MAIN_LOOP instruction should be called in order to go back to the main loop. Here is a typical implementation:

</div>
</div>
<div class="layoutArea">
<div class="column">
MAIN_LOOP:

BTFSC PORTD, 2

GOTO PORTD1xx GOTO PORTD0xx

PORTD1xx:

GOTO TASK_BCD

PORTD0xx:

BTFSC PORTD, 1 GOTO PORTD01x GOTO PORTD00x

PORTD01x:

BTFSC PORTD, 0

GOTO … GOTO …

PORTD00x:

BTFSC PORTD, 0

GOTO … GOTO …

</div>
<div class="column">
;testbit2ofPORTD ;iffallherethenbitissetto1 ;iffallherethenbitissetto0

; if fall here, bit 2 of PORTD is set ; to 1, go to place to execute

; BCD operation

; if fall here, bit 2 of PORTD is set ; to 0, now we have to check bit 1 ; test bit 1 of PORTD ;iffallherethenbit1issetto1 ;iffallherethenbit0issetto1

; test bit 0 of PORTD

; test bit 0 of PORTD

</div>
</div>
</div>
<div class="page" title="Page 7">
<div class="layoutArea">
<div class="column">
T ASK_COMP:

BCF PORTD, 7

BCF PORTD, 6

BSF PORTD, 5

CALL SUBROUTINE_COMP GOTO MAIN_LOOP

T ASK_ADD:

BCF PORTD, 7

BSF PORTD, 6

BCF PORTD, 5

CALL SUBROUTINE_ADD GOTO MAIN_LOOP

…

Note: PORTD has a mixture of inputs and outputs. The first three bits are used as inputs to read in the operation to be executed. The three bits 5-7 are setup as outputs to show what function is being executed. Make sure that the TRISD register is setup properly in order to reflect this condition.

Once this part is completed, demonstrate using the three switches on PORT D bits 0 through 2 to select an arithmetic/logical operation, then select the inputs and check that the outputs are correct. Also, verify that the Z Flag LED does reflect the proper result.

</div>
</div>
</div>
