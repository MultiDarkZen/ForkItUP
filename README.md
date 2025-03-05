# ForkItUP
Fork it yourself, (Firefox) The easy way!

Do-It-Yourself Guide: Make Your Own Firefox Fork!

Prerequisites and Setup
1. Install Node.js
   - Verify installation with: node --version

2. Download Visual Studio Community 2022
   - During installation, select these components:
     - Desktop development with C++
     - MSVC v142 toolset
     - Windows 10 SDK
     - CMake

3. Download and Install Mozilla Builds
   - Install to your C drive for easy access

4. Install Mercurial

5. Download Git
   - Use it to clone GitHub repositories to any folder

6. Install Rust
     - In CMD or Windows PowerShell, run:
     - rustup default stable
     - rustup update
   - Check version with: rustc --version

Creating Your Project Directory
1. Open a command prompt and run:
   
    cd /c
    mkdir your-browser
    cd your-browser
   
 Note: Ensure this folder is created on your C drive

Cloning Firefox Source Code
1. Clone the Firefox source code into your directory:
2. git clone https://github.com/mozilla/gecko-dev.git
3. cd gecko-dev
4. Note: This requires Git to be installed

Building Your Fork
1. Bootstrap the Build System
   - Run: ./mach bootstrap

2. Configure Your mozconfig
   - Run these commands to create and configure the mozconfig file:
     - echo 'ac_add_options --disable-crashreporter' > mozconfig
     - echo 'ac_add_options --disable-updater' >> mozconfig
     - echo 'ac_add_options --disable-telemetry' >> mozconfig

3. Build Commands
   - ./mach build
     - Builds the fork
   - ./mach build faster
     - Same as build but faster for smaller changes (e.g., changing a name)
   - ./mach run --purgecaches
     - Runs the browser and purges older cache from previous builds

4. Finalize your fork:
   - Run: ./mach build

Removing a Directory (If Needed)
- To remove a directory:
  - rmdir /s /q C:\name-here

rmdir "C:\your-browser" /s
