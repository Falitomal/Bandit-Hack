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

	The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the ???reset??? command.
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

	Bandit Level 6 ??? Level 7
	Level Goal
	The password for the next level is stored somewhere on the server and has all of the following properties:
	owned by user bandit7
	owned by group bandit6
	33 bytes in size
	Commands you may need to solve this level
	ls , cd , cat , file , du , find , grep

	En este caso, vamos a irnos a la raiz dado que dice en cualquier lugar y vamos a usar el comando "find . -group bandit6 -user bandit7 -size 33c -type f 2>/dev/null", para buscar por group y usuarios, ademas del tama??o especifico y que elimine los errores con "2>/dev/null", encontraremos que en la mitad final de la busqueda hay un archivo en
	"./var/lib/dpkg/info/bandit7.password", entonces mostramos el archivo y obtenemos la clave z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S

Bandit Level 7 ??? Level 8

	Level Goal
	The password for the next level is stored in the file data.txt next to the word millionth

	Commands you may need to solve this level
	man, grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd
	En este level vamos a buscar rapidamente con el comando find el archivo data.txt y que corte donde ponga bandit7, con el comando "find / -type f | grep data.txt | grep bandit7"
	Luego al ver el directorio y el archivo /home/bandit7/data.txt, vamos a leerlo vemos que tiene mucho texto y hacemos una seleccion con la palabra millionth con el comando "cat /home/bandit7/data.txt | grep millionth"
	millionth       TESKZC0XvTetK0S9xNwm25STk5iWrBvP

Bandit Level 8 ??? Level 9
	Level Goal
	The password for the next level is stored in the file data.txt and is the only line of text that occurs only once
	Commands you may need to solve this level
	grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd
	
	En este ejercicio vemos que con ls sale directamente el archivo, asi pues vamos a ordenarlo con sort, se muestran muchas lineas y tenemos que buscar la que no se repita asi pues usamos el comando uniq con -u para mostrar solo las unicas, el comando final seria:
	sort data.txt | uniq -u
	obteniendo en la linea 1001 el password: EN632PlfYiZbn3PhVK3XOGSlNInNE00t

Bandit Level 9 ??? Level 10
	Level Goal
	The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ???=??? characters.
	Commands you may need to solve this level
	grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

	Vemos el archivo en el directorio y usamos cat concatenado junto a strings, vemos que salen varios textos por filas, asi como nos dice que tiene varios == vamos a selecionarlo con grep el resultado del comando es :
	cat data.txt | strings | grep "===="
	y el password es G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s

Bandit Level 10 ??? Level 11
	Level Goal
	The password for the next level is stored in the file data.txt, which contains base64 encoded data

	Commands you may need to solve this level
	grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd
	Lo mismo que en el anterior usamos cat para leerlo junto con base64 -d para que decodifique, luego de haber leido el man de base64, dando el resultado de :
	cat data.txt | base64 -d
	The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM

Bandit Level 11 ??? Level 12
	Level Goal
	The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions
	Commands you may need to solve this level
	grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

	Use info in wiki and command tr, the result is 
	tr 'A-Za-z' 'N-ZA-Mn-za-m' <<< "Gur cnffjbeq vf WIAOOSFzMjXXBC0KoSKBbJ8puQm5lIEi"
	The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv

Bandit Level 12 ??? Level 13
	Level Goal
	The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)

	Commands you may need to solve this level
	grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd, mkdir, cp, mv, file
	Use bzip2, gunzip and mv some times and command file to know that file its
	The password is wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
