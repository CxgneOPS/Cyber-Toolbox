# IDA

## What It Is

IDA (Interactive Disassembler) is a reverse engineering tool used to analyze compiled binaries.

It allows investigators to inspect program structure, functions, and strings to understand how software behaves.

---

## What I Use It For

- Static analysis of binaries  
- Reviewing suspicious executables  
- Inspecting strings and imports  
- Understanding program behavior  
- Practicing malware analysis fundamentals  

IDA is one of the most valuable tools for static analysis in DFIR work.

---

## Basic Setup

1. Install IDA  
2. Open a binary file  
3. Allow auto-analysis to complete  
4. Begin reviewing functions and strings

---

## Core Concepts

IDA works around **disassembly and analysis views**.

Key concepts:

- Disassembly view  
- Functions and control flow  
- Strings analysis  
- Imports and exports  

Understanding navigation is critical.

---

## Common Workflow

### Basic Investigation Flow

1. Load binary  
2. Let auto-analysis run  
3. Check strings for clues  
4. Review imports and functions  
5. Identify suspicious behavior

---

## Troubleshooting

Analysis looks incomplete:
- Re-run auto-analysis  
- Verify correct file type detected  

Too complex to follow:
- Focus on strings and imports first  
- Break analysis into small sections

---

# Commands

---

## File Analysis

Open file:

File → Open

Re-run auto-analysis:

Options → General → Reanalyze Program

---

## Navigation

View functions:

View → Functions

View strings:

View → Open Subviews → Strings

View imports:

View → Open Subviews → Imports

---

## Search

Search for text:

Search → Text

Search for byte sequence:

Search → Sequence of Bytes

---

## Lessons Learned

- Strings often reveal useful clues  
- Imports hint at program behavior  
- Static analysis requires patience  
- Reverse engineering builds strong analysis skills
