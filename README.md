# Beefstrike
Penetration testing bot for BeEF and Armitage/Cobalt Strike integration.

+--------------------------------------------+
+         BeEF and Armitage integration      +
+               by @thebenygreen             +
+--------------------------------------------+

The purpose of this script is to add a browser exploitation layer to Armitage using all the power of BeEF features. You will be able to use all the attack workflow of BeEF-xss through the intuitive Armitage's user interface.
Beefstrike assist you in automatic and targeted browser's exploitation.

#WHAT IT DO -
* Connect Armitage to the beef's server 
* Perform MiTM with the help of ettercap and inject beef payload all over the LAN 
* Auto import all the new zombies inside metasploit database
* Auto perform MiTB attack to ensure persistence on the victim's browser.
* Geolocate every new zombies on a google map
* Generate a browser fingerprinting hash (MD5 & SHA-1) for every zombie
* Expose the most effective BeEF's commands in a click & Run fashion (recon, iframe, social engineering, proxy-tunnel ...)
* Generate browser extension able to inject BeEF in every HTTP request (Better persistence)
* Track the results of every commands and log entry from BeEF
* Automatic and targeted client-side attack against browser (Sniper, a native feature or ARE ruleset)
* Export and Import the auto-targeted attack configuration to one and another attack infrastructure
* generate PDF report of BeEF zombies


#HOW TO USE -

For use this script you need to 
1. Download and install all libraries listed on the read_this file located on the lib folder : http://ow.ly/JMx09  
   And modify the  "import" lines on beef_strike script to point to the right path.
        [ Note: beefstrike.iso file have all you need :-)  ]
3. To use MiTM attack, Ettercap must be available on system path. [That is the case in Backtrack & Kali].

4. Launch Beef xss server and Armitage

5. Load beef_strike.cna cortana script. A sub new menu will appear on the attack menu

6. Connect to your Beef server instance.

7. Begin the zombies recruitment. You can use xss exploitation or ettercap method. In this folder you will find the infect.filter file. 
   This is the default file for html injection. You must change it and point to your beef server. 
   The default value is the localhost address and port 3000 the default port of beef server
   Have fun with ettercap filter: http://www.irongeek.com/i.php?page=security/ettercapfilter
      You can also use the web cloner or mass mailer for recruitment purpose.

8. if you have choose MiTM recruitment method, choose the interface to poison and let beef_strike do the job. You can also use hooker to play with beef hook inside cobalt strike workflow.

8. Once a zombie appear, many beef's commands (and you can add) are automatically launch again victim. 
   You have profiling the victim browser (you can see result on zombies menu item). 
   Now feel free to use client-side exploits and send to your zombies through beef invisible iframe module. 

----------------------------------------------------------------------------------------------------------------+
Tested on Backtrack and Kali
Video demos: http://www.youtube.com/watch?v=YhKhkYzq2s8&feature=share&list=UU7_xeQ_4d8jAMtxdJgikjlA
- 		    	http://youtube.com/mrbenygreen	

- LIMITATION -
  The result of some command can only be see on Beef web ui. 

