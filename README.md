# wiki-use-the-scripts
This repository explains how to configure your laptop in order to use the different scripts within the organization.

If you have never coded before or have a faint notion of what is it, keep yourself here for further explanation. In case you already know the gist, then check out [this repo](https://github.com/ABEI-Energy/wiki-how-to-git).

## Set up
To run the programs, you need an environment to work within. You can download VS Code from their website [Download VS Code](https://code.visualstudio.com/), just select the download the site offers in the first place.

![VS code install](https://user-images.githubusercontent.com/116873281/200835711-bf44f5b9-e6ca-42e0-95cc-361745b6cded.png)

Great! Now you have installed successfully VS Code. It should look something like this:

![Visual Studio first page](https://user-images.githubusercontent.com/116873281/200892720-0fbc8f0e-ba52-45ce-a516-145a11100b39.png)

As you can see on the image above, the circle points at the "Extensions" tab of VS Code. Here you can customise your experience with VS. In this case, we will need to go there to install a few extensions that will help us to run the scripts.

>**Note** **If you are here we assume you just want to run a certain script here and there and not actively code or add to any of the repositories. As so, you will need just some extensions.**

#### Python extension
It will provide the language required to read the scripts (or write onto them).

![python extension](https://user-images.githubusercontent.com/116873281/200858537-7f164807-9aed-44f7-b664-2d92a1598c82.png)

#### Python interpreter
[Download python interpreter](https://www.python.org/ftp/python/3.11.0/python-3.11.0-amd64.exe)

In case you have some trouble with the installation of python, check this [Get started with Python in VS Code](https://code.visualstudio.com/docs/python/python-tutorial)

## How to get the script

Go to the [ABEI repository](https://github.com/orgs/ABEI-Energy/repositories) and you should look for the Scripts 

![image](https://user-images.githubusercontent.com/116873281/204485747-e9ca02c3-3b2a-4483-8d80-f0df9fb8ecc6.png)

Once opened you should be greeted with a bunch of files, maybe a wiki, anyother folder, etc. 
![image](https://user-images.githubusercontent.com/116873281/204486345-aad4e4d9-5a16-4362-aa0c-93316807dfaa.png)

Go to the <img src="https://user-images.githubusercontent.com/116873281/204487640-694e76ba-66c6-4f86-ba1c-b3e469249cbe.png" width="90" height="30"> button and click on it.

![image](https://user-images.githubusercontent.com/116873281/204489064-20a5d21b-5c22-41d2-a992-5ad66e110f7f.png)

Just download the .zip file and save it somewhere in your computer where you can access to it easily. 

After that, open VS Code where you should be greeted by something like this (and if not, go to the upper file menu bar  ```Help -> Get Started```)

![getstarted](https://user-images.githubusercontent.com/116873281/204485974-cc8e6af1-2b70-4a44-876b-7b3b319f60b2.png)

 Go click on ```Open Folder...``` and choose the one you just created a few steps ago.
 
 &nbsp;Opening the folder       |  Choosing the folder
:-------------------------:|:-------------------------:
![image](https://user-images.githubusercontent.com/116873281/204495379-84fda3f0-b0f0-4a2f-b40a-f42468f1337f.png)|  ![image](https://user-images.githubusercontent.com/116873281/204497056-ecd8773a-c34e-44ba-a3a8-89dfd47c50e8.png)
>**Warning** When extracting the .zip folder, make sure the folder you are opening does not contain another folder with the same name that the one you exctracted. If this happens, take out the inner folder to another place, or when choosing the folder in VScode, make sure to select the inner folder when opening (see the image below)
>![image](https://user-images.githubusercontent.com/116873281/204500091-5b3b4772-2733-4779-b9a0-07a512ac8061.png)

And once opened, you should see that VScode greets you with something like this:

![image](https://user-images.githubusercontent.com/116873281/204500266-9aeac9ac-e80c-4b69-8227-8f3275ce1b31.png)

## How to run the script

All the elements you see in the side bar of VScode are there for a reason and you should touch them the least possible. The ones you should be interested in are the **README.md** and the **main.py**. 

The first one is the instructions on how to run the script. As a rule of thumb, you will just have to hit run and follow the instructions prompted by the terminal. However, some other scripts will require you to drag files into a folder within VScode or do something in particular. The main.py is the main code and is what you have to execute following the instructions on the README document. 

>**Warning** Since you are opening a code editor, it is easy to slip in and maybe modify by error certain things here and there. The way this wiki is explaining it is to make it as easy as possible. Nevertheless, if you want to dig a little deeper, you can prevent in a better way the small (or big) mistakes by means of **Cloning the repository** as explained [here](https://github.com/ABEI-Energy/wiki-how-to-git/blob/master/README.md#how-to-clone). It is a little bit more cumbersome but it will give you some peace of mind ensuring that no matter what you do, if you change anything VScode will make it obvious for you and you will be able to step back as much as you want.

Almost all, (not to say the whole of) the scripts have to run in a virtual environment. This is because the programs need certain libraries that are updated from time to time and occupy space, therefore having them installed "outside" will make things easier for everybody. 

## How to create a virtual environment

Open the main.py file in VScode. Once opened, you will need a terminal. You can use the shortcut ```ctrl+shift+ñ``` or go to the menu located on the upper part and click on ```Terminal-->New terminal```, which will make appear something like this on the bottom of your screen:

![terminal](https://user-images.githubusercontent.com/116873281/200888248-6bd2fece-808c-4915-9b9f-3b944c4fc30e.png)

Click on the blinking cursor and type in the following commands (hit enter after each one of them):
```ruby
pip install --user virtualenv 
```
```ruby
python -m venv venv
```
In this step VS Code will ask us to select a new workspace folder, we chose yes:

![popup](https://user-images.githubusercontent.com/116873281/200890130-00799449-d003-40e6-9cf1-3a01445d66c5.png)

And we continue with the following commands in the terminal as previously:
```ruby
cd venv
```
```ruby
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope Process
```
```ruby
Scripts/activate.ps1
```
After this step, your terminal should show the following on the left part, indicating that the virtual environment is activated.

![venvsaved](https://user-images.githubusercontent.com/116873281/200893486-ea5ba188-cfa1-4477-82ff-a4baca72d0e7.png)

As well, down in the right part of the window, it should be seen that the interpreter has changed to 'venv'

![underscore ](https://user-images.githubusercontent.com/116873281/200894790-09732c3b-f2b9-477f-9cfc-76de6daffe2b.png)

To finally install all the packages we need to run the program we cloned, we proceed as follows
```ruby
cd..
```
```ruby
pip install -r requirements.txt 
```
This last step might take time, but you should see how the first lines of your ```main.py```file (the ones with ```import Package as pck``` are not red-underscored anymore). That means that the virtual environment is correctly installed. 

And, now yes, finally, go to the right-upper part to run the script that README indicates (usually the main.py mentioned before) with whatever the instructions are to make it work. 

![play](https://user-images.githubusercontent.com/116873281/201102119-f7c563ad-22bd-495e-bb3d-b0dea2a41f4e.png)

>**Note** The terminal might ask you to verify certain things (such as if you have access to certain folders for example) which are yes/no questions. Simply type in ```Y``` or ```N``` and hit enter every time. On other occasions it might ask you certain data, but this will be stated in the README, so just follow what it says and you should be fine.


### Some extra tips 
- If you need to run this repository once again, VS will remember that you once did all of this, therefore just open VS Code as in the first steps, and you should see somewhere all of your recent files.
- **To re-activate again the virtual environment:** Open the terminal again and type in ```venv\Scripts\activate.ps1```, and the ```(venv)``` should appear again.
- If you want to verify that your program is all set-up after installing the requirements, run (within the venv, i.e. the coloured venv logo should appear in the terminal directory) ```pip list```, and there you should see the different packages that should have been installed from the file ```requirements.txt```

![recent](https://user-images.githubusercontent.com/116873281/200894338-8bc435ce-2ac4-4548-9df3-3df14eaa7513.png)




