Guide for Bandit Game

Level 0

	connect to bandit.labs.overthewire.org, on port 2220 
	---->

	Open console and paste url with options of ports and user:
	ssh bandit.labs.overthewire.org -l bandit0 -p 2220

Level 0-1
	---->

	The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.
	Commands you may need to solve this level
	ls , cd , cat , file , du , find 


	Make a ls and see the file readme, then use cat for read the file and search.
	Copy the password, NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
	And now write exit, and connect again with user bandit1 with ssh bandit.labs.overthewire.org -l bandit1 -p 2220

Level 1-2
	----->

	The password for the next level is stored in a file called - located in the home directory
	Commands you may need to solve this level
	ls , cd , cat , file , du , find

	First use cd .. for see home and users, then see some folders, use cd for navigate to folder "bandit1", now use ls and see file named "-", this is a special character.
	You can see this file with a tip, a "./", to see use command:
	cat ./-
	And now see the password for next level rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi

Level 2-3
	----->

	The password for the next level is stored in a file called spaces in this filename located in the home directory
	Commands you may need to solve this level
	ls , cd , cat , file , du , find

	This is very simple, use ls see the archive, and use cat write space and pulse key "tab"
	Copy the key: aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG

Level 3-4
	----->

	The password for the next level is stored in a hidden file in the inhere directory.
	Commands you may need to solve this level
	ls , cd , cat , file , du , find

	use cd for navigate in folder "inhere", then use "ls -la" for search hidden files, now use cat .hidden and copy the key
	2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe


Level 4-5
	----->

	The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.
	Commands you may need to solve this level
	ls , cd , cat , file , du , find

	Again use cd for navigate in folder "inhere", now use ls -la and see some files type "-file0*", then use cat ./-file00 and repeat in all archives,
	only the file 7 have characters readeable, see the code and copy 
	lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR

Level 5-6
	----->
	
	The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:

    human-readable
    1033 bytes in size
    not executable

	Commands you may need to solve this level
	ls , cd , cat , file , du , find

	Navigate again inside the folder "inhere", now use ls -Rla for searh in all folders and search 1033 bytes, a tip, with pipex | and grep "1033" see the name of file is "file2".
	The command for search, "ls -Rla | grep "1033"", now see in all folder the file, then the folder "./maybehere07" contains the file, use cat for read type this "cat ./.file2"
	Copy the code, P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU

Level 6-7
	----->