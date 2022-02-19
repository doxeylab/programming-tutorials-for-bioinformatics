# Tutorial 2 - Python
Python is a popular programming language used for many purposes ranging from building websites and software development to data analysis and automating tasks. Many people like Python over other programming languages becasue its syntax (language structure) is similar to the English language - after all, it was designed for readability!

## General Information
* If you're interested in learning more Python, consider enrolling in [CS 116 Introduction to Computer Science 2](https://cs.uwaterloo.ca/current/courses/course_descriptions/cDescr/CS116) at the University of Waterloo.
* Python files (modules) are stored using ".py" (e.g., HelloWorld.py).
* Indentation is used to group code blocks. This refers to the spaces at the beginning of a code line. Standard indents are 4 spaces.

## Getting Started

#### What are Code Editors?
A code editor, or an Integrated Development Environment (IDE) is a computer software that allows the user to write code and debug. 
Popular free code editing software includes: Sublime Text, Visual Studio Code, IDLE, Spyder, Jupyter, Wing, or replit.com

### Downloading Python and Code Editor
Download and install Python [here](https://www.python.org/).
We recommend you to install Python 3 and up.

For the ease of this tutorial, we will be using a code editor called IDLE. IDLE is bundled with your Python installation.
1. Open the IDLE Application
2. Go to `File > New Window` to open the programming editor
3. You can save your file on your computer by navigating to `File > Save` 

### Your First Program
When we <i>print</i> text in a program, we're not literally talking about printing a piece of paper from a printer. <i>Print</i> means our computer is outputting some text.

Let's print our first message:
```python
print("Hello world")
```
This line is called a <i>statement</i>.

`print` is the name of a <i>function</i>. <i>Functions</i> are codes that are used to accomplish a specific task. They can be blocks of code, or individual statements like `print`.

The text within the round parentheses are called <i>arguments</i>. Depending on the function, there can be one or more arguments. These tell our functions what exactly to do. In this case, our argument is telling our function `print` to output the text `Hello world`.

## Programming Basics

### Comments
<i>Comments</i> are short notes in code that help explain how your program works, or in-code documentation.
In Python, these start with a hash character '#' and continue until the end of the line. 
```python
#This is a comment!
```
They can be placed at the end of a function.
```python
print("Hello world") #This is a comment
```
Span more than one line
```python
#This
#is a
#comment
```
And can prevent Python from executing your function.
```python
print("Hello world")
#print("Goodbye world")
```
Comments are useful when you are showing your code to somebody else, but more importantly, they're extremely useful to reminding <b>you</b> how your code works. These can help you understand your own code. Let's write a comment for our first program:
```python
# Print a greeting; say hello to the world.
print("Hello world")
```

### Variables
<i>Variables</i> store data to be referenced and can be changed using a computer program.

They can be:
* <i>strings</i> (text), defined using double quotations
* numbers (integer, float (number with decimals)

They're also case-sensitive. So, ACGT, acgt, acGT, AcGT are all separate variables.

```python
courseName = "Introduction to Computational Biology"
myInteger = 9876
myFloat = 54.321

print(courseName)
print(myInteger)
print(myFloat)
```
The variable courseName is assigned to the string "Introduction to Computational Biology". Now, we can refer to the variable instead of the string itself, and use it in a print statement. Since the quotes are already part of the string in courseName, we don't need to include them because they are part of courseName.

We can also reassign the variable as many times as we need to.
```python
courseName = "Introduction to Computational Biology"
print(courseName)
#Update Course Name
courseName = "Methods in Bioinformatics"
print(courseName)

luckyNumber = 7
print(luckyNumber)
#Re-assign number
unluckyNumber = 13
print(unluckyNumber)
```

It might seem like there's a relationship between our variable and its content, but we can name our variable anything we want. 
```python
courseName = "Methods in Bioinfornatics"
print(courseName)
#Change variable name
ilovemarshmellows = "Methods in Bioinformatics"
print(ilovemarshmellows)

luckyNumber = 7
print(luckyNumber)
# Change variable name
unluckyNumber = 7
print(unluckyNumber)
```

### Lists
Lists are used to store multiple items (strings, numbers, etc.) in a single variable. Lists are one of Python's four built-in data types. The others are Tuple, Set and Dictionary, but we won't dive too deep into those in this tutorial. 

Square brackets define lists.
```python
# Example of an empty list
emptyBasket = []
print(emptyBasket)

# Example of a list with items
myDNA = ["A", "C", "T", "G"]
print(myDNA)
```

We can access different items in the list by specifying its `index` using square brackets. <b>The first index of a list in Python is 0</b>,not 1. For instance, in a list of 4 items, we have the indices 0, 1, 2, 3. You can also use negative indices to access items with respect to the right-end of the list.
```python
myDNA = ["A", "C", "T", "G"]

# Access adenine from myDNA
print(myDNA[0])

# Assign adenine its own variable
adenine = myDNA[0]
print(adenine)
```

### Operations
Operations are special symbols that carry out arithmetic or logical computation, like adding, subtracting, dividing, multipling, comparing numbers and more.
```python
myInteger = 9876
myFloat = 54.321

# Add myInteger and myFloat
mySum = myInteger + myFoloat
print(mySum)
```

Other operations are included below:
```python
x = 42
y = 241

# Addition
z = x + y
print(z)

# Subtraction
z = x - y
print(z)

# Multiplication
z = x * y
print(z)

# Division
z = x / y
print(z)

# Exponents
z = x ** y
print(z)
```

We can also use operations on strings.
```python
# Concatenate Sentence
courseCode = "BIOL 266"
courseName = "Introduction to Computational Biology"

course = "Welcome to " + courseCode + " " + courseName
# notice we included two quotation marks with an empty space - this is a string!
print(course)

# Repeat Strings
minion = banana * 100
print(minion)

# Slice a string (substrings)
print(course[0:6])                      # should output "Welcome"

# Compute the length of the string
len(course)
print(len(course))

# Identify the index of a character
i = course.index("B")                   # should return 11, since the first occurence of 'B' is at index 11

# Counting the number of 'B' characters in the string
i = course.index("B")
print(i)                                # should return 2
```

### Conditional Statements (If/Else)
<i>If statements</i> or <i>conditions</i> are commonly used to evaluate if conditions are true or false given a set of rules using `if`.

Logical conditions include:
* equals: `a == b`
* not equals: `a != b`
* greater than: `a > b`
* less than: `a < b`
* greater than or equal to: `a >= b`
* less than or equal to: `a <= b`
* `and`
* `or`
* `not`

```python
DNAsequence1 = "ATAGCGCATCGATCAGCTATGCGA"
DNAsequence2 = "ATGATCGACCGCTATAGCTAGCTA"

if DNAsequence1 == DNAsequence2:
    print("The two DNA sequences are identical")
else:
    print("The DNA sequences are different")
```

Python relies on indentation (standard indentation is 4 spaces) at the beginning of a line to specify a code block.
The `else` function directs the code to another result if the preceding conditions aren't met.

We can also put an if statement in an if statement. This is refered to as a <i>nested</i> if statement.
```python
DNAsequence1 = "ATAGCGCATCGATCAGCTATGCGA"
DNAsequence2 = "ATGATCGACCGCTATAGCTAGCTA"

if DNAsequence1 == DNAsequence2:
    print("The two DNA sequences are identical")
else:
    print("The DNA sequences are different")
    if len(DNAsequence1) == len(DNAsequence2):
        print("but they have the same length")
    else:
        print("and they are different in length")
```
In this example, we first compare if DNAsequence1 is equal to DNAsequence2. If they are identical, we print a sentence stating that they are identical. If they're not identical, we move to the `else` portion of the statement and print a sentence stating that the sequences are different. We also move to the next `if` block which compares the string lengths of our DNA seuqeqnces. If they are identical, we print a sentence stating that they have the same length. If they are not identical lengths, we print a statement stating that our sequences are different in length.

The `in` operator is also useful to see if a variable mathes an element of a list.
```python
DNAsequence1 = "ATAGCGCATCGATCAGCTATGCGA"

if DNAsequence1[1] in ["A","C","G","T"]:
    print("The first character is a nucleotide")
else:
    print("The first character is not a nucleotide")
```

### For and while Loops
To repeat code, you can use `for` and `while` loops
```python
nucleotides = ["A", "C", "G", "T"]
for nucleotide in nucleotides:
    print(nucleotide)

#or a numeric example

for i in range(1,10):
    print(i)
```

## Functions
We've mentioned functions earlier in this tutorial - they are blocks of code which run only when they are called. They take <i>arguments/parameters</i> and can return data or do some action as  result.

`def` is used to define a Python function.
```python
def my_first_function():
    print("Hello world! This is my first function.")
```

To call a function, use the function name followed by parenthesis.
```python
def my_first_function():
    print("Hello world! This is my first function.")
    
my_first_function()
```

### Arguments/Parameters
An argument or parameter (interchangeable) is information that is given to the function. There can be as many arguments as you want in a function. However, if you function expects n number of arguments, you must call the function with exactly n arguments.
```python
def add_nucleotides(nucleotide1, nucleotide2):
    print(nucleotide1 + nucleotide2)
    
add_nucleotides("TATATATA", "ATG")        # should print "TATATATAATG"
```

## Exercise
### A Simple Gene-Finder

#### The phi X Phage: 
Phi x 174 is a bacteriophage and is famous for being the first DNA-based genome to be sequenced (by Sanger and colleagues in 1974).
#### The phi X Genome:
Pasted below is the genome of phi X (the fasta file from the NCBI database). Amazingly small isn't it? The genome is about ~5 kb and only encodes 11 proteins, 8 of which are virulence related.
```
>gi|9626372|ref|NC_001422.1| Enterobacteria phage phiX174, complete genome
GAGTTTTATCGCTTCCATGACGCAGAAGTTAACACTTTCGGATATTTCTGATGAGTCGAAAAATTATCTTGATAAAGCAGGAATTACTACTGCTTGTTTACGAATTAAATCGAAGTGGACTGCTGGCGGAAAATGAGAAAATTCGACCTATCCTTGCGCAGCTCGAGAAGCTCTTACTTTGCGACCTTTCGCCATCAACTAACGATTCTGTCAAAAACTGACGCGTTGGATGAGGAGAAGTGGCTTAATATGCTTGGCACGTTCGTCAAGGACTGGTTTAGATATGAGTCACATTTTGTTCATGGTAGAGATTCTCTTGTTGACATTTTAAAAGAGCGTGGATTACTATCTGAGTCCGATGCTGTTCAACCACTAATAGGTAAGAAATCATGAGTCAAGTTACTGAACAATCCGTACGTTTCCAGACCGCTTTGGCCTCTATTAAGCTCATTCAGGCTTCTGCCGTTTTGGATTTAACCGAAGATGATTTCGATTTTCTGACGAGTAACAAAGTTTGGATTGCTACTGACCGCTCTCGTGCTCGTCGCTGCGTTGAGGCTTGCGTTTATGGTACGCTGGACTTTGTGGGATACCCTCGCTTTCCTGCTCCTGTTGAGTTTATTGCTGCCGTCATTGCTTATTATGTTCATCCCGTCAACATTCAAACGGCCTGTCTCATCATGGAAGGCGCTGAATTTACGGAAAACATTATTAATGGCGTCGAGCGTCCGGTTAAAGCCGCTGAATTGTTCGCGTTTACCTTGCGTGTACGCGCAGGAAACACTGACGTTCTTACTGACGCAGAAGAAAACGTGCGTCAAAAATTACGTGCGGAAGGAGTGATGTAATGTCTAAAGGTAAAAAACGTTCTGGCGCTCGCCCTGGTCGTCCGCAGCCGTTGCGAGGTACTAAAGGCAAGCGTAAAGGCGCTCGTCTTTGGTATGTAGGTGGTCAACAATTTTAATTGCAGGGGCTTCGGCCCCTTACTTGAGGATAAATTATGTCTAATATTCAAACTGGCGCCGAGCGTATGCCGCATGACCTTTCCCATCTTGGCTTCCTTGCTGGTCAGATTGGTCGTCTTATTACCATTTCAACTACTCCGGTTATCGCTGGCGACTCCTTCGAGATGGACGCCGTTGGCGCTCTCCGTCTTTCTCCATTGCGTCGTGGCCTTGCTATTGACTCTACTGTAGACATTTTTACTTTTTATGTCCCTCATCGTCACGTTTATGGTGAACAGTGGATTAAGTTCATGAAGGATGGTGTTAATGCCACTCCTCTCCCGACTGTTAACACTACTGGTTATATTGACCATGCCGCTTTTCTTGGCACGATTAACCCTGATACCAATAAAATCCCTAAGCATTTGTTTCAGGGTTATTTGAATATCTATAACAACTATTTTAAAGCGCCGTGGATGCCTGACCGTACCGAGGCTAACCCTAATGAGCTTAATCAAGATGATGCTCGTTATGGTTTCCGTTGCTGCCATCTCAAAAACATTTGGACTGCTCCGCTTCCTCCTGAGACTGAGCTTTCTCGCCAAATGACGACTTCTACCACATCTATTGACATTATGGGTCTGCAAGCTGCTTATGCTAATTTGCATACTGACCAAGAACGTGATTACTTCATGCAGCGTTACCATGATGTTATTTCTTCATTTGGAGGTAAAACCTCTTATGACGCTGACAACCGTCCTTTACTTGTCATGCGCTCTAATCTCTGGGCATCTGGCTATGATGTTGATGGAACTGACCAAACGTCGTTAGGCCAGTTTTCTGGTCGTGTTCAACAGACCTATAAACATTCTGTGCCGCGTTTCTTTGTTCCTGAGCATGGCACTATGTTTACTCTTGCGCTTGTTCGTTTTCCGCCTACTGCGACTAAAGAGATTCAGTACCTTAACGCTAAAGGTGCTTTGACTTATACCGATATTGCTGGCGACCCTGTTTTGTATGGCAACTTGCCGCCGCGTGAAATTTCTATGAAGGATGTTTTCCGTTCTGGTGATTCGTCTAAGAAGTTTAAGATTGCTGAGGGTCAGTGGTATCGTTATGCGCCTTCGTATGTTTCTCCTGCTTATCACCTTCTTGAAGGCTTCCCATTCATTCAGGAACCGCCTTCTGGTGATTTGCAAGAACGCGTACTTATTCGCCACCATGATTATGACCAGTGTTTCCAGTCCGTTCAGTTGTTGCAGTGGAATAGTCAGGTTAAATTTAATGTGACCGTTTATCGCAATCTGCCGACCACTCGCGATTCAATCATGACTTCGTGATAAAAGATTGAGTGTGAGGTTATAACGCCGAAGCGGTAAAAATTTTAATTTTTGCCGCTGAGGGGTTGACCAAGCGAAGCGCGGTAGGTTTTCTGCTTAGGAGTTTAATCATGTTTCAGACTTTTATTTCTCGCCATAATTCAAACTTTTTTTCTGATAAGCTGGTTCTCACTTCTGTTACTCCAGCTTCTTCGGCACCTGTTTTACAGACACCTAAAGCTACATCGTCAACGTTATATTTTGATAGTTTGACGGTTAATGCTGGTAATGGTGGTTTTCTTCATTGCATTCAGATGGATACATCTGTCAACGCCGCTAATCAGGTTGTTTCTGTTGGTGCTGATATTGCTTTTGATGCCGACCCTAAATTTTTTGCCTGTTTGGTTCGCTTTGAGTCTTCTTCGGTTCCGACTACCCTCCCGACTGCCTATGATGTTTATCCTTTGAATGGTCGCCATGATGGTGGTTATTATACCGTCAAGGACTGTGTGACTATTGACGTCCTTCCCCGTACGCCGGGCAATAACGTTTATGTTGGTTTCATGGTTTGGTCTAACTTTACCGCTACTAAATGCCGCGGATTGGTTTCGCTGAATCAGGTTATTAAAGAGATTATTTGTCTCCAGCCACTTAAGTGAGGTGATTTATGTTTGGTGCTATTGCTGGCGGTATTGCTTCTGCTCTTGCTGGTGGCGCCATGTCTAAATTGTTTGGAGGCGGTCAAAAAGCCGCCTCCGGTGGCATTCAAGGTGATGTGCTTGCTACCGATAACAATACTGTAGGCATGGGTGATGCTGGTATTAAATCTGCCATTCAAGGCTCTAATGTTCCTAACCCTGATGAGGCCGCCCCTAGTTTTGTTTCTGGTGCTATGGCTAAAGCTGGTAAAGGACTTCTTGAAGGTACGTTGCAGGCTGGCACTTCTGCCGTTTCTGATAAGTTGCTTGATTTGGTTGGACTTGGTGGCAAGTCTGCCGCTGATAAAGGAAAGGATACTCGTGATTATCTTGCTGCTGCATTTCCTGAGCTTAATGCTTGGGAGCGTGCTGGTGCTGATGCTTCCTCTGCTGGTATGGTTGACGCCGGATTTGAGAATCAAAAAGAGCTTACTAAAATGCAACTGGACAATCAGAAAGAGATTGCCGAGATGCAAAATGAGACTCAAAAAGAGATTGCTGGCATTCAGTCGGCGACTTCACGCCAGAATACGAAAGACCAGGTATATGCACAAAATGAGATGCTTGCTTATCAACAGAAGGAGTCTACTGCTCGCGTTGCGTCTATTATGGAAAACACCAATCTTTCCAAGCAACAGCAGGTTTCCGAGATTATGCGCCAAATGCTTACTCAAGCTCAAACGGCTGGTCAGTATTTTACCAATGACCAAATCAAAGAAATGACTCGCAAGGTTAGTGCTGAGGTTGACTTAGTTCATCAGCAAACGCAGAATCAGCGGTATGGCTCTTCTCATATTGGCGCTACTGCAAAGGATATTTCTAATGTCGTCACTGATGCTGCTTCTGGTGTGGTTGATATTTTTCATGGTATTGATAAAGCTGTTGCCGATACTTGGAACAATTTCTGGAAAGACGGTAAAGCTGATGGTATTGGCTCTAATTTGTCTAGGAAATAACCGTCAGGATTGACACCCTCCCAATTGTATGTTTTCATGCCTCCAAATCTTGGAGGCTTTTTTATGGTTCGTTCTTATTACCCTTCTGAATGTCACGCTGATTATTTTGACTTTGAGCGTATCGAGGCTCTTAAACCTGCTATTGAGGCTTGTGGCATTTCTACTCTTTCTCAATCCCCAATGCTTGGCTTCCATAAGCAGATGGATAACCGCATCAAGCTCTTGGAAGAGATTCTGTCTTTTCGTATGCAGGGCGTTGAGTTCGATAATGGTGATATGTATGTTGACGGCCATAAGGCTGCTTCTGACGTTCGTGATGAGTTTGTATCTGTTACTGAGAAGTTAATGGATGAATTGGCACAATGCTACAATGTGCTCCCCCAACTTGATATTAATAACACTATAGACCACCGCCCCGAAGGGGACGAAAAATGGTTTTTAGAGAACGAGAAGACGGTTACGCAGTTTTGCCGCAAGCTGGCTGCTGAACGCCCTCTTAAGGATATTCGCGATGAGTATAATTACCCCAAAAAGAAAGGTATTAAGGATGAGTGTTCAAGATTGCTGGAGGCCTCCACTATGAAATCGCGTAGAGGCTTTGCTATTCAGCGTTTGATGAATGCAATGCGACAGGCTCATGCTGATGGTTGGTTTATCGTTTTTGACACTCTCACGTTGGCTGACGACCGATTAGAGGCGTTTTATGATAATCCCAATGCTTTGCGTGACTATTTTCGTGATATTGGTCGTATGGTTCTTGCTGCCGAGGGTCGCAAGGCTAATGATTCACACGCCGACTGCTATCAGTATTTTTGTGTGCCTGAGTATGGTACAGCTAATGGCCGTCTTCATTTCCATGCGGTGCACTTTATGCGGACACTTCCTACAGGTAGCGTTGACCCTAATTTTGGTCGTCGGGTACGCAATCGCCGCCAGTTAAATAGCTTGCAAAATACGTGGCCTTATGGTTACAGTATGCCCATCGCAGTTCGCTACACGCAGGACGCTTTTTCACGTTCTGGTTGGTTGTGGCCTGTTGATGCTAAAGGTGAGCCGCTTAAAGCTACCAGTTATATGGCTGTTGGTTTCTATGTGGCTAAATACGTTAACAAAAAGTCAGATATGGACCTTGCTGCTAAAGGTCTAGGAGCTAAAGAATGGAACAACTCACTAAAAACCAAGCTGTCGCTACTTCCCAAGAAGCTGTTCAGAATCAGAATGAGCCGCAACTTCGGGATGAAAATGCTCACAATGACAAATCTGTCCACGGAGTGCTTAATCCAACTTACCAAGCTGGGTTACGACGCGACGCCGTTCAACCAGATATTGAAGCAGAACGCAAAAAGAGAGATGAGATTGAGGCTGGGAAAAGTTACTGTAGCCGACGTTTTGGCGGCGCAACCTGTGACGACAAATCTGCTCAAATTTATGCGCGCTTCGATAAAAATGATTGGCGTATCCAACCTGCA
```

In this exercise, you will write a simple open-reading frame (ORF) finder. To simplify things, we will examine one frame (out of six) AND disregard start codons. Therefore, we will define ORFs as all long sequences in between potential stop codons.

#### 1. Translate genomics DNA into proteins (open reading frames)
Given what you have learned above, store the entire genome sequence as a string. In the example below, I'm calling the string variable <b>sequence</b>.
Then, using a sliding window of 3 nucleotides at a time (codons), output the sequence again but mark which codons are STOP codons (TAG, TAA, or TGA).

<details>
    <summary>
    Show Code
    </summary>
    
    position = 0  # need to define it first
    while position < len(sequence) - 2:
        codon = sequence[position:(position+3)]
        if (codon in ("TAG","TAA","TGA")):
            print(codon + "-----> STOP")
    else:
        print(codon)
    position = position + 3
                                  
</details>


#### 2. Recording the lengths of ORFs
Real proteins can be identified by looking for <b>LONG OPEN READING FRAMES</b>, so let's modify our program to indicate ORFs over 100 nucleotides in length.

<details>
    <summary>
    Show Code
    </summary>
    
    position = 0  # need to define it first
    ORFlength = 0
    while position < len(sequence) - 2:
        codon = sequence[position:(position+3)]
        if (codon in ("TAG","TAA","TGA")):
            print(codon + "-----> STOP")
            if (ORFlength > 100):
                print("--------------------LONG ORF")
        ORFlength = 0
    else:
        print(codon)
        ORFlength = ORFlength + 3
    position = position + 3
    
</details>
    
#### 3. Printing only the long open reading frames
Now, let's no longer print out all codons. Modify your code to only print out the ORFs > 100 nt in length.

<details>
    <summary>
    Show Code
    </summary>
    
    
    position = 0  # need to define it first
    ORFlength = 0
    ORFsequence = ""
    while position < len(sequence) - 2:
        codon = sequence[position:(position+3)]
        if (codon in ("TAG","TAA","TGA")):
            #print(codon + "-----> STOP")
            if (ORFlength > 100):
                print("--------------------LONG ORF")
                print(ORFsequence)
            ORFsequence = ""
            ORFlength = 0
    else:
        ORFsequence = ORFsequence + codon
        ORFlength = ORFlength + 3
    position = position + 3
    
</details>
    
#### 4. Check Results using BLAST
Copy and paste your predicted open reading frames and BLAST them against the NCBI protein database. Is your program identifying valid proteins?

[BLASTX](http://blast.ncbi.nlm.nih.gov/Blast.cgi?PROGRAM=blastx&PAGE_TYPE=BlastSearch&LINK_LOC=blasthome)

#### 5. On your own
Not much is needed to expand this tool to become a more sophisticated ORF-finder (& gene-finder)!
* Incorporate start codons (ATG)
* Examine all 6 reading frames
* Include homology information! Using [BioPython](https://biopython.org/docs/dev/api/Bio.Blast.Applications.html), you could BLAST each ORF against a protein database to check for homology.


# Resources
* [W3Schools Python Tutorial](https://www.w3schools.com)
* [LearnPython.org](https://www.learnpython.org/)
* [Python for Biologists](http://userpages.fu-berlin.de/digga/p4b.pdf)
* [PythonTutor](https://pythontutor.com/)
