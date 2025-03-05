#ForkItUp

Do it yourself Guide, Make your own Firefox Fork!

I almost forgot, make sure to disable your anti-virus while you are building your fork 
because it will falsely flag it as malware and delete the files if 
you try to build it  with it enabled! It's A false-flag.


Install Node.js.com
node --version checks installation 

Download visual studio community 2022 version, https://visualstudio.microsoft.com/downloads/
when installing select these components
Desktop development with C++
MSVC v142 toolset
Windows 10 or 11 SDK
CMake

Download and install https://wiki.mozilla.org/MozillaBuild to your C drive for easy access
Download https://www.mercurial-scm.org/
Download https://git-scm.com/ to clone GitHub repositories to any folder

Install Rust using CMD or Windows PowerShell |

rustup default stable
rustup update
Check version
rustc --version this checks the version you have installed

restart computer

|COMMANDS|

cd /c
mkdir your-browser
cd your-browser 

this creates a new folder with the name you chose 
Make sure to make the folder in your C drive

Now clone the Firefox source code inside of  your Directory

git clone https://github.com/mozilla/gecko-dev.git
cd gecko-dev
./mach bootstrap installs required files in your folder/ sets it up\ Do this after cloning the source-code, make your you are in cd gecko-dev first!


This is why you need git installed, now locate your mozilla-build folder and open start-shell.bat
./mach build faster same thing as build but is much faster for smaller changes you made.
./mach run --purgecaches runs the browser and purges any older cache from previous build
./mach build |
Builds the fork





Configure your mozconfig | Do this after building your fork first just in case it might cause issues

echo 'ac_add_options --'disable-crashreporter' mozconfig
echo 'ac_add_options --'disable-updater'  mozconfig
echo 'ac_add_options --'disable-telemetry' mozconfig

 
now build your browser! ./mach build to finalize the fork!


removes a directory | (If Needed)

rmdir /s /q C:\your directory here



Signed -- MultiDarkZen



happy forking!
