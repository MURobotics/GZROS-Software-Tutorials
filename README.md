# MU Robotics Software Tutorial 1: Setting Up

### Preface
This tutorial will walk you through the process to setup the development environment that we will use within our other tutorials. There are multiple options to set up the development environment, and we encourage you to consider which option will be the best for you. We will provide the best recommended options given the available software for engineering students, free options, ease of setup and more.

### Hardware/Software Requirements?
Currently, these methods should be supported on Windows, Mac and Ubuntu to varying degrees of ease to implement.

In consideration to processor architecture, while x86 is the expected processor architecture, accommodations can be made to support arm-based processors if needed.

For minimum system requirements, requirements can vary between methods. It is encouraged that you have 2 cores and 4GB of RAM. It is additionally encouraged that your system has a form of GPU to assist in removing the burden of rendering the simulation (for Methods 1 & Bonus). While there is a chance that these tutorials can work with any system not fulfilling these requirements, we expect the minimum viable performance to be at this level.

If you are using the methods involving virtual machines, you'll want atleast 25GB of free memory (Storage, not RAM) (20GB is the default for the Virtual Machine). If you are planning on running the Development Environment Natively or with Docker, it's reccommended to have approximately 7-10GB of memory available.

## **IMPORTANT:** How to choose a method
Each method has its own pros and cons, and depending on what your priorities are, it can greatly impact your decision. Here is a list of methods that you can choose between and what their benefits and drawbacks are.

- Method 1 (using VMWare): What makes this method unique is how VMware has excellent support for computer GPUs and it allows for people to run VMs with little performance impacts compared to a native system. The reason why this is the recommended method is that it has a stark advantage on framerates compared to using Method 2 (Virtual Box) and Method 3 (Native Docker) due primarily to the aforementioned reason. The main drawback its software is only free to those who are enrolled within the College of Engineering, while we go through the process of downloading it, this can detract people from its uses.

- Method 2 (using Virtual Box): Admittedly, we're on the fence about the use of this option. With some manual GPU modifications, we're sure it could be more powerful than the native docker option. With that in mind, it appears to have a slower response from a stock configuration that what's desired on OSX (Mac). While this currently has the worst performance, we've included it as an option as other Operating Systems might have better experience using it. Additionally, it's a free VM software that could be viewed as an alternative if Method 3 fell through, or if you have the experience to optimize the graphics.

- Method 3 (Running Docker Natively with no VM): This was the original method for working with the development environment and as such, has its own merits to its creation. This is the simplest to set up (if you can install docker and docker-compose) and should take the least ammount of storage in your PC. While this is the case, the drawback lies within its responsiveness and FPS (this is due to a difference in communication protocols). While it's better than the Virtual Box method, there is a noticable difference in FPS (not awful, but definitely not 60FPS). While it is a noticable difference, it's preferred over Virtual Box, as it's an easier setup, and you can view your simulations within your browser, this is additionally the way how I (the guy writing this) develop out our programs, as it's pretty straight forward and has the best rebuild times, but I would use method 1 if I had to manually edit the simulation worlds for the better performance.

- Bonus Method (If you have Ubuntu 18.04 already installed on your PC): As long as your PC drivers were set-up properly, this would result in the optimal performance for your development. While this would result in the best performance, we would only encourage you to use this path if you already have sufficient experience with linux or if you know how to setup a dual-boot on your PC. In the steps I will show you what items you'll need to install, and the links to do so, but additionally the tutorial will assume you can understand what the instructions are having you do and you will want to place care into ensuring you follow only the required steps of your system.

## Method 1 (free for MU Engineering students, recommended for those without Ubuntu OS): Using VMware for virtual machine management

This method will have us walk through the process of setting up a virtual machine which has Ubuntu installed along with the core software required for these tutorials, in addition to other robotics components you can work with in the future. We will work towards how you can get VM Ware for free, and the process to setup and install the development environment.

### Part 1: Downloading VMware

#### Step 1: Logging into the College of Engineering's web store
For us to download and use VMWare fusion, we first want to renew a license. By following this [link](https://e5.onthehub.com/WebStore/ProductsByMajorVersionList.aspx?ws=e9adeca3-0c29-de11-a497-0030485a8df0&vsro=8), you should be able to login to College of Engineering's web store with your standard 2-factor login information.

#### Step 2: Select the appropriate VMware option
 - For Windows and Linux users, you'll want to download VMware Workstation pro, and select the appropriate operating system
 - For Mac users, you'll want to download VMware Fusion pro
 - **Both licenses should be free in the COE Store. If not, you can defer to the other methods below**

#### Step 3: Download the appropriate VMware software

### Part 2: Setting up the Dev Virtual Machine

#### Step 1: Install the Virtual Machine package
On your host machine, you'll want to download the [Dev Env.ova]() file that is on Mizzou's box account. Then wait for it to install.

#### Step 2: Import the Virtual Machine package into VMware
Open up VMWare and select File > Import > Choose File, then select your recently downloaded Dev Env.ova file. Once selected, click through the process of setting up the import by saving your virtual machine location and allowing it to build.

#### **NOTE:** VMware might provide an error, stating that the .ova file doesn't match a hardware specification. If this occurs, press retry as it will remove high level warnings and allow for the import to start.

#### Step 3: Configure your Virtual Machine Settings
Either select the customize settings button on the finished page, or select the tool icon to configure your virtual machine. We recommend going to the Processor & Memory section to select how many processor cores and RAM you want. A recommended amount is 2 cores and 4096MB of RAM.

### Part 3: The initial launch of your Virtual Machine

#### Step 1: Activate your Virtual Machine
Select your Virtual Machine to launch it with your configured settings. VM ware might provide a pop-up asking to upgrade your virtual machine, we recommend that you select to upgrade it, then wait for the setup to complete.

**Note:** If you accidentally pressed cancel or no, you may upgrade by going into the 'compatibility' section of the virtual machine settings page when the virtual machine is off, then select 'upgrade'

#### Step 2: Logging in
Select the MU Robotics account for the lock screen, it will ask you for a password which is "robotics". With this you should be able to see a desktop.

#### Step 3: Adjust your Display
To adjust your display, you may select the icon in the bottom left corner, then you should be able to select the settings icon (if it's not visible, select the 'All' tab at the bottom of the screen). Then, you may change the resolution of your screen to your preferred pixel ratio. (1680 x 1050 @16:10 works well for a full-screen 2017 MacBook Pro)

### Part 4: Testing

#### Step 1: Create a Project Folder
On your desktop, if you right click, you can make a folder that we will place our future projects in (this will be known as our project folder). For the tutorials, our folder will be called 'projects'.

#### Step 2: Copy the Example Project
There are two ways we can do this, either by the command line, or through the desktop.

#### Step 2 (Desktop Version):
On the virtual macine, open firefox from the start menu.

Then, go to this [link](https://github.com/MURobotics/TemplateDockerGZ) with your firefox browser.

Press the 'Clone' or 'Code' Button and download the zip into your project folder.

Then, right click the donloaded zip to extract the folder.

Lastly, right click the .zip folder to delete it

#### Step 2 (Command Line Version):
First, we will change our directory by running:
``` cd ~/Desktop ```

You should be able to see your project folder listed by running 'ls', this shows the folders in your current directory.
``` ls ```

Next, we'll go into our project folder. Since we called ours 'projects' we will type:
``` cd projects ```

Now, we will copy the example project folder by running:
``` wget https://github.com/MURobotics/TemplateDockerGZ/archive/master.zip ```

With the zip folder installed, we will open it with:
``` unzip master.zip ```

If we look at what's in our desktop project folder, you can see how there is the .zip folder, and our project folder

Then, we can delete the compressed folder by running:
``` rm -rf master.zip ```

#### Step 3: Running the simulation
With our project downloaded, we will need to open up our terminal from the side menu.

Now, we will want to change our folder so we are inside the template folder. To do this we will first want to go into our project folder. For us, our project folder is called 'projects' so to change our directory, we will run ``` cd ~/Desktop/projects/TemplateDockerGZ-master ``` 
(hint: when typing out your directory, you can press the TAB key to auto-complete a directory name after typing a few letters)

Then, to allow our startup script to run, we will type ```chmod +x startup.sh```

Finally, to run our program, we will run ```./startup.sh```

**NOTE:** The first time running this it will take a few minutes to do the initial setup, but re-running this command in the future should only take a few seconds

#### Step 4: Connecting the Simulation Client

## Method 2 (free for non-engineering students): Using Virtual Box Software

## Method 3 (free for non-engineering students, less setup): Using Docker Natively
Throughout these tutorials we'll be developing and testing using these technologies:

### Part 2:

## Bonus Method (best performance, but requires native installation of Ubuntu 18.04 or dual boot): Adding Required Packages for native implementations

### Prerequisite: Have a Ubuntu 18.04 natively installed on your PC as your primary OS or via dual-boot
For this method to be viable, we're expecting that you already have Ubuntu 18.04 installed on your host PC, or you've gone through the process of setting up a dual boot of Ubuntu 18.04 (using [other distributions will vary your experience if attempted](http://wiki.ros.org/melodic#:~:text=Changes-,Platforms,are%20supported%20to%20varying%20degrees.)). If you have little experience with installing a new OS to your computer, or with setting up a dual-boot, we recommend either working with someone who has experience in this, or deferring to another method. As setting up a dual boot or switching your operating systems may result in data-loss if done improperly.



## Report a Bug
If you are experiencing technical difficulties throughout these courses, you may report these on our repository [issues page](https://github.com/MURobotics/GZROS-Software-Tutorials/issues). We'll attempt to keep an active eye on issues that are presented and help provide some guidance to these issues, we want to actively encourage the reporting of issues to better improve the learning experience for everyone. Additionally, if you have any questions regarding the completion of these tutorials, be sure to ask fellow MU Robotic members for any questions or help.

## Next Steps
To continue with the series of tutorials, be sure to select a new branch to change your lesson. Our next section will begin to show how Robot Operating System (ROS) can interact with Gazebo and be used to program movement for a robot. Here is a link to our [tutorials](https://github.com/MURobotics/GZROS-Software-Tutorials/branches/all).
