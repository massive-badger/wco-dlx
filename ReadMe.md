# wco-dlx [![GitHub release](https://img.shields.io/github/release/EpicUnknown/wco-dl.svg?style=flat-square)](https://github.com/EpicUnknown/wco-dl/releases/latest) | [![Github All Releases](https://img.shields.io/github/downloads/EpicUnknown/wco-dl/total.svg?style=flat-square)](https://github.com/EpicUnknown/wco-dl/releases)

**wco-dlx** is a command-line program to download cartoons/anime/movies from WCOStream.com. 

**wco-dlx** is a fork of the excellent **wco-dl** by **EpicUnknown** [available here](https://github.com/EpicUnknown/wco-dl).

## PLEASE NOTE!

> Downloading and distributing content from WCOStream.com is probably illegal.
> This script was written for education purposes purely and you are responsible for its use.
> Show your support for streaming websites/apps by registering a premium subscription account!

Please go check out the wiki as it is indepth on what this script does.

## Table of Contents

* [To-Do](#to-do)
* [Dependencies Installation](#dependencies-installation)
* [Installation](#installation)
* [Python Support](#python-support)
* [Windows Binary](#windows-binary)
* [List of Arguments](#list-of-arguments)
* [Usage](#usage)
    * [Windows](#windows)
    * [Linux/Debian](#linuxdebian)
    * [Example Commands](#example-commands)
    * [Example URLs](#example-urls)
* [Features](#features)
* [Opening An Issue/Requesting A Site](#opening-an-issuerequesting-a-site)
    * [Reporting Issues](#reporting-issues)
    * [Suggesting A Feature](#suggesting-a-feature)

## Dependencies Installation
This script can run on multiple Operating Systems. But, the script depends on some external binaries or libs.

**`These dependencies are required on ALL the operating systems, ALL!.`**

1.) Make sure you have Python installed and is present in your system's path.

2.) Browse to the directory of this script and open command prompt/shell in that directory and run this command :

```
python3 -m pip install -r requirements.txt
```

## Installation
After installing and setting up all the dependencies in your Operating System, you're good to go and use this script.
The instructions for all the OS would remain same. Download this reposititory and put it somewhere in your system.

**Windows users**, it's better to not place it places where it requires administrator privileges. Good example of places to avoid would be `C:\Windows` etc.. This goes for both, the Python script and the windows binary file (.exe).

**Linux/Debian** users make sure that this script is executable.Just run this command, if you run into problem(s) :

`chmod +x __main__.py`

and then, execute with this :

`./__main__.py`

## Python Support
- [ ] Python 2.7 or earlier (Will not support)
- [x] Python 3.5 or newer

## Windows Binary
It is recommended that windows users use this binary to save both, your head and time from installing all the dependencies. 

Go download this binary and start using the script right off the bat:
* `Binary (x64)` : [Click Here](https://github.com/EpicUnknown/wco-dl/releases/latest)


## List of Arguments
Currently, the script supports these arguments :
```
-h, --help                             Prints the basic help menu of the script and exits.
-i,--input                             Defines the input link to the show. [REQUIRED]
-V,--version                           Prints the VERSION and exits.
-hd,--highdef                          Selects 720p version if available (Only 480 and 720 are offered on WCO Stream)
-v,--verbose                           Starts Verbose Logging for detailed information.
-o,--ouput                             Specifies download location
-se,--season                           Selects the season to download of a show (Default = All)
-epr,--episoderange                    Selects the range of episodes to download (Default = All) [ Ex : --range 1-10 (This will download first 10 episodes of ALL Seasons!)]
-x,--exclude                           Specifies what shows not to download [Ex: -x ova,special will make it so no ova or special episodes are downloaded]
-n,--newest                            Downloads the newest episode of the show given.
-sh, --show_downloaded_animes          Show all downloaded shows and episodes.
-us, --update_shows                    Update all shows in your database that have new episodes.
-b, --batch                            Batch download, download multiple anime [Ex : -b ./file_name (a text file with wcostream.com, to download from).
-t, --threads                          This will create multiple threads, in other words download multiple episodes at ones [Ex : -t 4 (Number of threads to create).
```

## Usage
With this script, you have to pass arguments in order to be able to download anything. Passing arguments in a script is pretty easy. Since the script is pretty basic, it doesn't have too many arguments. Go check the [`ARGUMENTS SECTION`](https://github.com/EpicUnknown/wco-dl#list-of-arguments) to know more about which arguments the script offers.

Default Download Location will be the directory in which you run this script. Inside of an Output folder will be each of the show names you have downloaded.

Follow the instructions according to your OS :

### Windows
After you've saved this script in a directory/folder, you need to open `command prompt` and browse to that directory and then execute the script. Let's do it step by step :
* Open the folder where you've downloaded the files of this repository.
* Hold down the **`SHIFT`** key and while holding down the SHIFT key, **`RIGHT CLICK`** and select `Open Command Prompt Here` from the options that show up. <sup>*PowerShell users see below*</sup>
* Now, in the command prompt, type this :

*If you're using the windows binary :*

`wco-dl.exe -i "<URL TO THE SHOW>"`

*If you're using the Python Script :*

`__main__.py -i "<URL TO THE SHOW>"`


### Linux/Debian
After you've saved this script in a directory/folder, you need to open `command prompt` and browse to that directory and then execute the script. Let's do it step by step :
* Open a terminal, `Ctrl + Alt + T` is the shortcut to do so (if you didn't know).
* Now, change the current working directory of the terminal to the one where you've downloaded this repository.
* Now, in the Terminal, type this :

`__main__.py -i "<URL TO THE SHOW>"`

### Example Commands
`__main__.py -i "<Whole Show URL>" -x special,ova -se 2 -epr 1-10` - Download Episodes 1-10 in Season 2 minus specials and ovas

`__main__.py -i "<Single Episode URL>" -o "/home/username/shows/showname` - Download to a specific path!

`__main__.py -i "<Whole Show URL>" -epr 1-10` - Download Episodes 1-10 in ALL seasons

`__main__.py -i "<Whole Show URL>" -se 2` - Download entire of Season 2

`__main__.py -i "<Whole Show URL>" -se 2 -epr 5` - Download Episode 5 of Season 2

`__main__.py -i "<Whole Show URL>" -epr L5` - Get the newest five episodes of the series

### Example URLs
* WCOStream :
    * Single Episode : (https://www.wcostream.com/cool-show-name-here-episode-17-english-subbed)
    * Whole Show : (https://www.wcostream.com/anime/cool-show-name-here-english-subbed)

## Features
This is a very basic and small script, so at the moment it only have a few features.
* Downloads a Single episode
* Downloads and puts them all in a directory named "Output".
* Downloads all the episodes for a show available on WCO Stream.

## Opening An Issue/Requesting A Site
If your're planning to open an issue for the script or ask for a new feature or anything that requires opening an Issue, then please do keep these things in mind.

### Reporting Issues
PLEASE RUN THIS SCRIPT IN A COMMAND LINE (as mentioned in the Usage section) AND DON'T SAY THAT `THE SCRIPT CLOSED TOO QUICK, I COULDN'T SEE`. If something doesn't work like it's supposed to, run the command with the `--verbose` argument. It'll create a `Error Log.txt` file in the same directory. Upload the content of that file on Github Gists/Pastebin etc. and share that link.

If you're here to report an issue, please follow the basic syntax to post a request :

**Subject** : Error That You Get.

**Command Line Arguments You Gave** : The whole command that you gave to execute/run this script.

**Verbose Log Link** : Link to the Gist/Pastebin that holds the content of Error Log.txt.

**Long Explanation** : Describe in details what you saw, what should've happened and what actually happened.

This should be enough, but it'll be great if you can add more
 
### Suggesting A Feature
If you're here to make suggestions, please follow the basic syntax to post a request :

**Subject** : Something that briefly tells us about the feature.

**Long Explanation** : Describe in details what you want and how you want.

This should be enough, but it'll be great if you can add more
