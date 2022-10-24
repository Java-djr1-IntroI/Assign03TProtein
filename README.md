**Assign 03 - Protein Creation**

**Date assigned:**

**Program due:**

**Points:**

**This is an individual assignment.**

**Goals:**

1.  Use composition

2.  OOD using UML

3.  Implement and test each class one method at a time

4.  Code reusability

<img align="left" src="http://zeus.cs.pacificu.edu/ryand/apcs_a/images/Assignments/Protein/dna.png" alt="DNA">

DNA (deoxyribonucleic acid) is hereditary material found in nearly every
cell in a person's body and most other organisms. Most DNA is found in
the nucleus of the cell. The DNA information is coded from the four
chemical bases adenine (A), guanine (G), cytosine (C), and thymine (T).
DNA can replicate where each strand of DNA can serve as a pattern for
replication.

Genes contain the information that determine a person's traits which are
features or characteristics inherited by the person's parents. Each cell
in the human body contains around 20,000 genes and the number continues
to be revised down over time. In molecular terms, a gene is a region of
DNA that contains code used to make a polypeptide (a molecular chain).
Polypeptides link together to form proteins which perform a vast array
of functions within organisms.

![DNA to protein](http://zeus.cs.pacificu.edu/ryand/apcs_a/images/Assignments/Protein/dnatoprotein.png)

**The Problem**

<img align="left" src="http://zeus.cs.pacificu.edu/ryand/apcs_a/images/Assignments/Protein/premrnatomrna.png" alt="DNA">

During transcription, a pre-mRNA string contains segments called exons and
introns. For the purposes of protein translation, the introns are cut
out and the exons are sequentially put together. This process, cutting
and pasting, is known as splicing. The exons deriving from a gene are
collectively referred to as the "coding region." Now how cool is that???

Assume the introns and exons of a pre-mRNA string have been identified. The
problem of creating the coding region is simply deleting the introns and
concatenating the exons to form a new string ready for translation.
Therefore, given a DNA string and a collection
of substrings acting as introns, create the
protein string. For the purposes of this assignment, there will be one
DNA string and one intron in the file strings.txt.

**Example**

Consider the following sample dataset:

<pre>
ATGGTGCATCTGACTCCTGAGGAGAAGTAG
CTGACT
</pre>

The protein string produced is:

<pre>
MVHPEEK
</pre>

Question: How does ATG in the original DNA string become M in the
protein string?

Answer: Groups of 3 in the coding region are known as codons. Remember,
all T's will become U's in the pre-mRNA string; therefore, ATG becomes
AUG which is also known as the start codon of a pre-mRNA string and UAA,
UAG, and UGA are all stop codons. For the purposes of this assignment,
any stop codon can be used and exist anywhere in the pre-mRNA string; however,
codons will be well-formed in groups of three. A stop codon will not go
across two codons.

How to solve this problem?

1\) Load up an Amino Acid Table from a file created from this <a href="https://github.com/zhanxw/anno/blob/master/codon.txt">Amino Acid Table</a>. Name the file <b>aminoacids.txt</b> in your program and save the file in a folder called <b>data</b> which is at the same level as the folder src.

2\) Create a file <b>strings.txt</b> in the folder <b>data</b> that contains a DNA string and a collection (one
for this assignment) of substrings acting as introns.

3\) Convert the DNA string into a pre-mRNA string.

4\) Convert the pre-mRNA string into an mRNA string.

5\) Convert the mRNA string into a protein.

The main challenge of this problem is the design!!!!!

The output from your program is to look exactly like the following:

<pre>
Protein Creation
----------------

Coding Region
-------------
ATGGTGCATCTGACTCCTGAGGAGAAGTAG

pre-mRNA
AUGGUGCAUCUGACUCCUGAGGAGAAGUAG

mRNA
AUGGUGCAUCCUGAGGAGAAGUAG

Protein
-------
MVHPEEK
</pre>

**Error Checking**

1\) Make sure all bases of the coding region are legit. If not, print
out "Illegal Coding Region" and terminate the program.

2\) Make sure AUG is the start codon. If not, print out "Illegal Start
Codon" and terminate the program.

3\) Make sure a legit stop codon is encountered in the mRNA before the
end of the string is reached. If not, print out "No Stop Codon" and terminate
the program.

**Deliverables**

1. Using UMLet, you are to design the necessary classes that handle any logic relating to the Amino Acid Table. This logic will allow the lookup of any codon and the return of any information from the table if the codon is found. Again, make the Amino Acid table from: <a href="https://github.com/zhanxw/anno/blob/master/codon.txt">Amino Acid Table</a>. This deliverable must be approved before any coding begins. Email the .uxf anf .pdf files of your design to ryandj@pacificu.edu.

2. Implement your design from 1. where your driver tests your implementation in 1.

3. Design the remainder of the problem using UMLet. Add classes as needed. Think reusability and well defined classes. Again, this deliverable must be approved before continuing on with the implementation of the design. Email as in 1.

4. Implement your design from 3 where your driver solves the given problem and produces the desired output.

**To complete this assignment you must submit the following:**

1.  **An electronic Solution of your program on GitHub**

    a.  You are to click on the Assign03 Link to accept this
        assignment. Once accepted, code up a
        complete solution to the above assignment specification. Your
        complete solution is to be pushed to GitHub no later than the
        date and time specified above for your specific section. I will
        only grade your solution from the proper location on GitHub.

    b.  Pay attention to the example output above. Your program's output
        must look **exactly** like the example output! The spacing and
        newlines in your output must match exactly.

    c.  Make sure that your program compiles and runs correctly with no
        errors and no warnings. If you get any errors, double check that
        you typed everything correctly. Be aware that Java is
        case-sensitive.

2.  **An electronic copy of your program (punetidAssign03Protein.pdf) is to be emailed to ryandj@pacificu.edu**

