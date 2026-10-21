# Contemporaneous Notes

## 01 - VM Setup
### 10/10/2026
17:30 - I opened VirtualBox which was already installed on my device.

17:31 - I clicked on new in VirtualBox and entered the name of the VM to be ‘laptop’.

17:33 - I selected the ISO image to be Windows 10 which I already had downloaded on my device from the Microsoft software download.

17:35 - Selected the OS Edition to Windows 10 pro and unticked proceed with unintended installation then clicked next.

17:36 - Allocated 4096MB to the base memory and gave it 2 CPUs.

17:37 - I pressed finish.

17:38 - I started the Virtual Machine.

17:40 - I followed the setup, chose ‘I don't have a product key’. I then selected Windows 10 pro and chose custom install onto the empty disk.

17:41 - I clicked next and waited for it to install.

18:10 - Created an Account called ‘Caleb Bridger’ without entering an email for a Microsoft account. 

18:11 - I skipped all the extras. 

18:17 - On Microsoft edge, I searched 7-Zip and downloaded it. 

18:18 - I Shutdown the device and took a snapshot by going to machine then take snapshot. I then named it ‘clean install’. 

18:20 - I started up the VM again.

18:22 - Inside the file explorer, I created a folder called ‘Sales’. 

18:23 - I Created a file in notepad called ‘Customerssss.csv’. Inside the notepad I added fake details for 15 Customerssss, noting down their CustomersssID, Name, email and order value. I Didn't use any personal date.

18:43 - Created another notepad within the ‘sales’ folder and named it ‘pricing.csv’ and added a list of product names and prices.

18:44 - searched random things on Microsoft edge and download some photos to store in the pictures folder.

20:00 - I Shut down the device.



## 02 - Incident Creation
### 11/10/2026
13:30 - I started up 'laptop' VM.

13:34 - I went to the file explorer and opened the sales folder, then opened ‘Customersss.csv’ and ‘pricing,csv’. I then closed the files.
  
13:40 - I selected both of these files and right clicked. I went to the 7-Zip option and clicked 'add to archive'.
  
13:42 - Changed the archive path to ‘HolidayPictures.7z’, then set a password and clicked ok. This file is now saved in the ‘sales’ folder.

14:31 - I searched OneDrive and tried to create an account to store the file ‘HolidayPictures.7z’. However, an error came up stating there is unusual activity on the device and that it couldn’t make an account.
  
14:57 on Microsoft edge I searched ‘how to permanently delete files from windows’. I then clicked and read one of the links.
  
 15:36 - I went to the sales folder. selected the files ‘Customersss.csv’ and ‘pricings.csv’ and deleted them.
 
15:37 - I made sure these files were properly deleted from the device by going to the bin and selecting the two files and deleting them.

15:38 - I went back to file explorer and deleted ‘HolidayPictures.7z’ but kept it in the rubbish bin.

15:40 - I shut down the "laptop" VM.



## 03 - Evidence Handling
### 13/10/2026
17:04 - I clicked on the ‘laptop’ VM settings and changed it from basic to expert and saved the changes. 

17:05 - I right clicked the ‘laptop’ vm and cloned it.

17:07 - I named the VM ‘Laptop clone’ and changed the Mac address policy to ‘generate new Mac addresses for all network adapters. I pressed finish and waited for the machine to be copied. 

17:17 - I opened terminal on mac to hash the clone file. 

18:59 - hash value came back: 9f8a1761ccf71f801bf7d97b01af0c52c3b160a4e939c675c54a586aef558d16

19:27 - created a master copy of the laptop clone. I then hashed it to make sure it matched the clone file which it did. However, when making the file i named it incorrectly it was supposed to be ‘case’ but it made ‘~case’.


### 14/10/2026
20:50 - I moved and renamed the the file using terminal on Mac.

20:53 - Stayed in terminal and gave the file a unique ID and hashed it. The 'evidence-working.vhd' and the 'laptop clone' now have 2 different hashes. ce738168f4bde150b8cfaa5083c93b3d455137a08f4c70393403c36ae676d23d


## 04 - Analysis
### 16/10/2026
00:13 - I exported contemporaneous notes into a pdf.

00:20 - I hashed the contemporaneous notes file in terminal using ‘shashum -a 256 and the file path. hash: 3c626edeb7e9e632dc6151575c3587caccb2241658db7d05f37bb1e8bdcf2ca1.

17:31 - I opened vitualbox and pressed on new and created a new VM called ‘analysis’. I allocated it the ISO file and gave it 4096 MB in RAM, 2 CPUs and 50GB disk and unticked unattended install.

17:33 - I started the ‘analysis’ VM.

17:34 - I set the language, time and keyboard to english (united kingdom and clicked install and pressed i don't have a product key.

17:35 - I selected Windows 10 Pro.

17:36 - Selected install windows only and pressed next. 

18:55 - I selected the region to United Kingdom.

18:59 - I set the account name to be ‘examiner’.

19:03 - I shut down the VM.

21:34 - Booted up the ‘analysis’ VM.

21:46 - I opened Microsoft edge.

21:47 - Searched autopsy.com in the search bar and clicked download.

23:11 - I shutdown the VM.

23:13 - I then created a snapshot called tools-installed.


### 17/10/2026
00:13 - I added the evidence-working.vhd by going into media and clicking add. I changed the type of the working copy to ‘immutable’.

01:09 - On the analysis VM i clicked settings then storage and added the working copy to the SATA and saved it.

14:40 - Started up the "analysis" VM.

14:42 - Opened autopsy.

14:45 - I created a new case and named it “laptop-analysis” and added the path to documents. I Pressed finish and waited for the case to be created.

14:51 - selected local disk ad data source type.

15:16 - I closed autopsy as i didn't run it in administrator.

15:17 - I right clicked on autopsy and selected “run as administrator” then created a new case named “laptop-analysis” and gave it the case number ‘001’ and name as examiner.

15:23 - Select the local disk and use the drop down box to select “drive-1”.

15:24 - I deselected all in the configure ingest and only selected recent activity, file type identification, extension mismatch detector and encryption detection.

15:26 - Pressed finish and waited for the case to load.

20:42 - Finished booting up.

20:49 - I closed autopsy.

20:50 - I shutdown the VM.

20:51 - Made a snapshot called “case001”. 


### 19/10/2026
17:34 - I started up the ‘analysis’ VM.

17:35 - I right-clicked autopsy and pressed ‘run as administrator’.

17:36 - I clicked on open recent case and located the case made and waited for it to load up.

17:52 - Searched for evidence.

18:18 - I extract all the files.

18:20 - Opened PowerShell.

18:53 - I created hash text file with the encrypted hashes of all the files in export folder.

19:00 - Made a table of my findings.

19:53 - Shutdown Analysis VM.

20:00 - Hashed the working-evidence.vhd in Terminal to see that it matched and it did.
