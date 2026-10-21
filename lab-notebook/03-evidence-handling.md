# 03 - Evidence Handling and Acquisition 

## Goal
Turn Caleb Bridger's laptop virtual machine into a single verified disk image, then make a working copy to analyse so that the original virtual machine is never touched.

## What I did
1. I made sure the 'laptop' VM was powered off.
2. Created a clone of the 'laptop' VM on VirtualBox 7.4.2 by right clicking the VM and pressing clone. I chose this instead of deleting the snapshot on the 'laptop' VM as deleting changes the original disk and modifies it. Cloning the VM leaves the original untouched.
3. I hashed the clone VM with shasum -a 256 and the path to the VM and it outputted: 9f8a1761ccf71f801bf7d97b01af0c52c3b160a4e939c675c54a586aef558d16 at 18:59. The clone VM is the master and hasn't been booted.
4. I copied the clone to make a working-evidence.vhd copy, which i then hashed to confirm it matches the clone. The hash outputted: 9f8a1761ccf71f801bf7d97b01af0c52c3b160a4e939c675c54a586aef558d16 which matches the clone.
5. Ran VBoxManage internalcommands sethduuid on the working copy so that virtualbox will accept it as a separate disk. This changed the hash of the working copy to: ce738168f4bde150b8cfaa5083c93b3d455137a08f4c70393403c36ae676d23d.
6. Using terminal on Mac i hashed the 'contemporaneous notes' pdf at 00:20 on 16/10/2026 it outputted: 3c626edeb7e9e632dc6151575c3587caccb2241658db7d05f37bb1e8bdcf2ca1. This is to show that it wasn't edited during analysis.

## Why?
- Hashes prove that the copy is identical to the source. The post analysis rehash will show that the analysis didn't alter the working copy.
- Analysing a copy means that I can discard the copy and make a new one incase anything goes wrong.

## Problems, Decisions and Limitations
- I originally planned to do a separate master copy. However, I decided to use the clone which hasn't been run as the master to make things simpler.
- I mistyped ~case instead of ~/case when typing in the 'mkdir -p' command. This created a folder named '~case' instead of 'case'. A copy of the laptob disk was saved to this folder at 19:27 on 13/10/2026. I checked the hash of the file in terminal to make sure it matches the clone. Once i confirmed it matches i renamed it and moved it to ~/case/evidence-working.
- The 'laptop' VM went through a snapshot which wouldn't happen in a real forensics acquisition as they would using a physical or software write blocker which is a limitation.
