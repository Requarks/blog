---
categories:
- Tutorials
date: "2017-06-05"
description: The installation script provided by Visual Studio Team Services (VSTS) for Ubuntu 14.04 have no service capabilities and creating one is far from obvious.
image: images/vsts.jpg
slug: start-vsts-agent-as-service-on-ubuntu-14-04
tags:
- tutorials
title: Start VSTS Agent as service on Ubuntu 14.04
---

The installation script provided by Visual Studio Team Services (VSTS) for Ubuntu 14.04 have no service capabilities and creating one is far from obvious.

1. Logged in as root (or sudoer), create a new user:  
	`sudo adduser`
2. Start session with that user *(replace USER with the actual username)*:  
	`sudo -i -u USER`
3. Run the install script provided by VSTS for Ubuntu 14.04 and configure your agent.
4. Upon completion, you should see something like "*Listening for jobs*". At this point, we can kill the process as we want to run it as a service.
5. Exit from the user session:  
	`exit`
6. Create a new file **vsts-agent.conf** under **/etc/init**:  
	`sudo nano /etc/init/vsts-agent.conf`
7. Paste the following content *(replace USER at line 11 and 12 with the username created in step 1)*:

	```
	description "VSTS Agent"
	author      "VSTS"

	start on started mountall
	stop on shutdown

	respawn
	respawn limit 99 5

	script
	        chdir /home/USER/vstsagent
	        exec sudo su USER ./run.sh >> vsts-agent.log 2>&1
	end script
	```

8. Save and close the file.
9. Start the service: `sudo service vsts-agent start`

You now have your VSTS Agent running as a service in the background, like it should be.