> ⚠ IMPORTANT: This repo is updated daily, things can be removed / changed anytime - This text will be gone when I got things sorted and misspellings and other small things will be corrected during time, At bottom you will find the "proper" way how things should be done. I do not recommend **anyone to use my methods if you do not know exactly what you are doing**! I really mean what I say, your computer will probably die and never be able to start again. You have been warned, this text will be removed but this repo is FAR away from done. I have hacked those devices since years now and created shotgun tools for older bioses from HP (my first hack as kid was a compaq bios pw). I will add alot of stuff that is not known for the public during time + tools for manipulates data and tools that is used before the motherboards is programmed by manufaturer(HP)..  

<p align="center">
  <img src="https://i.imgur.com/haDz3G6.png" />
  <h2 align="center"># HP Wolf Security: The World’s Most Secure PC’s | Security</h2>
  <h3 align="center">---=== <i>Elitebook</i> - ThinClient - <i>EliteDesk</i> - PowerBook - Printers - BIOS  ===---</i></h3>
</p>

***
> ⚠ WARNING: USE EVERYTHING IN THIS REPO AT YOUR OWN RISK  
> ⚠ WARNING: YOUR COMPUTER WILL BE BRICKED - THERE IS NO GUARANTEES !!
> the developer can never be held responsible for the actions of other users and I have warned you! 
> If the computer is dead, you cant fix it without replacing the  the motherboard. The chip alone is not enough 

> This repo can contain illegal acts depending on the country you live in. It is strictly forbidden and it can end with penalties in high penalties such as imprisonment for fraudulent behavior. You are responsible for your own actions and you can never ever blame wuseman for your acts. **Manipulating** data of various things to deceive a third party by selling a computer where hardware figures are manipulated and false  warranty can be presented  is a very serious crime, in almost all countries.. I urge no one to commit crimes, I dedicate this repo to everyone as a non-profit hacker/cracker of software and hardware devices to show how you are deceived by advertising. 

***

<blockquote>

###### [Video Introduction for Wolf Security: A New Breed of Endpoint Security | Security | HP ](https://www.youtube.com/watch?v=KOq4LutcLr0)

Please watch the video above to follow the story I will do overtime in this repo 
  
  "Hackers are also working from home, isn't it time you had a security that does too? "

</blockquote>

# HP's story:

![Screenshot](https://japan.zdnet.com/storage/2021/06/10/ebe3e11946a47fef8f3d1ce7bc61978c/210610_hp_003.jpg)

* "[What It Really Takes to Catch a Hacker | HP](https://www.youtube.com/watch?v=OiUPrio9eVY)"

* "HP WOLF Security: The hacker is always on THE HUNT"

* "THE WORLD'S MOST SECURE AND MANAGEABLE WORKDTATIONS"

* "PROTECT SENSITIVE DATA AND IP, WITH HARDWARE-ENFORCED SECURITY"

* "Sure Start Protects the Bios"

* Wwhile in the case of WIPER of ransomware attacks or hadware attacks. Sure Recovery provices fast, effective recovery"

* (Nice, I already knew you are creating ransomware ;)

![Screenshot](https://www.securityopenlab.it/immagini/2021/05/hp-1.jpg)

....... it never ends, it's crazy!...... Lets end here else I must quote 100 things they claim in ads since the new name.

# wuseman story:

> My banner is from by HP and the hoodie guy is what HP refers to the "bad guys" and they are the wolves ..

![Screenshot](https://i.imgur.com/eDALA4S.png)

#### If that's true..... We are more vulnerable then ever?

.. Then we should be we able to hack the Bios within seconds ....... is my first thought?

They laught at me because i'm different. I laught at them becuase they all are the same with economic interests.

HP: My first bios I managed to hack was from Compaq and since that day when I was 6 years old I have followed your developers for over 30 years now. We do not have to guess, we know how good your employees are from asia with extremely small salaries while you pull in billions on misleading and false advertising. Who are the "bad guys" in your ads? We'll see. This repo will be updated frequently and recurring as you develop your security. 


***

My first thought that appeared immediately was, if I short circuit the chip it will (please notice healing) heal itself not `recover/restore` itself, `healing` is an unusual word in these terms. I decide to belive my thoughts and the results can be found below .

Sounds crazy? Maybe.. Not for me.. However, this repo will be updated frequently with all kind of HP Devices **AND** I will also include if I fail and what I failed at and what I did. I know there is alot of people that is interested in HP's security f these computers but on other platforms a GitHub.(Forums mostly)

# Hacking Secureboot (incomplete part)

Before you will try anything I wanna tell you that you are able to bypass the secure boot protection if you have some linux skills. Windows setups can be installed allways since the certs are from microsoft, ubuntu and kubuntu I know have preinstalled shim installed.

I dont like those distros or windows so I will add how to fix this so we can boot gentoo minimal cd 

mok + shim ... adding howto later

![Screenshot](.secureboot.bypass/securebootauthrequired.jpg)
![Screenshot](.secureboot.bypass/security_viaolation.jpg)
![Screenshot](.secureboot.bypass/enroll_our_new_keys.jpg)
![Screenshot](.secureboot.bypass/sha256hash.jpg)
![Screenshot](.secureboot.bypass/mokmanagment.jpg)
![Screenshot](.secureboot.bypass/createderfiles.jpg)

## Lets hack!

### HP EliteDesk 800 G5/G2 (DANGEROUS METHOD)

```sh
Born On Date................: `2022-03-01`
Secured by latest features..: `yes`
Bios Chip...................: `25B127DSIG`
BiosProgrammer..............: `CH341a`
Require Bios Programmer.....: `no`
Level of difficulty.........: `simple`

* Tools Recommended:

   Microscope so you can watch the legs so you are not shortcuits the wrong one by mistake

* Tools Required..............: 

  1x Phillips screwdriver 
  1x Tiny wire (I used 2 mini grabbers for safety)  
  
```

This device has an extra option for bios password. It is possible to set security settings to "Ignore" the cmos jumper and reset reset button if pressed on motherboard. If the setting is set to IGNORE you are fucked, you will NOT not succeed in getting around without programmers. so if you try on this unit and do not understand why it does not work, it is precisely because it can ignore this that many other Elitedesk can NOT.

#### The clip is easy to find, its under the below nvme disk (if you have two) and you can read the chip via a Soic Clip 8

![Screenshot](.800.g5.pics/nvme.slot2.jpg)
![Screenshot](.800.g5.pics/clip_chip.jpg)

> THIS WILL BRICK YOUR PC - DO IT ON YOUR OWN RISK!! 
> PLEASE NOTICE THE LEGS 1, 7, 8 are from my PICTURE, NOT FROM THE DATASHEET!!!

* A wire on pin  1 and 7 for ~1.2s erased Intel Firmware 
 
* A wire on pin  1 and 8 for ~1.0s bios noticed something happend and restore itself

*  A wire on leg  1 and 8 for ~3.0s erased Bios Password 

#### Pins

![Screenshot](.800.g5.pics/pins.jpg)

#### Impressive, I was wrong about all this, well well. After 1 touch on pin 1 and 8 (notice just a touch like in 0.1ms) we gonna see below

![Screenshot](.800.g5.pics/1s_is_not_enough.png)

* I still don't trust their shit so before I saying I was wrong and they won, I try 2. seconds!
* Since ages back in the days for some reason I know 4.2 seconds will brick the device if we touch the pins. And this is something I just has figured out on many devices, I can't confirm or promise it will work the same for you so dont listen on this if you didnt try and then cry in pm to me

* I tried to hold a wire on leg 1 and leg 8, now things happens! Bios missmatch! Now its dangerous, and I'm not as impressed anymore. One more wrong and things will be bricked, Now it's 50/50 .. HP or wuseman, who's right? It will not be a fourth time I know from past experience.

![Screenshot](.800.g5.pics/bios_missmatch.jpg)

#### Fuck it, i´m to curios and since ages i know 4.2 seconds is the limit for break things as I said so I decided to try: 3.0 seconds while PC was ON running as normal....
#### after 3.0s I pull the AC and keep it off for 25 seconds.. The PC wont die itself so you must pull the AC

* REMOVE THE BATTERY BEFORE DOING THIS!

#### Fuck, now things was bricked! I thought

![Screenshot](.800.g5.pics/it_does_not_start.gif)

#### Leaving AC out and pressing power button for 25 seconds, gave life to the computer, damn now it flashes red and beeps every time the led flashes! According to the HP dev manual for what 3 x beeps + 3 red flashing indicates its the CPU or GPU. What the hell? It should be 4.2 seconds before it breaks on cpu, mem, motherboard, bios or gpu!

#### Holy maria! it does not even start!

![Screenshot](.800.g5.pics/leds_blinking_red.gif)

#### ...After device is blinking red and fan had run at 10k rpm few times we finally have device booting, THUMBS UP! HP's manuals sucks! ;-)

![Press Me For Video](.800.g5.pics/fan_run_at_max.gif)

#### First screen we gonna see is

![Screenshot](.800.g5.pics/system_time_invalid.jpg)

#### Second screen we gonna see is that intel firmware is fucked, press ok

![Screenshot](.800.g5.pics/intelfirmfucked.jpg)

#### Intel firmware install is in progress

![Screenshot](.800.g5.pics/intel_firmware_running.jpg)

#### Device reboots after a while and reading bios up to 16M will start and finally you will see the below screen.

![Screenshot](.800.g5.pics/bios_part2.jpg)

#### Now the below message popups, what will this result in

![Screenshot](.800.g5.pics/and_secure_boot_keys_seems_gone.jpg)

#### Next screen takes us to to gbe recovery (will it never ends?)

![Screenshot](.800.g5.pics/network_gbe_upgrade_getting_started.jpg)

#### Now it want us to upgrade once again, i choose yes

![Screenshot](.800.g5.pics/import_update.jpg)

#### After the shortcuit and few reboot, it was time to enter bios and see if its password protects!! IT IS GONE!

![Screenshot](.800.g5.pics/bios_removed_lol.jpg)

#### Now, feel free to set your own bios password and then press F11 and choose network recovery

![Screenshot](.800.g5.pics/installing_network_recovery.jpg)

* Worlds most secured BIOS that has hardware protection was hacked in ~3.0 second! 
* The only question I have to HP is, did you never try this? 
* Do you now understand why I want to have a technical analysis for your tests? You talk about losses, re-start by showing your winnings based on false advertising instead.
* You are a scam and fooling your customers with fabricated statistics! **Fuck you!**

***
* If HP's bios is the most secure bios in the world that will protect the companies from hackers incl. tpm protections and keys that will keep the "bad guys" away then im so it's just as true that I'm sitting on the planet "Jupiter" and writing this, there are no laws and rules here so therefore I do not break any laws and rules here, ezi! .. Idiots ... 

***

* *In hps advertising, they are the bad guys, and I the wolf hence the banner! Fuck you HP ... This is just the first part, I will update this repo with MORE proofs of your lies, next up is laptops followed by printers. Stay tuned!

***

## General info about Elitedesks!

#### There is another switch on the motherboard, its not easy to find and the switch is not available wiht chassi closed:

![Screenshot](.800.g5.pics/hidden_button.jpg)
![Screenshot](.800.g5.pics/switch2.jpg)

#### I Really recommends to use a ´better clip then the cheap ones, spend some money for a 3M clip ~20-30€, the chip black ones from china sucks as hell! After 2-3 grabs it's not possible to grab the clip anymore. (probably thats why they sell those clips in 4-6xPackets on amazon - DONT BUY THOSE!!! >See yourself below after FEW grabs, it destroys the chip after few times)

![Screenshot](.800.g5.pics/soic8_did_this.jpg)

#### HP Sure Adminm / Hp Sure Run and Secure PLatform Management is not provisioned anymore

![Screenshot](.800.g5.pics/spm_not_prov.jpg)


#### You are now the full admin of the system and you can erase old TPM and take over this part

![Screenshot](.800.g5.pics/tpm_cleared.jpg)

#### Followed by reset all security featrures, not eve thief protection will help the owner

![Screenshot](.800.g5.pics/reset_all_security_features.png)

#### If you got problems with system recovery via F11 and bios gonna say there is a problem with manifest as: "error finding valid manifest" do as below (this problem was a mess with my Elitebook 870 G3 to figure out and solve: 

![Screenshot](.800.g5.pics/c06425212.png)

* **To avoid the issue:**
* Do not initiate a Preboot network enabled feature when the computer is on low battery power.
* Avoid pressing the power button.
* Do not use the CTRL+ALT+DEL key combination to restart the computer while a download or upload is in progress.
* To work around this issue, perform the following steps to reset the IPv4 configuration:

```sh
1. Power on the computer.
```

```sh
2. Press F3 to enter the 3rd Party Option ROM Management menu.
```

```sh
3. Navigate to Network Device List -> MAC:xx:xx:xx:xx:xx:xx -> IPv4 Network Configuration.
```

```sh
4. Uncheck Configured.
```

```sh
5. Select Save Changes and Exit.
```

***

## Help with password removal 



I don't know if I will add this part here yet but upload your bios dump to any of the forums and I will help you or someone else, I am active there too for this stuff. Please dump the right file and not the firmware file from EFI file. 

Cheers!

## To be added soon.

* How to hack elitbooks bios password, same as above but with wson chips
* How to hack a HP printer remotely
* How we can change serial...
* How we can change uuid....
* How we can set values and how we can unlock the motherboard 
* How we can get info from bios in powershell
* How we can remove the bios from the bios binary file when we have readed the chip
* How to get the SCM.bin tool for older devices (maybe)
* How scm.bin works
* How to get access to HP's private stuff that is public without they know it 
....and alot more, to'be continued!

## SPM 

#### For fix the SPM is not provisiong anymore see below:

If you short cuited the chip, it will be fucked output when you type: 

```sh
Get-HPSecurePlatformState
```

It should be like: 

```
State             : NotConfigured
Version           : 1.0
Nonce             : 0
FeaturesInUse     : None
EndorsementKeyMod : {0, 0, 0, 0...}
SigningKeyMod     : {0, 0, 0, 0...}
```

For fix this, please see below (it will works if your output is fucked too, i never saved the output but you will understand what I mean if you get there and typing the command above) - You also needs HP Sure Admin and HP Recovery from HP's download page (will add urls later, search on hp and you will find for now)

```sh
openssl req -x509 -nodes -newkey rsa:2048 -keyout key.pem -out cert.pem -days 3650 -subj "/C=US/ST=State/L=City/O=Company/OU=Org/CN=www.example.com"

openssl pkcs12  -inkey key.pem -in cert.pem -export -keypbe PBE-SHA1-3DES -certpbe PBE-SHA1-3DES -out kek.pfx -name "HP Secure Platform Key Endorsement Certificate"  -passout pass:test

openssl req -x509 -nodes -newkey rsa:2048 -keyout key.pem -out cert.pem -days 3650 -subj "/C=US/ST=State/L=City/O=Company/OU=Org/CN=www.example.com"

openssl pkcs12 -inkey key.pem -in cert.pem -export -keypbe PBE-SHA1-3DES -certpbe PBE-SHA1-3DES -out sk.pfx -name "HP Secure Platform Signing Key Certificate" -passout pass:test
```

```sh
New-HPSecurePlatformEndorsementKeyProvisioningPayload -EndorsementKeyFile .\kek.pfx -EndorsementKeyPassword test `
             | Set-HPSecurePlatformPayload
 New-HPSecurePlatformSigningKeyProvisioningPayload -EndorsementKeyFile .\kek.pfx -EndorsementKeyPassword test  `
            -SigningKeyFile .\sk.pfx -SigningKeyPassword test  | Set-HPSecurePlatformPayload
```

Now please check again :

```sh
State             : ProvisioningInProgress
Version           : 1.0
Nonce             : 1581536418
FeaturesInUse     : None
EndorsementKeyMod : {236, 247, 128, 76...}
SigningKeyMod     : {194, 160, 105, 233...}
```

So this is about it, when working with Secure Platform Management. To view any associated logs, you can use the Get-HPFirmwareAuditLog function. The last thing you may want to do is deprovision. For this, you will need the endorsement key:

```sh
New-HPSecurePlatformDeprovisioningPayload -EndorsementKeyFile .\tests\testdata\nopw\kek.pfx `
-EndorsementKeyPassword test   | Set-HPSecurePlatformPayload
```

SPM with HPCMSL in the Enterprise

So how would you plug HPCMSL in your enterprise to manage SPM? The solution is meant to be management console agnostic, so whether you use SCCM, Intune, Ivanti, or whatever else, these are the basic steps:

* Install HPCMSL  in a secure location, and place your certificates here.
* Also Install HPCMSL on your managed clients
* In the secure location, use  HPCMSL to generate a secure payload, as described above, using one of the New-* functions.
* Copy this secure payload to your clients via your process of choice. Do not copy your certificates.
* On your clients, apply the payload generated in 3. above, via the Set-HPSecurePlatformPayload function.

All commands can be found here: 

* [Developers Portal](https://developers.hp.com/hp-client-management/doc/firmware?language=es-un)

# All Elitedesk / Elitebooks (The Secure/Recommended way to erase bios password)

This is how you should do it, the dangerous method is NOT something you should try. Follow this instead:

## Linux:

> ⚠ READ + SAVE YOUR BIOS BEFORE YOU ERASING IT IN CASE SOMETHING GOES WRONG

#### Flashrom will detect your chip and know its model by itself:

* Read Chip

```sh
flashrom -p ch341a_spi -r
```

* Read and Backup*

```sh
flashrom -p ch341a_spi -r -o bios_elitebook_backup.bin
```

or

```sh
flashrom -p ch341a_spi -r > bios_elitebook_backup.bin
```
#### Now erase the bios with password protected bios

```sh
flashrom -p ch341a_spi -E
```

You don't need to remove the password from the bin file from a hexeditor, bios will "heal" itself.. Please try. If im wrong, just remove the password via hexedit (this will not be covered in this repo at the moment, will add a tutorial how you can do this without uploading your file for help later) and re-write the chip:

#### Not needed if you are on latest models, but in case you wanna do it:

```sh
flashrom -p ch341a_spi -w hacked_bios_file_with_no_pw.bin
```

#### On older bios versions, you must crack the password OR remove the password from bios file with a hexeditor

> ⚠  READ + SAVE YOUR BIOS BEFORE YOU ERASING IT IN CASE SOMETHING GOES WRONG!

## Windows

Download NeoProgrammer v2.2.0.10 and put the clip on the chip, read bios for backup and then erase it, done!

![Screenshot](.800.g5.pics/reading_chip.png)
![Screenshot](.800.g5.pics/neoprogrammer.png)


#### On older bios versions, you must crack the password OR remove the password from bios file with a hexeditor and write the new bios file to the chip - You should know how to do this if you reading this.

### More devices will be added, to be continued!


***


## HP Urls:

* [HP BIOS Configuration Utility](http://ftp.ext.hp.com//pub/caps-softpaq/cmit/HP_BCU.html)
* [HP BIOS Configuration Utility FAQ](http://whp-hou4.cold.extweb.hp.com/pub/caps-softpaq/cmit/whitepapers/HP_BCU_FAQ.pdf)
* [Client Management Script Library](https://developers.hp.com/hp-client-management/doc/client-management-script-library?language=es-un)


### References

* [Daniel Enberg - How To Deploy HP BIOS Settings Using SCCM and HP BIOS Configuration Utility
](https://www.danielengberg.com/hp-bios-configuration-utility-sccm/)

* [Some HP Laptops Have A Hidden Keylogger That Hackers Can Activate](https://www.techtimes.com/articles/216912/20171212/some-hp-laptops-have-a-hidden-keylogger-that-hackers-can-activate.htm)

* [August, 2010 - Bios Password Hack for HP EliteBook Part 1
](https://syntaxerrorready.wordpress.com/2010/08/24/bios-password-hack-for-hp-elitebook-part-1/)


#### License

This project is licensed under the GNU General Public License v3.0 - see the [LICENSE.md](LICENSE.md) file for details... 

### Contact

  If you have problems, questions, ideas or suggestions please contact me on *_wuseman@nr1.nu_  - For faster contact visit Libera irc network or the webchat and type '/msg wuseman hi!' in the input bar and I will reply to you ASAP.
  
  Enter Libera's network via your own client 'chat.libera.chat:+6697 or use their new web client [here](https://web.libera.chat/).
