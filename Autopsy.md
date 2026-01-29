# Autopsy

## What It Is

Autopsy is a digital forensics platform used to analyze disk images and recover forensic artifacts.

It provides a graphical interface for investigating file systems, user activity, and system artifacts.

---

## What I Use It For

- Analyzing disk images  
- Recovering deleted files  
- Investigating user activity  
- Timeline analysis  
- Practicing DFIR workflows  

Autopsy is one of the most valuable tools for disk forensics in DFIR work.

---

## Basic Setup

1. Install Autopsy  
2. Create a new case  
3. Add a data source (disk image)  
4. Select ingest modules  
5. Review results

---

## Core Concepts

Autopsy works around **cases and data sources**.

Key concepts:

- Cases (investigation containers)  
- Data sources (disk images)  
- Ingest modules (analysis tools)  
- Artifact recovery  

Understanding ingest modules is critical.

---

## Common Workflow

### Basic Investigation Flow

1. Create a case  
2. Add disk image  
3. Run ingest modules  
4. Review artifacts and files  
5. Build timeline if needed

---

## Troubleshooting

No results appearing:
- Ensure ingest modules are enabled  
- Verify image loaded correctly  

Slow analysis:
- Limit ingest modules  
- Use smaller datasets for labs

---

# Commands

---

## Case Creation

Create new case:

Use GUI → New Case

---

## Add Data Source

Add disk image:

Use GUI → Add Data Source

---

## Ingest Modules

Enable modules:


Select during data source setup

---

## Timeline Analysis

Open timeline:

Tools → Timeline

---

## Exporting Data

Export files:

Right-click file → Extract

Generate report:

Tools → Generate Report

---

## Lessons Learned

- Disk images hold valuable evidence  
- Timeline analysis reveals patterns  
- Deleted files can still be recovered  
- Disk forensics builds strong DFIR skills
