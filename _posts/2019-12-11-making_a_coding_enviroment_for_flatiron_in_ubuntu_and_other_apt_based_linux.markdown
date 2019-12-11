---
layout: post
title:      "Making a coding enviroment for flatiron in Ubuntu and other apt based linux"
date:       2019-12-11 01:59:23 -0500
permalink:  making_a_coding_enviroment_for_flatiron_in_ubuntu_and_other_apt_based_linux
---


Recently I was trying to find a coding set up guide for linux. I ended up asking in the slack channel and got only 1 result an pretty out of date result. But at least it got me halfway and I was able to google my way through the rest.  But I didn't want to leave other linux users in the same boat I was so here is a guide on setting up your coding enviroment in Ubuntu and other apt based linux systems.

First step is to prep your system.  Run the following command in your terminal.

` $ sudo apt-get update `

The next part is to install Gnupg2.  First check if its installed by running this command: `gnupg --version`.  If it isn't installed run:
` $ sudo apt-get install gnupg2`

And now the same with Curl first run :`curl --version` to see if its installed and then run if it isn't: 
`$ sudo apt-get install curl`

I recommend installing the following things before getting to ruby as (at the time of writing this they will be required/helpful in later labs (depending on when you are doing all this) 

`sudo apt-get install sqlite`
`sudo apt-get install sqlitebrowser`

Now we need to actually install Ruby and half of why this guide is in existance is this part because it can be such a pain.  IF at any point this guide doesn't work for you please visit the RVM site at https://rvm.io/rvm/install.  run:

`$ gpg2 --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB`
`$ \curl -sSL https://get.rvm.io | bash -s stable` 
`$ sudo apt install ruby`

And now ruby is installed.  So what is left is a few required gems (atleast for flatiron and installing our IDE)

install the following gems
`gem install rails` and `gem install bundler`

Now all that is left is to set up learn first run `gem install learn-co` and now run `learn whoami`.  At this point it will ask you for an OAuth token to find this go to your profile on learn ans scroll all the way down.  copy that and past it in the terminal and press enter.

Now that that is done we have to get our system to talk to github.  We have to generate a SSH key. run the following command editing your email in  `ssh-keygen -t rsa -b 4096 -C "your_email@example.com"` it will ask you where to save it and I recommend just leaving it defualt.  you will thn be asked about a passphrase this is optional and can be skipped by just hitting enter. Now it is created all you have to do is open the id_rsa.pub file.  For this open files and enable "show hidden files" and navigate into `home/.ssh/` and open the id_rsa.pub in a text editor.  copy the contents and go to your github page.  Navigate to your setting and "SSH and GPG keys".  Now click add "New SSH key" and paste the contents in the key area and give it a name so you know what it is.

From here download and use whatever IDE you wish but if you don't have one selected I highly recommend Visual Studio Code.  it is a good all round IDE and can due every coding language out there. 


CONGRATS your local enviroment is all set up

