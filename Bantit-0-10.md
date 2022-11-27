Guide for Bandit Game

Level 0
	connect to bandit.labs.overthewire.org, on port 2220 
	---->

	Open console and paste url with options of ports and user:
	ssh bandit.labs.overthewire.org -l bandit0 -p 2220

Level 1
	The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.
	Commands you may need to solve this level
	ls , cd , cat , file , du , find 
	---->

	Make a ls and see the file readme, then use cat for read the file and search.
	Copy the password, NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
	And now write exit, and connect again with user bandit1 with ssh bandit.labs.overthewire.org -l bandit1 -p 2220

Level 2
	The password for the next level is stored in a file called - located in the home directory
	Commands you may need to solve this level
	ls , cd , cat , file , du , find

	----->
	First use cd .. for see home and users, then see some folders, use cd for navigate to folder "bandit1", now use ls and see file named "-", this is a special character.
	You can see this file with a tip, a "./", to see use command:
	cat ./-
	And now see the password for next level rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi