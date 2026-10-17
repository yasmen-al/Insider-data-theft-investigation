# 01 - Virtual Machine Setup

## Goal
Build a Windows 10 VM to act as the suspects (Caleb Bridger's) laptop. On the laptop, create fake company files and produce normal activities on the VM.

## Lab Environment
- Macbook Pro.
- VirutalBox 7.4.2, already installed.
- Windows 10 ISO, already installed on mac from Microsoft's software downloads.

## What I Did:
- At 17:31 on October 10th I created a VM called "laptop". I selected the Windows 10 ISO, chose Windows 10 pro and unticked unattended installation so that I can create a user account myself. I gave the VM 4096MB in RAM, 2CPUs and 40GB VHD virtual disk.
- I started the VM at 17:38 and installed Windows 10 Pro without a product key and I used custom install onto the empty disk.
- At 18:10 installation finished and I created an account named "Caleb Bridger" (made up name). I didn't add a Microsoft account and skipped all the optional setup options.
- At 18:17 I installed 7-zip from Microsoft Edge
- At 18:18 I shutdown the VM and took a snapshot called "clean install" which i can revert back to incase something goes wrong.
- I started the VM up again and created a "Sales" folder within the Documents folder. Inside the sales folder I created a text file called "customers.csv" and added 15 made up customer details (Customer ID, name, email, order value).
- I then created another file within the sales folder called "pricings.csv" with product names and prices.
- I then searched and browsed different sites in Edge and downloaded some images into pictures. Once I was finished I shut down the VM.


## Why?
Using a visual machine kept the incident isolated from my Mac. Additionally, I used fake personal information for the customers in accordance with UK GDPR. Adding normal browsers activity adds to the investigation so the files i made isn't the only evidence.


