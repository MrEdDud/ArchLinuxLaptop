# linux-laptop

Why did I do this? 
Basically no reason. I saw a video showcasing Arch Linux, and I thought to myself, I want that, so here we are.

What did I learn by doing this?
Crucial Linux skills and patience.

### **28th April 2025**
I started by going to the Arch Linux installation guide *(https://wiki.archlinux.org/title/Installation_guide)* where I started to read the installation process. I got the download file and used balenaEtcher to put it into a spare SSD I had. Now you may be thinking, why did I put it on an SSD? It's because I couldn't find a USB stick in my house.

I inserted the SSD into the laptop, and after tinkering with the boot options, I was greeted with the CLI of Arch Linux. Now, because I was hasty, I didn't read the next step, where it says to check the signature to check if it's malware, so I checked the signature by looking at the SHA256 code on the website and my own, and they were identical. I checked the SHA256 of my installed file by doing "certutil -hashfile /path/to/file SHA256" on my Windows PC, and it worked.

Next, I connected to the wifi using iwd (my laptop does not have a LAN cable port), changed the font using "setfont ter-132b" and then, after doing some other random useless commands, I started partitioning by doing "fdisk -l" to see the disk name. Then, after getting confused by the table the website shows you and getting confused by the windows partitions that were previously on my laptop and after asking ChatGPT for even more help, I was able to make the 3 partitions that are needed, the boot, swap and root partitions. At this part of the process, the command "lsblk" became very useful to me so that I can check that I'm doing everything correctly.
