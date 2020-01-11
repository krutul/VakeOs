# VakeOs
REMASTERING VAKE OS

How To Remastering Ubuntu 16.04 LTS to VakeOS 1.1 using Pinguy Builder


Download application:
* gnome-tweak-tool
* Pinguy Bulider 4.3

Step to customize:

1. Install Aps
* sudo apt-get install inkscape 
* sudo apt-get install gimp 
* sudo apt-get install synfig 
* sudo apt-get install blander 
* sudo apt-get install k3d 
* sudo apt-get install wings3d 
* sudo apt-get install krita 
* sudo apt-get install mypaint
* sudo apt-get install  tupi

2. Change the  icon. 
* you can download flat remix on https://github.com/daniruiz/flat-remix
* extract the zip file
* for our project we use  Flat-Remix-Blue-Dark icon
* copy directory  Flat-Remix-Blue-Dark in Download to /usr/share/icon
* change the icon with gnome-tweak-tool

3. Change Theme
We use arc-theme for our project, for more information you can read on https://github.com/arc-design/arc-theme. The command to install theme:
* sudo add-apt-epository ppa:noobslab/themes
* sudo apt-get update
* sudo apt-get install arc-theme
	Change theme with gnome-tweak-tool, then choose arc-dark-solid

4. Change icon launcher 
Download icons from https://drive.google.com/open?id=141Ldyp4xleLPpvUC4ifPJijiN-E9ZT8I
* cd Downloads/ 
* sudo mv launcher.png /usr/share/unity/icons 
* cd /usr/share/unity/icons 
* sudo mv launcher_bfb.png 1.png 
* sudo mv launcher.png launcher_bfb.png 

5. Change Dock or launcher Position 
* gsettings set com.canonical.Unity.Launcher launcher-position Bottom 

6. Change Walpaper and lockscreen 
* Choose vakewallpaper.png in Downloads and set to wallpapper

7. Change Plymouth 
* sudo cp plymouth.png /usr/share/plymouth
* sudo cp plymouth.png /usr/share/plymouth/themes/ubuntu-logo/
* cd /usr/share/plymouth/
* sudo mv plymouth.png ubuntu-logo.png
* cd /usr/share/plymouth/themes/ubuntu-logo/
* sudo rm ubuntu-logo.png
* sudo rm ubuntu-logo16.png
* sudo mv plymouth.png ubuntu-logo.png
* sudo cp ubuntu-logo.png ubuntu-logo16.png
* sudo nano ubuntu-logo.script
set configuration like :
window.SetBackgroundTopColor (0.00, 0.00, 0.255)
window.SetBackgroundBottomColor(0.20, 0.00, 0.00)
bits_per_pixel = Window.GetBitsPerPixel();
if (bits_per_pixel == 4) {
		logo_filename= “ubuntu-logo16.png”}
else {
		logo_filename= “ubuntu-logo.png”}
* sudo update-alternatives –config defult.plymouth
	(select number 2 or file was configured) 
* reboot 

6. Edit lsb release and issue 
* sudo nano /etc/issue 
set configuration to :
VakeOS 1.1 PB \n \l 
* sudo nano /etc/issue.net
set configuration to :
VakeOS 1.1 PB
* sudo nano /etc/lsb-release 
* sudo nano /etc/os-release

8. Change detail image
* sudo cp vakeOS.png /usr/share/unity-control-center/ui
* cd /usr/share/unity-control-center/ui
* sudo rm UbuntuLogo.png
* sudo mv vakeOS.png UbuntuLogo.png

9.Step to remastering :
* sudo apt-get install syslinux-utils
* sudo apt-get install isolinux
* sudo apt-get install ubiquity-frontend-gtk
* sudo apt-get install gdebi
* sudo gdebi pinguybuilder_4.3-8_all-beta.deb
Open pinguy builder and select the picture needed in Download
Costumize name file in settings tab. 


Link Apps and video
- Pinguy Builder: https://sourceforge.net/projects/pinguy-os/files/ISO_Builder/
- Icon : https://github.com/daniruiz/flat-remix
- picture and logo : https://drive.google.com/open?id=141Ldyp4xleLPpvUC4ifPJijiN-E9ZT8I
- All Applications installing from terminal
- Video Tutorial: https://youtu.be/O7u_LAmt-cU

our team :
1. Moh. Khoirul Anwar 18.01.4216
2. Cessaricki Yudi Kurniadi 18.01.4259
3. Alfiana Rismawati Wibowo 18.01.4149
4. Rizah pahlipi 18.01.4218
