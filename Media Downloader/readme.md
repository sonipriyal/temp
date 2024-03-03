
##### Overview 
This code takes a webpage/website as an input and identifies the image, audio and video files in it and provides links to download them in your system.

##### Structure 
The code is divided into the `main` function and  a `download` function. The `main` part of the code fetches the input from the user and identifies the type of files by checking its page source. The `download` function is designed to give the user a liberty to choose what files he/she wants to download.

##### Flow of the code 

##### User input 
Prompt the user to enter a webpage URL.

##### Fetch webpage source code 
It used the `curl` command to fetch the source code of the page

##### Extract all links 
The commands `grep` and `awk` are used to extract links from the source code and are stored in a variable called `all_links`.

##### Categorizing the links 
From all the links collected , again the `grep` command is used to filter image, audio and video files according to their file extensions and stored in their respective variables.

##### Downloading the files 
The download function is called three times and every time it sets the `$media_type` value to the corresponding type of file. 

