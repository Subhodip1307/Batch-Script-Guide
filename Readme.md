<div align="center"> 

![Screenshot 2023-07-02 022244](https://github.com/Subhodip1307/Batch-Script-Guide/assets/111901004/c9b1a5bd-a3ef-4ed8-9119-2acb494fe21e)
<h3>Welcome To Batch Script Full Guide</h3>
</div>

<h1 align="center">Description</h1> 
A bat script is also known as a batch script or batch file, is a type of script or program that contains a series of commands that are executed Prompt. It is a simple way to automate tasks in the Windows operating system. In this repo, you will get simple  notes for bat script which will help to work with bat script and I tried my best to explain all commands briefly and there is some example code written so use it for your learning. 

# Get started with bat file
Here I will explain to you how you can create and write commands in a bat file and how can you edit this file in the future. If you already know how to create and work with bat files then go to the [commands](#com)  section to read about the commands.
So first learn what are the requirements for a bat file, so basically you don’t need anything in order to work with a bat file except the Windows operating system and a simple text editor (notepad, Vs code, Subline text) here we will use Notepad.
Now we will create our first bat file in order to do that open your CMD or Terminal in a suitable location ( suggested: create a folder in Desktop and open there), after opening Terminal or CMD just type the following commands and press enter

```bash
notepad <give a file name>.bat
```
    
Here the ‘notepad’ command will open Notepad for you and after the command, give a required name like ‘myfile’ and at the end of the command don’t forget to give ‘.bat’ extension otherwise it will not work, after doing it, the command should look like this –

```bash
notepad myfile.bat
```
    
After clicking enter it will create a bat file with the name of ‘myfile.bat’ and open Notepad so that you can type your code here, so go further and let’s learn to print ‘Hello world'.

```bash
Echo Hello world
```
     
Write the following command in Notepad and save the file. Type the name of file with extension in the same terminal or CMD and press enter and see what happens. But if you just click on the file, it wouldn’t show anything and it will close within a sec to avoid it and make our scripting, we talk about this 		briefly in the Commands Section.If you want to edit the file then just repeate this command (notepad myfile.bat)
# Commands 
<h2 id="com"> In This section we will see almost most of the commands of bat script with examples</h2>

1.	echo

This command in bat script is used to print any value in the terminal, add this as shown in the example and try (run it by typing its name in the terminal other it wouldn’t work until you add the ‘pause’ command).

Example:-

```bash
echo Hello world
```

2.	pause

It’s a very important command in bat script, this command normally uses at the end of the script, this command wouldn’t allow your code to do the next step or close the code until you press any key, just add it to your bat file and try it (after adding this command you can the file just by clicking on the file ). So it's necessary to add this command in every script where you want to see values or input something(you should add the 'pause' command in our all examples).

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
 
I would like to suggest you, to run the code two times, first run without “@echo off” and then run by including “@echo off” and see the differences.

4.	 rem

If you are coming from a programming background it goanna very easy for you to know the use of the command, ‘rem’ or ‘Rem’ is used for giving comments in the code (if you don’t know want is a comment then make a search on the internet)

Example:-

```bash
echo Hello world
rem Hi, my name is Subho
pause
```
   
5.	Title <name>

Title is a very useful command in bat scripting by using this you can give a title for your script, if you can’t understand see the picture and see the difference.
					<div align="center"> <h5>Before adding the code</h5>
     ![before](https://github.com/Subhodip1307/Batch-Script-Guide/assets/111901004/ec67ab9b-608d-4d27-bdb4-89ed290c30f0)
					<h5 style="text-align: center;">After adding the code</h5>
![title](https://github.com/Subhodip1307/Batch-Script-Guide/assets/111901004/8db2b142-e959-4ba0-86b1-24ab2101b867)


</div>
   
Example:-

```bash
@echo off
Title Subho1307
echo Hello world
pause
rem using pause to see the changes	
```

# Working with variables
In batch script there is two methods to store a value in a variable one is for storing string values and another one is for storing integer values. We will see both of examples.

1.	Variables for String values

If you want to store a string value in a variable then use this flowing command
```bash
Set <variables name> = <put the value>
```

This is only for storing string values(like:- name, words, letters, etc.), change the ‘<variable name>’ with a required name, and change the ‘ <put the value>’ with a suitable value.

Example:-

```bash
Set name= Subho
Set HOME=India
Ren in case of variable letter case doesn’t matters but preferred to use Upper case 
```

Now let’s know how can we print the values that we have saved in variables


Example:-

```bash
Set name= Subho
Set HOME=India
Echo my name is %name%
Echo my home is %HOME%
Echo %HOME%
pause
```

To print the variable value just use ‘%’ before and after the variable name as I shown in the example.  
Here I have shown different methods by using you can print values, and I hope you why we should use pause at the end of the code. 

2.	Variables for String values

Now let’s know how can we store number /integer values to a variable .
To store a number in a variable you just need to add ‘/a’ after the ‘set’ command.

```bash
Set  /a <variable name> = <number>
Ren change the ‘<variable name>’ with any name and change the ‘<number>’ with any number
Ren as example
Set  /a AGE= 20
Ren in case of variable letter case doesn’t matters but preferred to use Upper case 
```

 Now if  you want to print the value then it’s quite simple, just use ‘%’ after and before of the variable name.
  Example:-

```bash
Set  /a AGE= 20
Set HOME=India
Echo my name is %name%
Echo my home is %HOME%
Echo %HOME%
Echo my age is %AGE%
Echo %AGE%
pause
```

# Predefined and Environment variables

In batch Script, there is some Predefined and Environment variables. Simpely it can be said that your computer has some variables with some specific values, which you can use as per your requirement. In this I would not explain them so kindly search in google. I will provide some examples regarding them .

```bash
Echo %RANDOM%
Echo %USERNAME%
Echo %WINDIR%
Ren there is more variables like this, I will al explain in next update 
Ren please wait for upcoming update
pause
```

  
# Taking Input

In this section we will learn about how we can take inputs from the user. First see an example then we will try to understand how the command is working.

Example:-

```bash
Set name= Subho
Set HOME=India
Ren in case of variable letter case doesn’t matters but preferred to use Upper case 
```

Now let’s try to understand what’s happening here and how does it working. So I have already learned to use variables and how can we store values in them, the same thing is applying here, but in this example, we have to use a different command which is ‘/p’ and then we have given a name of the variable (we used ‘name’ as a variable) then we have put a placeholder after ‘=’ (if you don’t know what is a placeholder then please wait I will an image so that you can understand), let see the structure of the code.

 ```bash
Set  /p <variable name> = <placeholder>
Set  /p <variable name> = <placeholder>
```
I hope how to edit these fields and use this so I am not explaining how to edit it.
Let’s run our first example of input-taking and see what happens.

<h3 align="center">The Code</h3>

```bash
Set /p name= Subho
Set /p HOME=India
Ren in case of variable letter case doesn’t matters but preferred to use Upper case 
```

<h3 align="center">After running the code </h3>
<div>
<div align="left">
	
![input1](https://github.com/Subhodip1307/Batch-Script-Guide/assets/111901004/3c836bf4-4978-497a-a1c1-a2a9fb7f20d6)

</div>

<div align="right">

![part2](https://github.com/Subhodip1307/Batch-Script-Guide/assets/111901004/9b6a1126-a9cf-4a5b-811d-c250815dfdf0)

</div>
</div>

<h4><i>I will expalin this picture in next updates</i></h4>

# This is Still not completed please hold on and wait for more. In our future updates we will try to increase the readability of the guide 
# If you facing any problem for  understanding this guide you message me here or [Telegram](https://t.me/Verger_py) me
# If you get any mistake in this repo or you want to contribute then feel free to 





