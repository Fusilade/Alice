
** DOWNLOAD THIS README FILE FOR EASY READING - BECAUSE GITHUB FORMATTING IS SHIT! **

----------------------------
Alice Madness Returns
----------------------------
* Title:		Alice Madness Returns Info & Mods
* Date:		June 2024
* Author:		TKBS 
* Mentions:	"sirarthuryeetcannon" (UT-Discord), AlfredStryker (NEXUS-site).
* Desc:		Enable Command Console, Unlock NewGame+, DLC, Menu Choices for weapons/ Dresses & Modify Alice.
* Info:		- "sirarthuryeetcannon" asked if Alice could be edited & mentioned that a post by "AlfredStryker" said console could be enabled
* Infox:	- Not a fan of nexus so i made what i could without seeing alfreds content then checked to see what alfred had done.

[Installtion: Pre-Requisites]
* DirectX
* dotnetfx35
* vcredist - msvc++ 2008 x86
* PhysX - Undocumented.
* SHA1 Certificate

[Versions]
- steam 				= unknown / Not Tested / Not available - Entry Map DIFFs - "VIV" Hex is DIFF/ removed
- GOG 					= unknown / Not Tested / Not available - 
- DVD 					= TODO: Check to see if files are diff. Pretty sure the backup i had on my HDD that i used for this is identical to original Install.  
- EA Latest VS EA old 	= The backup version i have seems ok, there are differences in the entry maps between the latest version and the old version for the acoompanying "viv" file.
* A1+A2 				= Alice 1 can be launched from within Alice 2 - infact - any .exe file can be... i am sure this can be exploited as a backdoor launcher for 16bit and sha1 cert software.
						- Someone could test it with Doom Win95 and see it the top taskbar menu is shown as this would not normally dissappear on anything above Win95 
* NODVD Patch 			= seems ok but as usual because the situation is a touchy subject, no means of replicating a clean crk or loader 
						... i.e. if you own the original DVD and don't want EA or Steam online forced shit then you have to take a risk.
								... if you use online undocumented crk exe then you may end up with the ironically frustration inability to re-edit that exe. (XCom The Bureau DLC becomes unavialable, XCom EU/EW cannot be hex edited for example)
						... i.e. if you want to buy the game you can't as it is not available?.. and due to the SHA1 Cert probably never going to be.
								....Unless an old origin Key can be claimed and it still work if you email EA?
								
*** Probably best not to publish the SHA1 Cert potential issue publicly as EA will DEFINATELY pull the game from the servers.
					
[Instructions (Quick Guide:)]
* [0] Install Game: * Install or Drag n Drop files to location
* [1] Create Shortcut 
* [2] Add modified or Edit ini files to;
*	a) * enable console commands					- See _Input.ini
*	b) * Edit Appcompat & Engine.ini settings you want		- See _Engine.ini & _AppCompat.ini 
*	c) * Add Cheats.txt to the binaries folder
* [3] 1st Run Enable NewGame+ & DLC etc
* [4] In-Game disable PostProcess | fog | MotionBlur | Coronas.

---- Enable Hidden Menu Option: "aliceentryextra" ----
"M:\Games\Alice\Binaries\Win32\AliceMadnessReturns.exe" aliceentryextra -nomoviesstartup -log
 
[Shortcut Example:]
"M:\Games\Alice\Binaries\Win32\AliceMadnessReturns.exe" aliceentryextra -SHOWBUILDVERSION=1 -debug -review -nohomedir -nomoviesstartup -physx -dx11 -freeconsole -allowcheats -offline -mcgee -playtestmode=true -log
// * not all parameters will work for every game,  it is just an example of UE Launch parameters.

---- Enable Console Commands ----
// * Edit the Input.ini to;
* Set a KeyBind ... - > ...to execute a command that... -> ... sets another keybind... -> which opens the command console

[Notes]
* When a Command that has any effect is entered in the console Alices' hair will flutter (turb)

---- Edit Input .ini to enable Console ----
[DefaultInput.ini]
+Bindings=(Name="NumPadOne",Command="set console TypeKey NumPadFour")
+Bindings=(Name="NumPadTwo",Command="set console consolekey NumPadFive")
+Bindings=(Name="NumPadThree",Command="exec cheats.txt")
+Bindings=(Name="NumPadSix",Command="exec Hysteria.txt")

---- Cheats & Console Commands ----
* Group cheats into "cheats.txt" file, place in the "Binaries\xxx.txt" folder so that it can be executed from the command console using "exec xxx.txt"
* See "Cheats.txt" | Cheats-Active.txt | Cheats-All.txt | Hysteria.txt | etc etc 

[Enable "NewGame+" ]  + [Unlock stuff etc]
// When In-Game... (unless you can get the console enabled in the menu first....)
* start a fresh first run -> enable console -> return to menu -> open console & exec cheats to unlock NewGame+ -> goto Chapter Select or "memories" -> Retun to Main Menu, NewGame+ Should now be available

---- Edit App Compat .ini ----
[1] force use of settings from engine ini

---- [AliceCompat.ini] ---- 
[AppCompat]
; BLANK all section in this File to use systemsettings spec
; keep the [AppCompat] LINE above.

---- Edit engine .ini ----
[1] Change Settings you want
[2] * Also set this to true
	GIsSpecialPCEdition=True
* Set to read-only when done.
* The Usual Unreal Engine ini Changes can be applied depending on personal preference.
* changes can also, or alternatively, be made within game to apply to that run.
* Once the APPCompat ini is edited (BLANKED) it should add these lines below to this engine.ini 

---- [AliceEngine.ini] ----
; - Edit path to Alice 1 and set specialedition to true.
[AliceGame.AliceGameEngine]
Alice1Path=.\Alice1\bin
GIsSpecialPCEdition=True
; - ADD THESE LINES if it has not.
[AppCompat]
MeasuredCPUScore=-1.000000
CompatLevelComposite=4
CompatLevelCPU=5
CompatLevelGPU=4


Known Issues:
	* Save Game dissappears when reaching the Oriental Chapter o rother random occassions 
	- recommended to backup save game before - during and after
	* Chapter Select / Continue / NewGame+ BUG - SEE RANT BELOW
	
-------------------------------------------------------------------------------------------
			END ALICE 2 
-------------------------------------------------------------------------------------------

* For "ALICE 1": 

* When looking Inside the "alice.exe" (in hex editor) there is the command line parameter:
	-RunningFromAlice2
	
* Launch Alice1 Without Alice2: Adding this to a command (.bat file) 
"M:\Games\Alice\Alice1\bin\alice.exe" -RunningFromAlice2

* cfg is saved to the my docs folder 
	
this sha1 stuff can be ignored......
					//Note: i have not tested with Windows 7!
						Win10 <-> Windows 7 (any version with SHA1 Block): ensure No SHA-1 Block, SHA-1 is expired/ deprecated  
				TODO:	Update this with KB##### (So users can uninstall sha1 blocker from windows update) 
						- I don't remember ever playing Alice1 and i did not find anything online about in terms of modding like DOOM/ Quake etc or SourcePorts/ Engines.
						* it is signed with a SHA1 which means if you installed the SHA1 Block on Windows 7 or have any OS above it may not work.
						//... but you can launch it from within alice 2... is it possible this can launch other stuff?
						* The usual ID Tech Commands should work (cfg | autoexec.cfg | etc)
						* I tried various methods to Run Alice 1 independant of Alice 2  - all failed. Needs Debugging & Patching.
						- i do not currently have a 32bit OS or anything with NTVDM on.
-------------------------------------------------------------------------------------------
			END ALICE 1 
-------------------------------------------------------------------------------------------

// Links:	// not recommended , just for additional credits reference
https://www.nexusmods.com/alicemadnessreturns/mods/5









	Save Game Rant:
	
	Something within teh persistant save data allows the menu to display the extra dresses and weapons selection.
Without this save data using cheats on a new save alone will not allow selecting those options
a hex edit can be made to change the Completeion from 0 - 100% on a clean save with 0:00 time - then executing the cheats MAY allow the menu slection options to appear but i have not tested - simply becuas eif that does work then the time it takes to learn to debug etc would outweigh the benefit since the save file is only like 2kb and already made.


there is weird save game activity

- If you choose chapter select - any chapter , play for a bit - wait for an autosave - exit to main menu 
it will still display NEWGAME+ -- instead of Continue - which is the expected behaviour - or should be.

To fix this issue you must start from the 100% complete save file - load game - Choose NEWGAME+ & NightMare Difficulty wait for the 1st cutscene with the doctor to end so the autosave finishes. Then q	uit back to main menu - It will now say "Continue" instead of "NewGame+"... Now you can Select any chapter - play a lil - wait for an autosave point (usually occurs immediately) Now when you quit back to teh main menu and press Contionue- it will actually continue from where you last saved from the chapter select,.


It is as if there are 3 functionalities with the options but only 2 m,enus

[1] start newgame + -> save in game -> back to menu -> continue
[2] start from chapter select = does not save persistent data 
[3] Combine [1] With [2] then -> Continue from where you left off in chapter select.
