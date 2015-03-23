/*
	Author: Chris(tian) "infiSTAR" Lorenzen
	Contact: infiSTAR23@gmail.com
	#92
*/
/* *******************Developer : infiSTAR (infiSTAR23@gmail.com)******************* */
/* **************infiSTAR Copyright®© 2011 - 2015 All rights reserved.************** */
/* *********************************www.infiSTAR.de********************************* */
_______________________________________________________________________________________
Once you purchase, your paypal email will be added to my Updater.
As soon as I am online again I will send you the most recent version, 
as that is always newer then what I have on the store (for several reasons).

CONTACT INFO
http://dayzantihack.com/form.html (infiSTAR23@gmail.com)
http://board.infiSTAR.de
_______________________________________________________________________________________

It is very important that you read through the "run.sqf".
Most people want to run this on AltisLife and forget to change the settings for AltisLife in the "run.sqf".
Also you may want to add/remove from the _devs or _testers arrays.

_______________________________________________________________________________________

The .dll files are not essential and only an addition.
They are not part of the purchase, just an free addition.
All Logs can be found in the server .rpt file.


Installation-Guide:
===================
RUS (thanks to ISP55):
http://epochmod.ru/forum/index.php?/topic/251-ustanovka-a3-antihack-admintools-infistarde/

ALL MODS - infiSTAR_AdminMenu:
ENG:
	To use the infiSTAR_AdminMenu Dialog you will need to edit your current MPMission.
	Go into your servers MPMissions folder and unpack the mission pbo file you want to run.
	Now open the "description.ext" and add this at the very top:
	#include "infiSTAR_AdminMenu.hpp"
	after doing this, you need to copy the "infiSTAR_AdminMenu.hpp" file from "MPMission Addition(s)" into the MPMission (so it is right next to your "description.ext").
	Repack the mission to a pbo again.
	You have to do this, or you will have no AdminMenu..!
	
GER:
	Moin moin,
	von nun an benotigt man eine kleine Datei ("infiSTAR_AdminMenu.hpp") in der MPmission um das AdminMenu nutzen zu konnen.
	Zu finden ist diese Datei im "MPMission Addition(s)" Order aus der infiSTAR.de_A3.zip.
	Zunachst muss man aus dem MPMissions Order auf dem Server die jeweilige Mission herunterladen, bzw herauskopieren.
	Ich empfehle eine Sicherheitskopie anzufertigen.
	Anschlie?end kopiert man nun die "infiSTAR_AdminMenu.hpp" in die MPmission (z.B. "epoch.Altis").
	Zu letzt muss man nur noch die "description.ext", innerhalb dieser Mission offnen und in der ersten Zeile
	#include "infiSTAR_AdminMenu.hpp"
	einfugen, um die Datei auch zu laden.
	Soviel zu dem neuem Dialog, bitte unten weiterlesen :)



ArmA3 Epoch:
01. Disable default AntiHack (SkaroKid copy paste *1) by going into "@EpochHive\epochAH.hpp"
	  antihack_Enabled = false; // built-in Anti-Hack
	  antihack_addOnCheck = false; //addon check
02. Go into your "infiSTAR.de_A3\_Epoch extras\@EpochHive\Addons" folder and copy paste "a3_epoch_infiSTAR.pbo" on your server
	 in the server pbo directory:
	 "@EpochHive\Addons"
	 so it is in the same folder as "a3_epoch_server.pbo"
	 
	 Like this:
	 http://infiSTAR.de/readme/a3_epoch_infiSTAR_location_picture.png
	 
03. Put the following files right next to your "arma3server.exe" (on the Server!).
     A3AH.sqf
     A3AT.sqf
     run.sqf
     all dlls
	  
	  examples:
	  http://infiSTAR.de/readme/AH_files_location_picture.png
	  http://infiSTAR.de/readme/AH_files_location_picture2.png
	  
04. Open the "run.sqf" and add your AdminUID(s), then check if the different settings are fine for you :) - do not edit the other files.
05. Upload the BattleEye Filters from my folder "infiSTAR.de_A3\_Epoch extras\BattlEye\ArmA3 Epoch"
	 into your instance folder (it should have a BEServer cfg file) - overwrite the existing filters but do not delete any file in this folder!
06. Default Open Menu Key is F1




USING THIS ON ALTIS-LIFE:
01. First we need to remove the spyglass start line.
     Open the Altis-Life MPMission folder and replace "initPlayerLocal.sqf" with the one in the folder called "_AltisLife extras" delivered with the AntiHack.
02. Make sure the folder you downloaded the pbo from "AltisLife\@life_server\Addons", only has the life_server.pbo in it.
     If that folder has a subfolder or the unpacked pbo in it -> DELETE that.
	  
	  should be looking like this:
	  http://infiSTAR.de/readme/life_server_pbo_location.png
	  
03. Once you are done, unpack your pbo file (google pbo manager or semilar)
04. go into "life_server" folder and open "init.sqf" (note - we are in the server pbo and not in the MPMission anymore..)
	  
	  this is how the location looks like:
	  http://infiSTAR.de/readme/init.sqf_location.png
	  
05. copy paste
     [] execVM "run.sqf";
     in the first line.
	  
	  should be looking like this:
	  http://infiSTAR.de/readme/firstline.png
	  
06. Put the following files right next to your "arma3server.exe" (on the Server!).
     A3AH.sqf
     A3AT.sqf
     run.sqf
     all dlls
	  
	  examples:
	  http://infiSTAR.de/readme/AH_files_location_picture.png
	  http://infiSTAR.de/readme/AH_files_location_picture2.png
	  
07. Open the "run.sqf" and add your AdminUID(s), then check if the different settings are fine for you :) - do not edit the other files.
	 It is the most important thing that you read carefully through the run.sqf and set all settings correctly for your AltisLife server.
08. Upload the BattleEye Filters from my folder "_AltisLife extras\BattlEye"
	 into your instance folder (it should have a BEServer cfg file) - overwrite the existing filters but do not delete any file in this folder!
09. Default Open Menu Key is F1



Good to know:
1. You can spectate by double clicking the name of a player in the admin menu.
2. Keybinds:
     F1 - Default AdminMenu Key
     F6 - Heal Yourself
     F7 - Heal & Repair withing 15m
     F10 - Stop Spectating
     F11 - Add Ammo for current weapon
     5 - Teleport in looking direction
     6 - Eject CursorTarget
     7 - Lock & Unlock closest vehicle you are aiming at.
     SHIFT & F2 - Adminconsole
     SHIFT & 4 - Fly Up
     SHIFT & TAB - Open Map
	  SHIFT & I - Show Info about CursorTarget
	  DELETE - Delete CursorTarget
	  DIK_PGUP (PageUP) - Flip CursorTarget Vehicle
3. If the map is opened and you hold LEFT-ALT key, you can click on the map and teleport there!
4. If you are added in the run.sqf as an admin, you are able to change from admin to a normal player and back by typing !admin in the chat.


 *1 As some of you may already know, Skaronator is trying to discredit me wherever he can.
    I am not sure if that is just childish behavior or because of the fact that he knows that copy pasting is not the right way to get things done.
    He also has a past(?) as a "hacker" and the default antihack that is within the default arma3 epoch files has a backdoor in it that makes him, avwol and someone else admin on your server.
    Also it allows skaronator to open his custom files/hackmenu.
    Do not believe the rumor or lies spread by him and his friends..
    
    That is how his menu looks like now: http://puu.sh/cyYwV/fab3e36568.png
    not just my old color them, also the same text (admin functions) in the same order and with the same description.
    Even same capital letters that I used :P (totally not copy paste.. *irony*).. http://puu.sh/czcR0/9e7a55a2f4.png
	 
	 Epoch devs are trying to defame me and probably others to be able to copy paste their work and use it as theirs.
	 As we know they are taking part in the contest of "make arma not war" and there is much money in the pot..
	 more about this on http://infistar.de/epoch.html


Have a great day and an awesome expierience,
chris aka infiSTAR


_______________________________________________
infiSTAR.de is used and supported by the biggest and best Communities like:
http://mgtrolls.eu
http://customcombatgaming.com
http://TrainwreckDayZ.com

I am doing this as a passionate 1-man Project.
The tool is actively developed and updated, trying to get the best
results vs Scripters, Hackers while implementing helpful features to administrate your server(s).

I ty to help anyone who needs help but it is very easy structured and self-explaining.
The tool comes with a readme including install instructions and there is even pictures.

If you have seen my tool on another server and you are not convinced about purchasing it yourself or what it does, how it works  or just unsure if you want to purchase it for your server/community.
I can offer you to add your UID to a Test-server so you can at least get a feel of a few benefits you get.

Due to the nature of this software, it needs to be updated quite often, because of new mods, mod updates or new hacks.
I provide Updates and support for my customers for more than 2 years now.
I am happy to go on providing Updates as long as it is possible for me.

Thanks for your attention.

P.S.
Thanks to those, who help(ed) me testing new features, bugs or sending in Hacks to check against them :)
__________________________________________________
problems?
just contact me:
http://infiSTAR.de/form.html

infiSTAR.de & DayzAntiHack.com & Arma-AntiHack.com
altislifeantihack.com & arma3antihack.com & arma3-antihack.net
__________________________________________________
You(I) hereby agree to the following

TERMS AND CONDITIONS
The script (which is a plain written text) stays property of infiSTAR.
As author he is the only one allowed to modify, share (sell, post, [..]) it.
You are not allowed to copy/modify any kind of intellectual property of infiSTAR (this),
unless you are permitted by infiSTAR.
Commercial use is prohibited unless it is permitted by infiSTAR.

REFUND POLICY
You agree that infiSTAR offers no refunds and all payments are final. 
Furthermore, you shall not institute any form or charge-back for any fees paid to infiSTAR. 
You acknowledge that you have read and agree to the above Policy.


Urheber- und Leistungsschutzrechte
Die infiSTAR Dateien und ihr Inhalt unterliegen dem deutschen Urheber- und Leistungsschutzrecht.
Die unerlaubte Vervielfältigung oder Weitergabe einzelner Inhalte oder kompletter Dateien ist nicht gestattet und strafbar.
Es ist ausschließlich der private und nicht kommerziellen Gebrauch erlaubt.
§ 11 UrhG
Das Urheberrecht schützt den Urheber in seinen geistigen und persönlichen Beziehungen zum Werk und in der Nutzung des Werkes.
Es dient zugleich der Sicherung einer angemessenen Vergütung für die Nutzung des Werkes.
§ 97 UrhG
Anspruch auf Unterlassung und Schadensersatz
§ 98 UrhG
Anspruch auf Vernichtung, Rückruf und Überlassung
§ 106 UrhG
Unerlaubte Verwertung urheberrechtlich geschützter Werke
(1) Wer in anderen als den gesetzlich zugelassenen Fällen ohne Einwilligung des Berechtigten ein Werk oder eine Bearbeitung oder Umgestaltung eines Werkes vervielfältigt, verbreitet oder öffentlich wiedergibt, wird mit Freiheitsstrafe bis zu drei Jahren oder mit Geldstrafe bestraft.
(2) Der Versuch ist strafbar.


/* *******************Developer : infiSTAR (infiSTAR23@gmail.com)******************* */
/* **************infiSTAR Copyright®© 2011 - 2015 All rights reserved.************** */
/* *********************************www.infiSTAR.de********************************* */