# DFRWS2019-KAPE-Workshop
Slides, scripts, notes, link, etc from my  2019 DFRWS KAPE Workshop

At a minimum, before you come to the workshop, download ZimmermanTools and KAPE.  Please feel free to install and get familair with them both.

#### Download Get-ZimmermanTools.zip [from here](https://f001.backblazeb2.com/file/EricZimmermanTools/Get-ZimmermanTools.zip)

Unzip the file,  determine where you want to "install the tools" and run the command.  The tools and KAPE can be run from any device ... Hard Drive,  USB Removable drive,  etc.  It is totally portable.

Example:  The PowerShell command below

```
C:\PS> Get-ZimmermanTools.ps1 -Dest c:\tools
```

This example downloads/extracts and saves details about programs to c:\tools directory.  Change the destination drive and folder to meet you needs.

#### Download KAPE from Kroll's Website [found here](https://learn.duffandphelps.com/kape?utm_campaign=2019_cyberitbn-KAPE-launch&utm_source=kroll&utm_medium=referral&utm_term=kape-launch-blog-post) 

Unzip the files to a folder of your choice.  Here is a suggested structure for KAPE and Zimmerman tools locations.  You can put them anywhere you want, even on a thumb drive or external hard drive.

##### Example Folder Structure

![1562561287380](C:\Users\Mark\AppData\Roaming\Typora\typora-user-images\1562561287380.png)

On-Line YAML Validator Sites
https://codebeautify.org/yaml-validator
https://jsonformatter.org/yaml-validator



Commands for the Labs

Lab 2 Simple KAPE command that:

Collects from your own C Drive

Collects LNK FIles and Jump lists.  Run the command below and then review the results.  Look at the folders and files that were collected.  Look at any logs that were produced. Find anything interesting?  Feel feel to practice by running other targets.  All the target configurations should quickly.

`kape --tsource C: --target LnkFilesAndJumpLists --tdest F:\evidence\tdest`





