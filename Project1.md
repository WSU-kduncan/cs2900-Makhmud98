# Part 1 - Building VMs ( / 4)

## Create a new Virtual Machine ( / 2)
- How much disk space? Fixed or flex?
My Virtual Machine has 2042 Megabytes of data, which is equal to roughly 2 gigabytes. It is fixed, because I specified the memory allocated to the VM. On the other hand, flexible disk space can expand as you add more data to it.

- How much RAM? What about your host?
My Virtual Machine has 27 MB or Ram. While this is horrible, it is enough to run basic video display modules. My host machine has 8 Gigabytes of Video Memory, this allows it to run multiple displays and can outperform the VM by miles.

- 3D acceleration? What performance do you need out of your VM? Do you even have GPU resources to make this really worthwhile?
3D Acceleration is a handy tool that allows the VM to use the hosts video memory to be used. If you plan on doing work on the VM which will exceed 27MB of Ram, for example running multiple displays that use video memory. In my case I do not need that kind of performance from my VM, atleast not yet. I do have enough GPU resources to make this possible, but at this moment there is no need for it.

- Guest Additions - what are you loosing without it, what would you gain with it, and do you want it?
You will not really lose much without Guest additions, but you will gain alot from it. It allows for drivers to be installed to optimize your VM. This could save loads of time if you plan on using the Virtual Machine consistently and is definitley something worth looking into. Do I want it? I need it.

## Install an OS to the Virtual Machine ( / 2)
- How to specify which ISO is the install ISO
Once You start the creation of a new VM, you will be asked to where you want your VM to live in your Hosts system, after specifying it and also specifying the memory that will be allocated to the VM, you will be asked about the Hard Disk of the VM. This is where you can either choose not to add one or create one yourself. Additionally, you can download a default ISO file which can be used as a start to your VM.

- Maybe (for your notes) any installation tips / tricks you did
Make sure you pay attention to the professors lectures!

-  How to detach install ISO once done
Make sure the machine is powered off and the select the settings for the machine. Inside the storage section you can select "Unmount" which will detach the ISO file from the VM.

# Part 2 - Exploring Virtualization ( / 4 )
Exploring Host Disk Usage ( / 2)

- Describe where your Guest OS is saved and how much space it takes up
They are stored inside your VirtualBox (Or Other VM Software) folder which is usually in the Usr/VirtualBox folder; however you can choose to change it. The amount of space it takes is determined by how much memory and data you have inside this VM.

- From your configuration above, is this going to expand?
Depending on your memory allocation of the VM it could expand. However in my VM it will not expand unless I tell it to.

- Can you directly access your Guest files from the virtual machine image folder? Why or why not?
It is possible to allow your VM to be accessed through the Host operating system, this is done by creating shared folders between your VM and your host system.

- Explore the sizes of creating "snapshots" vs. templates / clone. What do each of these achieve?
Snapshots are more of a backup file incase something goes wrong with your VM. While cloning will create a entirely new guest machine which can be run seperately. Snapshots are much smaller files while cloning creates an entirely seperate VM which will take up more space.

Exploring Guest Networking ( / 2)
Understanding of Host networking situation
Understanding of Guest networking situation

# Part 3 - Networking with Style ( / 2)
Pick a networking method besides NAT, and see what it does.
Document the networking configuration you choose.