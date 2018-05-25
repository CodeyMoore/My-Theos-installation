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

**Part 3 - Time to install Theos. (Choose a location for Theos, the default location is used below)**

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

$THEOS/bin/nic.pl - Command for NIC (New Instance Creator) 

&nbsp;

Command for compiling your project, make sure you change your directory (the folder your in) in Terminal use this command to change directory - cd CHANGE/TO/THE/FOLDER/DIRECTORY -.

&nbsp;

make package - Just makes the .deb

&nbsp;

make package install - Makes the deb and installs it on your iDevice

&nbsp;

**iOS installation:**


**COMING SOON**
