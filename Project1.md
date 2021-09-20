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

## Exploring Guest Networking ( / 2)

- Explain your approximate networking configuration for your Host  

My host's network is conducted by a physical router which contains data in packets. The router analyzes the data and determines which is the ebst way for the data to reach the finish line. My hosts IP is a unique number assigned to each device connected to a network which it uses for communication. The IP finds the device host network and the location of it. This IP is also used as a header when sending information from one IP to the destination. The IP can distinguish the device by the port that it is connected to, a good example of this was that the IP address is the hotel and the ports are the rooms inside the hotel.  


- Explain the network configuration for your Guest  

The guest network is connected to the host, it will receive the same Mac address and be apart of the same IP address. The guest network IP address will be obtained by the DHCP service which is a built in service of most if not all virtual machine emulators. If your guest VM uses a NAT networking type, then it will use the physical network of the host as an external network to allow connection to the Internet.

## Part 3 - Networking with Style
- Pick a networking method besides NAT, and see what it does.  

I picked 'bridge network' and first thing I did was test out the network speed to see if it can remotely come close to the host network speed. However after waiting about 2 minutes for the speed test website to load I could only assume the worst. I also noticed that my IP address specified by the speed test website was the same as my VM box IP address.

Document the networking configuration you choose.  
Network Type : Bridged Network
Adapter Type | Intel PRO/1000 MT  
Promiscous Mode | DENY  
Mac Address | CREATED  
Cable Connection | Checked  
