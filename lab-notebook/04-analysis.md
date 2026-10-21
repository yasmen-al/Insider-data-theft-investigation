# 04 - Analysis

## Goal:
To recover evidence from the 'laptop' VM.

## Environment
- 'analysis' VM with Windows 10 Pro.
- Autopsy Version 4.23.1

## What I Did:
- Hashed the Contemporaneous notes from the 01 - VM set up to the 03 - evidence handling by converting it into a PDF and using Terminal to hash it.
- Created the VM named 'analysis' and booted up the VM. I downloaded Autopsy from autopsy.com and then I shutdown the VM and created a snapshot called 'tools-installed'.
- I added the 'evidence-working.vhd' under media and set its type to 'immutable' as the state can't be changed. I then added the 'evidence-working.vhd' as a SATA controller to the 'analysis' VM.
- I ran Autopsy in administrator so that it can detect hard drives. I created a new case called 'laptop-analysis' with case number '001'. I selected 'disk-1' as the local disk. I chose 4 ingests: Recent activity, file type identification, extension mismatch detector and encryption detection. I waited for the case to load then closed Autopsy and shutdown the VM. I created a new snapshot called 'case001'.
- I reopened the case and bookmarked all the evidence found. I extracted the files to the folder 'Export' and using PowerShell I hashed all the files in the folder and inputted it into Notepad named 'hashes'. I made a findings table with all the evidence found.
- Once I finished I shutdown the VM and hashed the 'working-evidence.vhd' to make sure it remained unchanged by comparing the hashes and they were both identical.

## Why?
- I downloaded Autopsy before adding 'evidence-working.vhd' because when installing software it may touch the disk which will lead to the hash being different.
- Only 4 ingests were selected as the scenario didn't need the others and it would take a long time to process the case.
- I took the snapshot 'case001' as autopsy took 5 hours to process the case and I didn't want to redo it if the case failed.
- I hashed the exports in the event that I do any further analysis. However, I didn't end up doing it.

## Problems, Decisions and Limitations
- First attempt at making the case failed as I didn't run as administrator.
- The case took 5 hours to process and the VM was being slow.
- It wasn't a blind analysis as I already knew what I was looking for.

# What I would do differently
- I only used one tool which was Autopsy. I would check the USB connection artefacts with another tool to verify the findings.
- I couldn't identify what was on the archive from the evidence. In a real case I would check other documents to see if a password is stored. If not i would run a password cracking tool.
