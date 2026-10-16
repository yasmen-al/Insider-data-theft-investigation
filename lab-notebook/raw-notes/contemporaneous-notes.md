# Contemporaneous Notes

## 01 - VM Setup
### 10/10/2026
17:30 - I Opened VirtualBox which was already installed on my device.

17:31 - I Clicked on new in VirtualBox and entered the name of the VM to be ‘laptop’.

17:33 - I selected the ISO image to be Windows10 which I already had downloaded on my device from the Microsoft software download.

17:35 - Selected the OS Edition to Windows 10 pro and unticked proceed with unintended installation then clicked next.

17:36 - Allocated 4096MB to the base memory and gave it 2 CPUs.

17:37 - I pressed finish.

17:38 - I started the Virtual Machine.

17:40 - I followed the setup, chose ‘I don't have a product key’. I then selected Windows 10 pro and chose custom install onto the empty disk.

17:41 - I clicked next and waited for it to install.

18:10 - Created an Account called ‘Caleb Bridger’ without entering an email for a Microsoft account. 

18:11 - I skipped all the extras. 

18:17 - On Microsoft edge, I searched 7-zip and installed it. 

18:18 - I Shutdown the device and took a snapshot by going to machine then take snapshot. I then named it ‘clean install’. 

18:20 - I started up the VM again.

18:22 - Inside the file explorer, I created a folder called ‘Sales’. 

18:23 - I Created a file in notepad called ‘customers.csv’. Inside the notepad I added fake details for 15 customers, noting down their customerID, Name, email and order value. I Didn't use any personal date.

18:43 - Created another notepad within the ‘sales’ folder and named it ‘pricing.csv’ and added a list of product names and prices.

18:44 - searched random things on Microsoft edge and download some photos to store in the pictures folder.

20:00 - I Shut down the device.



## 02 - Incident Creation
### 11/10/2026
14:34 - I started up 'laptop'.

- I went to the file explorer and opened the sales folder, then opened ‘customer,csv’ and ‘pricing,csv’. I then closed the files.
  
- selected both of these files and right clicked. I went to the 7-zip option and clicked 'add to archive'.
  
- Changed the archive path to ‘holidaypictures.7Z’, then set a password and clicked ok. This file is now saved in the ‘sales’ folder.
  
- on Microsoft edge I searched ‘how to permanently delete files from windows’. I then clicked and read one of the links.
  
- I searched onedrive and tried to create an account to store the file ‘holidaypictures’. However, an error came up stating there is unusual activity on the device and that it couldn’t make an account.
  
 15:36 - I went to the sales folder. selected the files ‘customer.csv’ and ‘pricings.csv’ and deleted them.
 
15:37 - I made sure these files were properly deleted from the device by going to the bin and selecting the two files and deleting them.

15:38 - I went back to file explorer and deleted ‘holidaypictures’ but kept it in the rubbish bin.

15:40 - shut down the device.



## 03 - Evidence Handling
### 13/10/2026
17:04 - I clicked on the ‘laptop’ VM settings and changed it from basic to expert and saved the changes. 

17:05 - I right clicked the ‘laptop’ vm and cloned it.

17:07 - I named the VM ‘Laptop clone’ and changed the Mac address policy to ‘generate new Mac addresses for all network adapters. I pressed finish and waited for the machine to be copied. 

17:17 - I opened terminal on mac to hash the clone file. 

18:59 - hash value came back: 9f8a1761ccf71f801bf7d97b01af0c52c3b160a4e939c675c54a586aef558d16

19:27 - created a master copy of the laptop clone. I then hashed it to make sure it matched the clone file which it did. However, when making the file i named it incorrectly it was supposed to be ‘case’ but it made ‘~case’.


### 14/10/2026
20:50 - i moved and renamed the the file using terminal on Mac.

20:53 - Stayed in terminal and gave the file a unique ID and hashed it. The 'evidence-working.vhd' and the 'laptop clone' now have 2 different hashes. ce738168f4bde150b8cfaa5083c93b3d455137a08f4c70393403c36ae676d23d
