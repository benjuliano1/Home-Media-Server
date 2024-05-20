# Home Media Server

## Objective

The objective of this project was to set up my own media server using Jellyfin. The primary focus was building confidence setting up my first technical project. The experience helped me to deepen my skills in Linux, system management, access controls, and network configuration.

### Skills Learned

-	Linux set up and administration
-	File system and drive formatting
-	VPN configuration
-	Firewall rules
-	Docker and Github installation/deployment


### Tools Used

-	Zimaboard and CasaOS for server hosting
- Docker and Github for software installation
-	Windows Defender for firewall configuration
-	Diskpart command-line utility for drive formatting
-	Tailscale for secure remote server access via VPN


## Steps
1. The first step was to download Jellyfin via the CasaOS store

<img width="907" alt="1" src="https://github.com/benjuliano1/Home-Media-Server/assets/170282669/e911af4f-63e9-40e0-abf9-5e10e65d4f72">

2. Next, the Zimaboard will need additional storage to host my media. I had a 2TB Western Digital drive laying around that I could reformat to exFat for use with Linux. I accomplished this using the diskpart tool in command prompt.

3. Before plugging the 2TB storage into the Zimaboard, I navigate to Settings on the CasaOS homepage and select the “Auto-mount USB drive” toggle to make sure it is available to Jellyfin when I set up my library.

<img width="958" alt="2" src="https://github.com/benjuliano1/Home-Media-Server/assets/170282669/5ea9955b-f4c2-48de-80fb-f68728ded87a">

4. After plugging in the drive, we can see it's recognized in the left-hand panel.

<img width="959" alt="3" src="https://github.com/benjuliano1/Home-Media-Server/assets/170282669/330f0f44-142d-4242-9c1b-d5f62537ff52">

5. The next step is to create folders in the drive that Jellyfin can use as libraries for my content. You can see I’ve created “Movies” and “Kids’ Movies” so far.

<img width="956" alt="4" src="https://github.com/benjuliano1/Home-Media-Server/assets/170282669/eb9a29ee-7756-4258-b8db-122c000de9e8">

6. Jellyfin needs access to these new folders to create libraries. To do this, I return to the CasaOS homepage, go to the Jellyfin context menu, click “Settings” , and paste the paths to the new folders under the “Volumes” section. Now, Jellyfin will be able to access my media.

<img width="955" alt="5" src="https://github.com/benjuliano1/Home-Media-Server/assets/170282669/65a81a8f-d322-48df-90c0-7ecdf66bf913">

7. To connect to the newly set-up server on the client side, I sidedloaded the Jellyfin app on my Samsung Smart TV using an amazing Docker container by Georift.

<img width="929" alt="6" src="https://github.com/benjuliano1/Home-Media-Server/assets/170282669/b6d5fdc3-8dc7-4aff-be01-64de317344dd">

8. To get the IP to my new server, we return to CasaOS, open the terminal, and run the command “hostname -I”.

<img width="584" alt="7" src="https://github.com/benjuliano1/Home-Media-Server/assets/170282669/f5219fb8-ce69-4e35-8c08-6162b64525f7">

9. Once I enter the resulting IP on my Jellyfin client, we’re all set! Later, I configured access outside my network using Tailscale. You can see a picture of my Tailscale dashboard below.

<img width="957" alt="8" src="https://github.com/benjuliano1/Home-Media-Server/assets/170282669/934f72ad-78f2-4939-8fc1-e73c9e2499b3">




 


