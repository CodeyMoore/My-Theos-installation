**Codey Moore's Theos installation for noobs**

&nbsp;

**Macintosh installation:**

**Part 1 - Installing brew**

	1. To install brew open your favourite Terminal app (default Terminal app is located in Applications/Utilities)
  
	2. Enter the following command into the Terminal app - /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
	
	This part might take a bit so just dont touch anything and let it do its thing
  
&nbsp;

**Part 2 - Installing and cpan'ing a couple of things (Ldid, XZ and cpan IO::Compress::Lzma)**

	1. Install Ldid with the following command - brew install ldid
	
	2. Install XZ with the following command - brew install xz
	
	3. Lastly we need to cpan "IO::Compress::Lzma" do so with the following command - sudo cpan IO::Compress::Lzma 
	It'll prompt you to type in your admin password, type it in and dont stress 
	if you dont see your pasword on the screen thats just how it is, for whatever reason.

&nbsp;

**Part 3 - Time to install Theos. (Choose a location for Theos, the default location is used below)/the final steps**

	1. Copy and paste the following commands into Terminal and press Enter 
		- export THEOS=~/theos
		- export PATH=$THEOS/bin:$PATH
		- export THEOS_DEVICE_IP=CHANGE_ME_TO_YOUR_IDEVICES_IP THEOS_DEVICE_PORT=22
		
    
	2. Copy and paste the following command into Terminal and press Enter - git clone --recursive https://github.com/theos/theos.git $THEOS
	This part might take a bit so just dont touch anything and let it do its thing
	
  
	3. Now check if Theos is installed. If its not where you installed it to redo the steps above
	
  
	4. Acquire SDKS from somewhere 
	
  
	5. Put the SDK zip (assuming its a zip) into the 'SDKS' folder located in the 'Theos' folder and then unzip them
	
  
	(5a May not be necessary)
	5a. Move the unzipped folder into the following location - /Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/SDKs
	rename the folder with the correct iOS version there for (E.g. iPhoneOS9.2.sdk)
	
  
	6. Move the necessary headers (the files in the folder that was unzipped from the SDK zip) into 'Include' folder in the 'Theos' folder
	
  
	7. Check that Theos is working correctly by run the NIC command - $THEOS/bin/nic.pl

&nbsp;

Thats it! all done. Now you can start making Cydia Tweaks and etc. 

&nbsp;

&nbsp;

**iOS installation:**


**iOS installation thanks to Jake James, go follow him on Twitter - https://twitter.com/Jakeashacks**

&nbsp;

**Part 1 - Jailbreak your iDevice**


	Ill let you do that - www.reddit.com/r/Jailbreak/ - would be a good place to start

&nbsp;

**Part 2 - Adding a repo to Cydia**

	1. Open Cydia and let it refresh (if it has to)
	
	
	2. Go to the Sources tab and in the top right corner click the "Edit" button a pop up will appear copy and paste this repo into that pop up - http://jakeashacks.com/cydia/ - then let Cydia do its thing
	
	
&nbsp;

**Part 3 - Installing everything/the final steps**	
	
	1. Once Cydia has done its thing go to the "Search" tab and search for "Theos Installer" and then que that for install, then search for "MTerminal" and install both "Theos Installer" and "MTerminal"
	
	2. Now open MTerminal type - su - MTerminal will prompt you to type your root password (default password is - alpine - unless you've changed it) then copy and paste the following command - theosinstaller sdk-version - replace sdk-version with the sdk version you want to use (E.g. theosinstaller 9.3)
	
	3. This part might take a bit, once its done you can use the Theos commands below


&nbsp;

&nbsp;

$THEOS/bin/nic.pl - Command for NIC (New Instance Creator) 

&nbsp;

Command for compiling your project, make sure you change your directory (the folder your in) in Terminal.
Use this command to change directory - cd CHANGE/TO/THE/FOLDER/DIRECTORY -)

&nbsp;

make package - Just makes the .deb

make package install - Makes the deb and installs it on your iDevice
