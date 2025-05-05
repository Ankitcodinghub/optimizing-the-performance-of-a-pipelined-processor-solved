# optimizing-the-performance-of-a-pipelined-processor-solved
**TO GET THIS SOLUTION VISIT:** [Optimizing the Performance of a Pipelined Processor Solved](https://www.ankitcodinghub.com/product/optimizing-the-performance-of-a-pipelined-processor-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;5428&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;Optimizing the Performance of a Pipelined Processor Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

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

<div class="kksr-stars-active" style="width: 138px;">
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
            5/5 - (1 vote)    </div>
    </div>
<strong>1 Introduction</strong>

In this lab, you will learn about the design and implementation of a pipelined Y86 processor, optimizing both

it and a benchmark program to maximize performance. You are allowed to make any semantics preserving

transformations to the benchmark program, or to make enhancements to the pipelined processor, or both.

When you have completed the lab, you will have a keen appreciation for the interactions between code and

hardware that affect the performance of your programs.

The lab is organized into three parts, each with its own handin. In Part A you will write some simple Y86

programs and become familiar with the Y86 tools. In Part B, you will extend the SEQ simulator with two

new instructions. These two parts will prepare you for Part C, the heart of the lab, where you will optimize

the Y86 benchmark program and the processor design.

<strong>2 Logistics</strong>

You will work on this lab alone.

Any clarifications and revisions to the assignment will be posted on the course Web page.

3 Handout Instructions

SITE-SPECIFIC: Insert a paragraph here that explains how students should download

the archlab-handout.tarfile.

1. Start by copying the file archlab-handout.tar to a (protected) directory in which you plan to

do your work.

2. Then give the command: tar xvf archlab-handout.tar. This will cause the following files

to be unpacked into the directory: README, Makefile, sim.tar, archlab.ps,archlab.pdf,

and simguide.pdf.

3. Next, give the command tar xvf sim.tar. This will create the directory sim, which contains

your personal copy of the Y86 tools. You will be doing all of your work inside this directory.

4. Finally, change to the sim directory and build the Y86 tools:

unix&gt; cd sim

unix&gt; make clean; make

4 Part A

You will be working in directory sim/misc in this part.

Your task is to write and simulate the following three Y86 programs. The required behavior of these programs

is defined by the example C functions in examples.c. Be sure to put your name and ID in a

comment at the beginning of each program. You can test your programs by first assembling them with the

program YAS and then running them with the instruction set simulator YIS.

In all of your Y86 functions, you should follow the IA32 conventions for the structure of the stack frame

and for register usage instructions, including saving and restoring any callee-save registers that you use.

sum.ys: Iteratively sum linked list elements

Write a Y86 program sum.ys that iteratively sums the elements of a linked list. Your program should

consist of some code that sets up the stack structure, invokes a function, and then halts. In this case, the

function should be Y86 code for a function (sum list) that is functionally equivalent to the C sum list

function in Figure 1. Test your program using the following three-element list:

# Sample linked list

.align 4

ele1:

.long 0x00a

.long ele2

ele2:

.long 0x0b0

.long ele3

ele3:

.long 0xc00

.long 0

2

1 /* linked list element */

2 typedef struct ELE {

3 int val;

4 struct ELE *next;

5 } *list_ptr;

6

7 /* sum_list – Sum the elements of a linked list */

8 int sum_list(list_ptr ls)

9 {

10 int val = 0;

11 while (ls) {

12 val += ls-&gt;val;

13 ls = ls-&gt;next;

14 }

15 return val;

16 }

17

18 /* rsum_list – Recursive version of sum_list */

19 int rsum_list(list_ptr ls)

20 {

21 if (!ls)

22 return 0;

23 else {

24 int val = ls-&gt;val;

25 int rest = rsum_list(ls-&gt;next);

26 return val + rest;

27 }

28 }

29

30 /* copy_block – Copy src to dest and return xor checksum of src */

31 int copy_block(int *src, int *dest, int len)

32 {

33 int result = 0;

34 while (len &gt; 0) {

35 int val = *src++;

36 *dest++ = val;

37 result ˆ= val;

38 len–;

39 }

40 return result;

41 }

Figure 1: C versions of the Y86 solution functions. See sim/misc/examples.c

3

rsum.ys: Recursively sum linked list elements

Write a Y86 program rsum.ys that recursively sums the elements of a linked list. This code should be

similar to the code in sum.ys, except that it should use a function rsum list that recursively sums a

list of numbers, as shown with the C function rsum list in Figure 1. Test your program using the same

three-element list you used for testing list.ys.

copy.ys: Copy a source block to a destination block

Write a program (copy.ys) that copies a block of words from one part of memory to another (nonoverlapping

area) area of memory, computing the checksum (Xor) of all the words copied.

Your program should consist of code that sets up a stack frame, invokes a function copy block, and

then halts. The function should be functionally equivalent to the C function copy block shown in Figure

Figure 1. Test your program using the following three-element source and destination blocks:

.align 4

# Source block

src:

.long 0x00a

.long 0x0b0

.long 0xc00

# Destination block

dest:

.long 0x111

.long 0x222

.long 0x333

5 Part B

You will be working in directory sim/seq in this part.

Your task in Part B is to extend the SEQ processor to support two new instructions: iaddl (described

in Homework problems 4.47 and 4.49)1. leave (described in Homework problems 4.48 and 4.50)2. To

add these instructions, you will modify the file seq-full.hcl, which implements the version of SEQ

described in the CS:APP2e textbook. In addition, it contains declarations of some constants that you will

need for your solution.

Your HCL file must begin with a header comment containing the following information:

• Your name and ID.

• A description of the computations required for the iaddl instruction. Use the descriptions of

irmovl and OPl in Figure 4.18 in the CS:APP2e text as a guide.

1In the international edition, iaddl is described in problems 4.48 and 4.50

2In the international edition, leave is described in problems 4.47 and 4.49

4

• A description of the computations required for the leave instruction. Use the description of popl

in Figure 4.20 in the CS:APP2e text as a guide.

Building and Testing Your Solution

Once you have finished modifying the seq-full.hcl file, then you will need to build a new instance of

the SEQ simulator (ssim) based on this HCL file, and then test it:

• Building a new simulator. You can use make to build a new SEQ simulator:

unix&gt; make VERSION=full

This builds a version of ssim that uses the control logic you specified in seq-full.hcl. To save

typing, you can assign VERSION=full in the Makefile.

• Testing your solution on a simple Y86 program. For your initial testing, we recommend running

simple programs such as asumi.yo (testing iaddl) and asuml.yo (testing leave) in TTY

mode, comparing the results against the ISA simulation:

unix&gt; ./ssim -t ../y86-code/asumi.yo

unix&gt; ./ssim -t ../y86-code/asuml.yo

If the ISA test fails, then you should debug your implementation by single stepping the simulator in

GUI mode:

unix&gt; ./ssim -g ../y86-code/asumi.yo

unix&gt; ./ssim -g ../y86-code/asuml.yo

• Retesting your solution using the benchmark programs. Once your simulator is able to correctly

execute small programs, then you can automatically test it on the Y86 benchmark programs in

../y86-code:

unix&gt; (cd ../y86-code; make testssim)

This will run ssim on the benchmark programs and check for correctness by comparing the resulting

processor state with the state from a high-level ISA simulation. Note that none of these programs test

the added instructions. You are simply making sure that your solution did not inject errors for the

original instructions. See file ../y86-code/README file for more details.

• Performing regression tests. Once you can execute the benchmark programs correctly, then you

should run the extensive set of regression tests in ../ptest. To test everything except iaddl

and leave:

unix&gt; (cd ../ptest; make SIM=../seq/ssim)

To test your implementation of iaddl:

5

1 /*

2 * ncopy – copy src to dst, returning number of positive ints

3 * contained in src array.

4 */

5 int ncopy(int *src, int *dst, int len)

6 {

7 int count = 0;

8 int val;

9

10 while (len &gt; 0) {

11 val = *src++;

12 *dst++ = val;

13 if (val &gt; 0)

14 count++;

15 len–;

16 }

17 return count;

18 }

Figure 2: C version of the ncopy function. See sim/pipe/ncopy.c.

unix&gt; (cd ../ptest; make SIM=../seq/ssim TFLAGS=-i)

To test your implementation of leave:

unix&gt; (cd ../ptest; make SIM=../seq/ssim TFLAGS=-l)

To test both iaddl and leave:

unix&gt; (cd ../ptest; make SIM=../seq/ssim TFLAGS=-il)

For more information on the SEQ simulator refer to the handout CS:APP2e Guide to Y86 Processor Simulators

(simguide.pdf).

6 Part C

You will be working in directory sim/pipe in this part.

The ncopy function in Figure 2 copies a len-element integer array src to a non-overlapping dst, returning

a count of the number of positive integers contained in src. Figure 3 shows the baseline Y86 version

of ncopy. The file pipe-full.hcl contains a copy of the HCL code for PIPE, along with a declaration

of the constant value IIADDL.

Your task in Part C is to modify ncopy.ys and pipe-full.hcl with the goal of making ncopy.ys

run as fast as possible.

You will be handing in two files: pipe-full.hcl and ncopy.ys. Each file should begin with a header

comment with the following information:

6

1 ##################################################################

2 # ncopy.ys – Copy a src block of len ints to dst.

3 # Return the number of positive ints (&gt;0) contained in src.

4 #

5 # Include your name and ID here.

6 #

7 # Describe how and why you modified the baseline code.

8 #

9 ##################################################################

10 # Do not modify this portion

11 # Function prologue.

12 ncopy: pushl %ebp # Save old frame pointer

13 rrmovl %esp,%ebp # Set up new frame pointer

14 pushl %esi # Save callee-save regs

15 pushl %ebx

16 pushl %edi

17 mrmovl 8(%ebp),%ebx # src

18 mrmovl 16(%ebp),%edx # len

19 mrmovl 12(%ebp),%ecx # dst

20

21 ##################################################################

22 # You can modify this portion

23 # Loop header

24 xorl %eax,%eax # count = 0;

25 andl %edx,%edx # len &lt;= 0?

26 jle Done # if so, goto Done:

27

28 Loop: mrmovl (%ebx), %esi # read val from src…

29 rmmovl %esi, (%ecx) # …and store it to dst

30 andl %esi, %esi # val &lt;= 0?

31 jle Npos # if so, goto Npos:

32 irmovl $1, %edi

33 addl %edi, %eax # count++

34 Npos: irmovl $1, %edi

35 subl %edi, %edx # len–

36 irmovl $4, %edi

37 addl %edi, %ebx # src++

38 addl %edi, %ecx # dst++

39 andl %edx,%edx # len &gt; 0?

40 jg Loop # if so, goto Loop:

41 ##################################################################

42 # Do not modify the following section of code

43 # Function epilogue.

44 Done:

45 popl %edi # Restore callee-save registers

46 popl %ebx

47 popl %esi

48 rrmovl %ebp, %esp

49 popl %ebp

50 ret

51 ##################################################################

52 # Keep the following label at the end of your function

53 End:

Figure 3: Baseline Y86 version of the ncopy function. See sim/pipe/ncopy.ys.

7

• Your name and ID.

• A high-level description of your code. In each case, describe how and why you modified your code.

Coding Rules

You are free to make any modifications you wish, with the following constraints:

• Your ncopy.ys function must work for arbitrary array sizes. You might be tempted to hardwire

your solution for 64-element arrays by simply coding 64 copy instructions, but this would be a bad

idea because we will be grading your solution based on its performance on arbitrary arrays.

• Your ncopy.ys function must run correctly with YIS. By correctly, we mean that it must correctly

copy the src block and return (in %eax) the correct number of positive integers.

• The assembled version of your ncopy file must not be more than 1000 bytes long. You can check the

length of any program with the ncopy function embedded using the provided script check-len.pl:

unix&gt; ./check-len.pl &lt; ncopy.yo

• Your pipe-full.hclimplementation must pass the regression tests in ../y86-codeand ../ptest

(without the -il flags that test iaddl and leave).

Other than that, you are free to implement the iaddl instruction if you think that will help. You may

make any semantics preserving transformations to the ncopy.ys function, such as reordering instructions,

replacing groups of instructions with single instructions, deleting some instructions, and adding other

instructions. You may find it useful to read about loop unrolling in Section 5.8 of CS:APP2e.

Building and Running Your Solution

In order to test your solution, you will need to build a driver program that calls your ncopy function. We

have provided you with the gen-driver.pl program that generates a driver program for arbitrary sized

input arrays. For example, typing

unix&gt; make drivers

will construct the following two useful driver programs:

• sdriver.yo: A small driver program that tests an ncopy function on small arrays with 4 elements.

If your solution is correct, then this program will halt with a value of 2 in register %eax after copying

the src array.

• ldriver.yo: A large driver program that tests an ncopy function on larger arrays with 63 elements.

If your solution is correct, then this program will halt with a value of 31 (0x1f) in register

%eax after copying the src array.

8

Each time you modify your ncopy.ys program, you can rebuild the driver programs by typing

unix&gt; make drivers

Each time you modify your pipe-full.hcl file, you can rebuild the simulator by typing

unix&gt; make psim VERSION=full

If you want to rebuild the simulator and the driver programs, type

unix&gt; make VERSION=full

To test your solution in GUI mode on a small 4-element array, type

unix&gt; ./psim -g sdriver.yo

To test your solution on a larger 63-element array, type

unix&gt; ./psim -g ldriver.yo

Once your simulator correctly runs your version of ncopy.ys on these two block lengths, you will want

to perform the following additional tests:

• Testing your driver files on the ISA simulator. Make sure that your ncopy.ys function works properly

with YIS:

unix&gt; make drivers

unix&gt; ../misc/yis sdriver.yo

• Testing your code on a range of block lengths with the ISA simulator. The Perl script correctness.pl

generates driver files with block lengths from 0 up to some limit (default 65), plus some larger sizes.

It simulates them (by default with YIS), and checks the results. It generates a report showing the status

for each block length:

unix&gt; ./correctness.pl

This script generates test programs where the result count varies randomly from one run to another,

and so it provides a more stringent test than the standard drivers.

If you get incorrect results for some length K, you can generate a driver file for that length that

includes checking code, and where the result varies randomly:

unix&gt; ./gen-driver.pl -f ncopy.ys -n K -rc &gt; driver.ys

unix&gt; make driver.yo

unix&gt; ../misc/yis driver.yo

The program will end with register %eax having the following value:

0xaaaa : All tests pass.

9

0xbbbb : Incorrect count

0xcccc : Function ncopy is more than 1000 bytes long.

0xdddd : Some of the source data was not copied to its destination.

0xeeee : Some word just before or just after the destination region was corrupted.

• Testing your pipeline simulator on the benchmark programs. Once your simulator is able to correctly

execute sdriver.ys and ldriver.ys, you should test it against the Y86 benchmark programs

in ../y86-code:

unix&gt; (cd ../y86-code; make testpsim)

This will run psim on the benchmark programs and compare results with YIS.

• Testing your pipeline simulator with extensive regression tests. Once you can execute the benchmark

programs correctly, then you should check it with the regression tests in ../ptest. For example, if

your solution implements the iaddl instruction, then

unix&gt; (cd ../ptest; make SIM=../pipe/psim TFLAGS=-i)

• Testing your code on a range of block lengths with the pipeline simulator. Finally, you can run the

same code tests on the pipeline simulator that you did earlier with the ISA simulator

unix&gt; ./correctness.pl -p

7 Evaluation

The lab is worth 190 points: 30 points for Part A, 60 points for Part B, and 100 points for Part C.

Part A

Part A is worth 30 points, 10 points for each Y86 solution program. Each solution program will be evaluated

for correctness, including proper handling of the stack and registers, as well as functional equivalence with

the example C functions in examples.c.

The programs sum.ys and rsum.ys will be considered correct if the graders do not spot any errors in

them, and their respective sum list and rsum list functions return the sum 0xcba in register %eax.

The program copy.ys will be considered correct if the graders do not spot any errors in them, and the

copy block function returns the sum 0xcba in register %eax, copies the three words 0x00a, 0x0b,

and 0xc to the 12 contiguous memory locations beginning at address dest, and does not corrupt other

memory locations.

10

Part B

This part of the lab is worth 60 points:

• 10 points for your description of the computations required for the iaddl instruction.

• 10 points for your description of the computations required for the leave instruction.

• 10 points for passing the benchmark regression tests in y86-code, to verify that your simulator still

correctly executes the benchmark suite.

• 15 points for passing the regression tests in ptest for iaddl.

• 15 points for passing the regression tests in ptest for leave.

Part C

This part of the Lab is worth 100 points: You will not receive any credit if either your code for ncopy.ys

or your modified simulator fails any of the tests described earlier.

• 20 points each for your descriptions in the headers of ncopy.ys and pipe-full.hcl and the

quality of these implementations.

• 60 points for performance. To receive credit here, your solution must be correct, as defined earlier.

That is, ncopy runs correctly with YIS, and pipe-full.hcl passes all tests in y86-code and

ptest.

We will express the performance of your function in units of cycles per element (CPE). That is, if the

simulated code requires C cycles to copy a block of N elements, then the CPE is C/N. The PIPE

simulator displays the total number of cycles required to complete the program. The baseline version

of the ncopy function running on the standard PIPE simulator with a large 63-element array requires

914 cycles to copy 63 elements, for a CPE of 914/63 = 14.51.

Since some cycles are used to set up the call to ncopy and to set up the loop within ncopy, you

will find that you will get different values of the CPE for different block lengths (generally the CPE

will drop as N increases). We will therefore evaluate the performance of your function by computing

the average of the CPEs for blocks ranging from 1 to 64 elements. You can use the Perl script

benchmark.pl in the pipe directory to run simulations of your ncopy.ys code over a range of

block lengths and compute the average CPE. Simply run the command

unix&gt; ./benchmark.pl

to see what happens. For example, the baseline version of the ncopy function has CPE values ranging

between 46.0 and 14.51, with an average of 16.44. Note that this Perl script does not check for the

correctness of the answer. Use the script correctness.pl for this:

unix&gt; ./benchmark.pl -p

11

You should be able to achieve an average CPE of less than 10.0. Our best version averages 9.27. If

your average CPE is c, then your score S for this portion of the lab will be:

S =

8&gt;&lt;&gt;:

0 , c &gt; 12.5

24.0 · (12.5 − c) , 10.0  c  12.5

60 , c &lt; 10.0

By default, benchmark.pl and correctness.pl compile and test ncopy.ys. Use the -f

argument to specify a different file name. The -h flag gives a complete list of the command line

arguments.

8 Handin Instructions

SITE-SPECIFIC: Insert a description that explains how students should hand in the three

parts of the lab. Here is the description we use at CMU.

• You will be handing in three sets of files:

– Part A: sum.ys, rsum.ys, and copy.ys.

– Part B: seq-full.hcl.

– Part C: ncopy.ys and pipe-full.hcl.

• Make sure you have included your name and ID in a comment at the top of each of your handin files.

• To handin your files for part X, go to your archlab-handout directory and type:

unix&gt; make handin-partX TEAM=teamname

where X is a, b, or c, and where teamname is your ID. For example, to handin Part A:

unix&gt; make handin-parta TEAM=teamname

• After the handin, if you discover a mistake and want to submit a revised copy, type

unix make handin-partX TEAM=teamname VERSION=2

Keep incrementing the version number with each submission.

• You can verify your handin by looking in

CLASSDIR/archlab/handin-partX

You have list and insert permissions in this directory, but no read or write permissions.

12

9 Hints

• By design, both sdriver.yo and ldriver.yo are small enough to debug with in GUI mode. We

find it easiest to debug in GUI mode, and suggest that you use it.

• If you running in GUI mode on a Unix server, make sure that you have initialized the DISPLAY

environment variable:

unix&gt; setenv DISPLAY myhost.edu:0

• With some X servers, the “Program Code” window begins life as a closed icon when you run psim

or ssim in GUI mode. Simply click on the icon to expand the window.

• With some Microsoft Windows-based X servers, the “Memory Contents” window will not automatically

resize itself. You’ll need to resize the window by hand.

• The psim and ssim simulators terminate with a segmentation fault if you ask them to execute a file

that is not a valid Y86 object file.

13
