# KAPE Workshop DFRWS 2019 

This Readme page is a one stop shop for all the slides, scripts, notes, link, etc from my  2019 DFRWS KAPE Workshop.  If something is missing,  or you just are looking for some additional information,  create an issue through this GitHub repo and I will do my best to help.  My contact info is in the slide deck and at the bottom of this document.

At a minimum, before you come to the workshop, download ZimmermanTools and KAPE.  Please feel free to install and get familiar with them both.

The slide deck for the Workshop will be posted immediately after wrapping up the workshop.  

This page will change several times between now and conference.  Bookmark this page and check it a few times before you arrive at the workshop.

I hear that there are a large number of people registered for the workshop,  which it awesome but it also means that I could be spread a little thin.  Getting the tools installed on you machine or VM will be a big help.  Instructions to do that install follow.

Looking forward to seeing you all Sunday afternoon.

-Mark

## Installation for the Workshop

#### First,  here is the [Official KAPE Documentation by Eric Zimmerman](https://ericzimmerman.github.io/KapeDocs/#!index.md) 

**Second,  the update and install scripts are run PowerShell**,  that's just how it is.  But really, it is a good thing.  Come on over to the Dark Side.  Once installed and updated you can switch back to cmd if you must.  There is also a Windows GUI for KAPE which we will demo, but is later in the workshop.  

It will be so helpful if each of you could download and install KAPE and ZimmermanTools before you get to the Workshop.  I anticipate the the WiFi that will be available in the meeting rooms, of which there will be more than ours, will be terrible.  So there is a possibility that you will not be able to download in the classroom.  At that point USB drive will be at a premium.  ;-0

#### Step 1 - Download Get-ZimmermanTools.zip [from here](https://f001.backblazeb2.com/file/EricZimmermanTools/Get-ZimmermanTools.zip)

Unzip the file ,  determine where you want to "install the tools", create that folder structure if it does not exist and run the command below.  The tools and KAPE can be run from any device ... Hard Drive,  USB Removable drive,  etc.  It is totally portable.

Example:  The PowerShell command below

```
PS c:\Tools\ZimmermanTools> .\Get-ZimmermanTools.ps1 
```

This example downloads/extracts and saves details about programs to c:\Tools\ZimmermanTools directory.  Change the destination drive and folder to meet you needs.

#### Step 2 - Download KAPE from Kroll's Website [found here](https://learn.duffandphelps.com/kape?utm_campaign=2019_cyberitbn-KAPE-launch&utm_source=kroll&utm_medium=referral&utm_term=kape-launch-blog-post) 

Unzip the files to a folder of your choice.  Here is a suggested structure for KAPE and Zimmerman tools locations.  You can put them anywhere you want, even on a thumb drive or external hard drive.pp

##### Example Folder Structure

![1562561287380](D:\GitHub\DFRWS-2019-KAPE-Workshop\media\1562561287380.png)

#### On-Line YAML Validator Sites

https://codebeautify.org/yaml-validator
https://jsonformatter.org/yaml-validator



### Links to KAPE related Articles

[Official KAPE Documentation by Eric Zimmerman](https://ericzimmerman.github.io/KapeDocs/#!index.md) 

[Introducing KAPE!](https://binaryforay.blogspot.com/2019/02/introducing-kape.html)

[Introduction to KAPE](https://www.youtube.com/watch?v=pZRrZAJif8Q)

[Exploring KAPE’s Graphical User Interface](https://www.kroll.com/en/insights/publications/cyber/exploring-kapes-graphical-user-interface)

[Automating SFTP Creation for KAPE’s Sake!](https://medium.com/@bromiley/automating-sftp-creation-for-kapes-sake-b0bc68d10522)

[KAPE TRICKS](https://thinkdfir.com/2019/02/23/kape-tricks/)



### Links to KAPE related Scripts / Code

Mike Gray's [Get-KapeModuleBinaries](https://github.com/grayfold3d/Get-KapeModuleBinaries#get-kapemodulebinaries) - Downloads binaries used by KAPE Modules



### Commands in the Slides

These are the command show in the slides, you can cut and paste them into to your terminal window or your editor.  Is you have trouble with a particular command referencing these may help you resolve it.



Collect Lnk files and Jumplists from drive C.  Save the output to F:\kape_out\tdest.

`kape --tsource C: --target LnkFilesAndJumpLists --tdest F:\kape_out\tdest`

Collect Evidence of Execution.  Clean up you destination folder before writing new data to it.   Save the output to a vhdx and provide the computer name as the base name for the vhdx.

```
kape --tsource C: --target EvidenceOfExecution --tflush --tdest E:\evidence\tdest --vhdx $env:ComputerName
```

Collect all the registry hives from C and all the volume shadow copies (vss).  Cleanup your target destination before writing new data.  Your destination is on a network and is referenced by a UNC path.  Use an environment var to build the name of the vhdx.

```
kape --tsource C --target RegistryHives --vss --tflush --tdest \\share\DFIRkape_out\tdest --vhdx $env:ComputerName
```







### Hands on Labs

Lab 1.1a - Collect evidence of execution and all registry files from your own system. Your base folder should start with "kape_out".  Example:  F:\kape_out.  After the command has finished,  review the folder structure that was created under F:\kape_out\tdest\C.  Last

```
kape --tsource C: --target LnkFilesAndJumpLists,EvidenceOfExecution --tdest F:\kape_out\tdest
```

Lab 1.1b - What was the total execution time according to the Console_Log.txt

Lab 1.1c -  We you looked at the LNK files,  did you see anything unexpected?



Lab 1.2 

```
kape --tsource C --target RegistryHives --vss --tflush --tdest F:\kape_out\tdest --vhdx $env:ComputerName
```



### Contact Information

#### Mark Hallman

Email:   [mark.hallman@gmail.com](mailto:mark.hallman@gmail.com)  
Skype:   mhallman
Twitter:   @mhallman

