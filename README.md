# hazelvagrant
maintains a vagrant file that describes a virtual machine with the various artifacts set up

To use this repo, first install vagrant on your machine from https://www.vagrantup.com/. Then clone the repo to your machine, `cd` into the created directory and run `vagrant up`. This will take a while and use a fair amount of disk space. When it finishes, you can run `vagrant ssh` in the same directory to log in to the guest machine. The home directory will have copies of both branches of the POPL Agda repo, and Agda will have been run on all the files to demonstrate that they load cleanly.
