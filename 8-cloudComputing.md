#Cloud Computing

## Why use cloud servers?
+ Ideological reason: centralized information is exploitable, as we have discussed in class! 
	+ To be fair, most cloud services are provided in a centralized way, but it is still more independent.
+ Utilitarian reason: free up local processor resources

## Amazon Web Services (AWS)
+ This is the name of the cloud service we will be using
+ Cloud: a collection of services (storage, processing power, etc)
+ You can rent a little time on a 'raw' computer, attach 'blocks' (like little harddrives), and do whatever you want! 
+ There is flexibility in what you do on the machine, but that means you are also responsible for doing what you want with it (no one will hold your hand!)
+ There is a lot of potential here: many companies even run on this. (That is also why security is so difficult).
+ First... what is a "server"?
	+ The easy answer: a computer that serves stuff.
	+ They also tend to be connected to the Internet (to serve information)
	+ And they are constantly available.

## Getting started
+ First, you need to set up an Amazon AWS account. It's non-trivial. You can access it [here](aws.amazon.com).
+ Once you are logged in, you will go to the Amazon Web Services main page, listing the services that are available.
+ We will mainly use EC2 and IAM (which is security for the Amazon Services panel)
+ Before getting too far, look for the location in the upper right hand corner. Make sure it's pretty close--even though this is the Internet, it will affect your connection speed.

## EC2
+ Click on the EC2 logo to go to your main EC2 dashboard.
+ Check out the left hand panel. We'll walk through those.

###Instance
+ An "instance" is a server in the cloud. Click this to get to the instances.

###Images
+ This is like a blank tablet for a computer. When you install operating systems, they come in "images."

###Elastic Blocks
+ In the physical world, this is a harddrive (or volume).

###Snapshots
+ Once you have a block, you can take "snapshots" of the harddrive, which are stored in Amazon's long-term storage (Glacier) for cheap.

###Key Pairs
+ Hey! We learned about those in the cypherpunk week!

##Launching a server
+ Click on "Instances" in the left hand panel
+ Click "Launch Instance"
+ Now, you select an Image. We picked a Debian AMI from the Marketplace.
+ Then, configure instance details. Most stuff can be left on the default. But pick the availability zone and stick with one!
+ Next: Add Storage. When you configure an instance, you get a tiny little drive (8GB). You may want more space on the main drive, or you may want an external volume. But we'll leave it for now.
+ Next: Tag. Pick a name for your server! Just make it intuitive.
+ Next: Security Group. 
	+ A little lesson. Your computer's internet connection has lots of little ports. By default, they are all closed. So what we need to do is open at least one port, so that you can get in! Each port is specifically for some purpose (SSH, etc)
+ Click "Launch." You will then be asked to make a new key pair. Name it, and you will download it. Drop it in ~/.ssh/ on a Mac.
+ Now, don't click past the confirmation screen! Open "Usage Instructions." Think about it: you need to figure out how to log in for the first time! Copy and paste it for later use:
	+ "You must use an SSH client to access this instance, authenticating with your SSH key as the user 'admin'; you may then use 'sudo -i' to gain root (administrator) privileges."
+ Then you can return to the homepage.