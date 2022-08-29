# Day 5 of #100daysofcloud

### I worked and managed more with Linux process using different commands and continue my Terraform with AWS project

- I used a series of commands to manage processes (pgrep, top, htop, fg, bg, sleep ctrl+z, ctrl+c, kill, pkill etc)

- I learned how to run a process in the background (with & symbol) and foreground

- I use the kill command and its various signals

- I used kill -l to see all types of available kill signals like (9 - SIGKILL, 15 - SIGTERM default), 2 - SIGINT/ctrt+c, 19 - SIGSTOP/ctrl+z, etc)

- I deployed AWS EC2 instnce using terraform.

- I used datasources.tf to create an AMI for the EC2 instance

- I used userdata.tpl to create a startup actions (user data code) for the EC2 instance during initial boot where required software are installed and updated

- I generated an asymmetric "ed25519" keypair type to remotely login into the EC2 instance via ssh

- After more research, I finally settle for Cloud Academy as my cloud learning platform. All suggestions and recommendations are still welcomed in the comment section below.

#linux #linuxsystemadministration #terraform #cloudcomputing #learninpublic
