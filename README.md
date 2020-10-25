![GHDB ICON](https://i.ibb.co/dtn1Lfd/Webp-net-resizeimage-1.png)

# Intermezo


A few moments ago I was mentored by Mr. Digit about Cyber Threat Methods, on that opportunity I was told about Google Dorking. He inspired me to create a tool that can automatically check web vulnerabilities by leveraging the Google Hacking Database from Exploit-DB. This tool also can be used as early warning system based on Google Hacking Database [Exploid-DB] for our system. Once again I am very grateful about sharing experiences together.

## Methods

The techniques used in this tool are as follows:

- Crawling Google Hacking Database from Exploit-DB
- Using crawling results and combines with the target domain to become a search keyword
- Crawling Google Result based on keyword using [Barbarossa](https://github.com/nalonal/barbarossa)
- Display results on screen or save to file

## Requirements
- Python > 3.6
- I try this tools in Windows OS.



# Installation

## 1.Clone and Install Requirements

    git clone https://github.com/nalonal/ghdb.git
    cd ghdb
    pip install -r requirements.txt
    python ghdb.py



## 2.Running Script to Create Cookie.txt File
Run the python script

    python ghdb.py

![create token file](https://i.ibb.co/0c3q2LF/createfile.png)

## 3.Copy Facebook Developer Tools Token to Cookie.txt
open [Facebook Developers Tools](https://developers.facebook.com/tools/) in browser and press Ctrl+i or Ctrl+Shift+i
![enter image description here](https://i.ibb.co/zPjp4WT/cookie.png)
Open file cookie.txt and paste Facebook Developers Tools Cookie to string text paste_here_without_enter

## 4.Create ghbdb.txt Database and Update Google Hacking Database from Exploit
Run again python script

    python ghdb.py

After update cookie success then system will update GHDB and produce ghdb.txt it will take about 1-2 minute
![enter image description here](https://i.ibb.co/kMMWr8G/update-ghdb.png)

## 5.Running File

Running help

    python ghdb.py -h

Running GHDB but just print screen the result

    ghdb.py -d <domain or list domain separate using ','>
    example: ghdb.py -d example.com

Running GHDB and save the result to file

    ghdb.py -d <domain or list domain separate using ','> -o <outputfile>
    ghdb.py -d example.com -o result.txt

# Disclaimer
This script is used as an early warning system based on updating information from the Google Hacking Database [Exploit-DB]. Please use it as wisely as possible

