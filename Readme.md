# Description 
A bat script is also known as a batch script or batch file, is a type of script or program that contains a series of commands that are executed Prompt. It is a simple way to automate tasks in the Windows operating system. In this repo, you will get simple  notes for bat script which will help to work with bat script and I tried my best to explain all commands briefly. 

# Get started with bat file
Here I will explain to you how you can create and write commands in a bat file and how can you edit this file in the future. If you already know how to create and work with bat files then go to the [commands](#com)  section to read about the commands.
So first learn what are the requirements for a bat file, so basically you don’t need anything in order to work with a bat file except the Windows operating system and a simple text editor (notepad, Vs code, Subline text) here we will use Notepad.
Now we will create our first bat file in order to do that open your CMD or Terminal in a suitable location ( suggested: create a folder in Desktop and open there), after opening Terminal or CMD just type the following commands and press enter
    ```bash
        notepad <give a file name>.bat
    ```
Here the ‘notepad’ command will open Notepad for you and after the command, give a required name like ‘myfile’ and at the end of the command don’t forget to give ‘.bat’ extension otherwise it will not work, after doing it , the command should look like this –
   	```bash
    	notepad myfile.bat
   	```
	After clicking enter it will create a bat file with the name of ‘myfile.bat’ and open notepad so that you can type your code here, so go further and let’s 		learn to print ‘Hello world’
   	```bash
    	Echo Hello world
   	```
Write the following command in Notepad and save the file. Type the name of file with extension in the same terminal or CMD and press enter and see what happens. But if you just click on the file, it wouldn’t show anything and it will close within a sec to avoid it and make our scripting, we talk about this 		briefly in the Commands Section.If you want to edit the file then just repeate this command (notepad myfile.bat)
# Commands 
<h2 id="com"> In This section we will see almost most of the commands of bat script with examples</h2>

1.	echo
This command in bat script is use to print any value in terminal, add this as shown in example and try (run it by typing it name in terminal other it wouldn’t work until you add ‘pause’ command).
Example:-
	```bash
 	 echo Hello world
	```

2.	pause
It’s a very important command in bat script, this command normally uses at the end of the script, this command wouldn’t allow your code to do the next step or close the code until you press any key, just add it to your bat file and try it (after adding this command you can the file just by clicking on the file ).
Example:-
	```bash
    	echo Hello world
    	pause
	```
In this case, you can pause your code for being executed until the user presses any key but there is an awesome trick by which you can stop the code a time let look at that example.
Example:-
	```bash
    	echo Hello world
    	ping 127.0.0.1 -n 3 > nul
	```
In this code you can see there is a number 3 after ‘-n’ that’s mean the code will wait for 3 seconds, you can change the value to your requirements like 4 or 5 sec, etc. But there is one problem if you use this line then you have to run the file as administrator then it will work.

3.	@echo off
It’s the most important command in a bat file, this should be added at the first of the code. If I say it in very simple words, it keeps clean your code just by hiding some process so you should add this and if you need more information about it then you make a search.
 Example:-
	```bash
		@echo off
        	echo Hello world
	 	echo don’t forget to give a start
	```
I would like to suggest you to run the code two times, first run without “@echo off” and then run by including “@echo off” and see the differences.

4.	 ren
If you are coming from a programming background it goanna very easy for you to know the use of the command, ‘ren’ or ‘Ren’ is used for giving comments in the code (if you don’t know want is a comment then make a search on the internet)
Example:-
	```bash
    	echo Hello world
	ren Hi, my name is Subho
	```
   
5.	Title <name>
Title is a very useful command in bat scripting by using this you can give a title for your script, if you can’t understand see the picture and see difference.
					<h5 style="text-align: center;">Before adding the code</h5>
     ![before](https://github.com/Subhodip1307/Batch-Script-Guide/assets/111901004/ec67ab9b-608d-4d27-bdb4-89ed290c30f0)
					<h5 style="text-align: center;">After adding the code</h5>
![before](https://github.com/Subhodip1307/Batch-Script-Guide/assets/111901004/573ba17e-335d-43a1-bce7-711158a087ef)


   
Example:-

	```bash
   	@echo off
    	Title Subho1307
    	echo Hello world	
	```
# This is Still not completed please hold on and wait for more.

# If you get any mistake in this repo or you want to contribute then feel free to 





