
<h2 align="center">Task-3</h2>


 # Summary of Task
  
    1- Write a script in Shell.
     
    2- This script has been used to download 2 google sheets. 
     
    3- Both of those Google sheets will have the formate csv file. 
     
    4- Only the name, Average and Sum columns and their values should be printed. 
  
</details>

# Index
  
  
   1- Test cases
   
   2- Implementation 
   
   3- Script 
   
   4- Output of script
   
   5- Conclusion 
   
   6- download files links 
  
  </details>

<details>
  <summary> Test Cases </summary>
  
| **SR-No.** | **TEST CASE** | **COMMAND** | **TEST OUTCOME** | **EXPECTED OUTCOME** | **STATUS** | **REMARKS** |
| --- | --- | --- | --- | --- | --- | ---- |  
| **1** | First, we converted the link of the spreadsheet to the csv format | No Command |After that, We went to publish to the web option then change the spreadsheet link in csv format | After using Publish to the web option in Spreadsheet succesully got the link of Spreadsheet in csv format  | **Passed** | Testing has been passed |
| **2** | Download the spreadsheet | wget -q url of Spreadsheet | We used Wget command to download the spreadsheet in csv format. | After using wget command Spreadsheet successfully download in csv format.  | **Passed** | Testing has been passed |
| **3** | Rename the download file | mv "pub?output=csv" my11.csv | Using mv command  downloaded file successfully  rename. | After using mv command download file was successfully renamed.  | **Passed** | Testing has been passed |
| **4** | Get the output in NAME,AVRAGE and SUM | AWK command | Using awk command got the result of three columns NAME, AVERAGE and SUM | After using awk command, we got the result of 3 columns.Name,average,Sum |  **Passed** | Testing has been passed |
| **5** |After add any column in Spreadsheet  | No command | Using insert option added  any column in spreadsheet got the update result and added column is showing in csv file.| After that when we used inset option, we added any column in the spreadsheet, so we got the result of the update column and added column is showing in csv file.|  **Passed** | Testing has been passed |
| **6** |After add any ROW in Spreadsheet  | No command | Using insert option added any ROW in spreadsheet got the update result and added ROW is showing in csv file.| After that when we used the insert option,we added any row in the spreadsheet,so we got the result of the update row.and added ROW is showing in csv file.|  **Passed** | Testing has been passed |
  
  </details>
  
  <details>
  <summary> Implementation </summary>
  
In this script, first of all I went to publish to the web option and copied the csv link to the spreadsheet
then I used wget command to download the link of the spreadsheet and rename the download file with the mv command.
after that i used awk command to get the required output.
  
  </details>
  
  <details>
  <summary> Script </summary>
 #!/bin/bash
 
ECHO=/usr/bin/echo

WGET=/usr/bin/wget

MV=/usr/bin/mv

RM=/usr/bin/rm

AWK=/usr/bin/awk

#################################################################################################################################
#Script Name : script task

#Discription : 1-This script has been used to download 2 google spread sheets.
#            : 2-Both of those Google sheets will have the format csv file.
#	           : 3-All the columns of the entire csv file will not be printed in the output.
#	           : 4-Only the name, Average and sum columns and their values should be printed
#Author      : Shweta Mishra
#Date        : 20-04-2021
#################################################################################################################################
#This script for Self & other evaluation sheet-1

# Here rm command is used if csv file already exits then delete it.

# wget command is used to download the csv file .

# echo command is used to print  the message.

# if file already exits then delete it

rm -rf my11.csv

echo "self evaluation and other evaluation on the basis of previous performance."

wget -q https://docs.google.com/spreadsheets/d/e/2PACX-1vQjSvAMnKpqXy4p1ZCwoBl3OT4YAC3V8p-YKnciBTuPg-GDlVTJkCRNxYQqG_V99d7r6qTYL8OVrW2E/pub?output=csv

#Here the mv command is used to rename the csv file.

mv "pub?output=csv" my11.csv
#Here awk command is used to print the Name, Average and Sum columns and its value.
 
awk -F"," '
BEGIN {printf "%-15s %9s %5s\n" , "Name", "Average", "SUM" }
NR==4,NR==25{printf "%-15s %3d %10d\n", $2, $11, $11*8}'  /root/my11.csv

#This script for second spread sheet

rm -rf my25.csv

echo "self evaluation and other evaluation on the basis of md file."

wget -q https://docs.google.com/spreadsheets/d/e/2PACX-1vRpppfbIt8hE4xJYHJrvUFtDN22PotSOgvmKjYluc5sm97RBw6cOmuWSxpaiiiWp1pGthVTJqQ_egkE/pub?output=csv
#Here the mv command is used to rename the csv file.

mv "pub?output=csv" my25.csv

#Here awk command is used to print the Name, Average and Sum columns and its value.
 
awk -F"," '

BEGIN {printf "%-15s %9s %5s\n" , "Name", "Average", "SUM" }

NR==4,NR==25{printf "%-15s %3d %10d\n", $2, $11, $11*8}'  /root/my25.csv


  </details>
  
  <details>
 <summary> Output of script </summary>
 
 
  </details>
  
  <details>
  <summary> Conclusion </summary>
  
  I would like to share my experience while doing this work. The given script is doing its job correctly.
  
  </details>
  
  <details>
  <summary> Download files Links </summary>
  
#### Download the google sheet in csv format for evaluation of self and others on the basis of previous performance.
- [Link for download csv file 1](https://docs.google.com/spreadsheets/d/e/2PACX-1vQjSvAMnKpqXy4p1ZCwoBl3OT4YAC3V8p-YKnciBTuPg-GDlVTJkCRNxYQqG_V99d7r6qTYL8OVrW2E/pub?output=csv)


#### Download the google sheet in  csv format for evaluation of self and others on the basis of task1
- [Link for download csv file 2](https://docs.google.com/spreadsheets/d/e/2PACX-1vRpppfbIt8hE4xJYHJrvUFtDN22PotSOgvmKjYluc5sm97RBw6cOmuWSxpaiiiWp1pGthVTJqQ_egkE/pub?output=csv)


  </details>

```
     Thank You
```
