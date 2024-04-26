# **About the PATH** <br />


### **AUTHOR: Dr Asad Prodhan** https://asadprodhan.github.io/


<br />


PATH is a case-sensitive term in the Linux operating system. The lower case, path, is the location of a particular file or directory. The upper case, PATH, is called an environmental variable.


Now, what is an environmental variable? 


To explain that, let me ask ‘why your Linux computer is displaying everything in English, not in another language?’. Well, this is because you set ‘LANGUAGE=en_AU:en’ when you set up your computer. Likewise, ‘LC_TIME="en_AU.UTF-8"’ will set the time in English. Run ‘locale’ command in your terminal and you will see something like below:
 
 <br />
 <br />
<p align="center">
  <img 
    width="250"
    height="220"
    src="https://github.com/asadprodhan/About-the-PATH/blob/main/PATH_Variables.PNG"
  >
<p align = "center">
Fig. Environmental variables
</p>


All these variables (the left-hand side phrases of the ‘=’ sign in the above figure) are basically setting up the environment how your Linux computer will display the output. As such, these variables are called ‘Environmental Variables’.


In accordance, there is an environmental variable called PATH. PATH contains the locations (paths) for various installed softwares or executables in your computer. So, when you write a command in your terminal and hit ‘Enter’, your Linux machine will look for its executable in the locations saved in the PATH variable. 


If you run ‘echo $PATH’, you will see a collection of paths that are separated by a colon mark (:).


You can keep adding paths to the PATH variable as you install new softwares over times. 
<br />
<br />

>**For example, you have installed ‘guppy’ basecalling software in your computer. And you want to run the 'guppy' command from any directory in your computer. To do so, you will need to add the path (location) of the 'guppy' software in your computer to the PATH variable.**
<br />
<br />

## **How to add a path to the PATH variable?**



- ‘cd’ to the directory, which contains guppy


- get the path of this directory by running PWD command, say the output is something like /home/user_name/Softwares/ont-guppy/bin


- check your existing PATH variable: 

```
echo $PATH 
```


- run 

```
export PATH=$PATH:/home/user_name/Softwares/ont-guppy/bin
```


- now check again: echo $PATH 


The above ‘export’ command will add ‘/home/user_name/Softwares/ont-guppy/bin’ to the existing collections of paths in the PATH variable. 
<br />
<br />


**Now, when you exit your terminal, this newly added path will drop from the PATH variable automatically.**


**This means that you will need to repeat the above steps to execute ‘guppy’ from any directory in your computer.** 


**To avoid it, you can add “export PATH=$PATH:/home/user_name/Softwares/ont-guppy/bin” to the bashrc profile in your Linux computer.**


**This will add the guppy path permanently to the PATH variable.** 
<br />
<br />

## **How to add a path to the PATH variable permanently?**


- ‘cd’ to your user home directory by running just ‘cd’. The output will be something like: /home/user_name


- then, run 
```
nano .bashrc
```


- add the following line to the .bashrc profile

```
export PATH=$PATH:/home/user_name/Softwares/ont-guppy/bin
```


- save and close the .bashrc profile
<br />
<br />

**Now, you can run ‘guppy’ from any directory in your computer, not just from the one where you downloaded and installed ‘guppy’.**


***That’s the power of the PATH environmental variable!! It is briefly called as 'PATH variable'.***
