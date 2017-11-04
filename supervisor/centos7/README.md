# Description
Docker image based on CentOS 7 with supervisord as the PID 1 
SSH server is started as a supervisord service and uses *Vagrant*'s default insecure key to login using user vagrant

# Motivation
This image was created to be a replacement for a Vagrant VM, specially if you rely on *Ansible* for configuration (as it enables SSH server) and *supervisord* for service management. However I don't advise to use it outside dev environemnt.

# Features
- Enable container to run multiple services through *supervisord*
- Start SSH server to be connectable from *Vagrant* with user and insecure_key configured
- Avoid zombie reaping problem (https://blog.phusion.nl/2015/01/20/docker-and-the-pid-1-zombie-reaping-problem/)

# Usage
If you are using *Vagrant*, change your *Vagrantfile* provider to docker
If you are interested only on the *supervisor*, start it as any other container.

# More Info
For source code please visit my github.com page

