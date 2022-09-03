Day 7 of #100daysofcloud

I learned shortcuts for working around the terminal, I completed my project on using Terraform with AWS and continued studying for my AWS SAA-C03 certification

- I learnt a number of cool commands and shortcuts like (cd -, sudo !!, !<cmd>, ctrl/cmd + ⇦ or ⇨, ctrl+e, ctrl+a, ctrl+k, ctrl+y, ctrl+w, ctrl+r, ctrl+x+e, tail/head, less vs cat)

  - cd - will change directory to the previous one

  - sudo !! will run the last command with sudo

  - !<cmd>, !cd for example will run the last cd command

  - ctrl/cmd + left or right arrow will skip through words

  - ctrl + e will move the cursor to the end of the line

  - ctrl + a will move the cursor to the beginning of the line

  - ctrl + k will delete everything after the cursor

  - ctrl + u will delete everything before the cursor

  - ctrl + y will paste deleted items

  - ctrl + w will delete the last word before the cursor

  - ctrl + r will reverse search all previous commands

  - ctrl + x + e will open the current command in a default text editor like vim, nano, or less, and run after you are done with the command

  - tail/head show last/first 10 lines from a file, use -n for specific lines and for tail only -f for follow mode

  - cat vs less, the cat will display the content of file in standard output (stdout) stream while less will load only a part of a file at a time making it suitable for big files like logs and so on

- I worked with Terraform variables (with string interpolation)

  - I used variables.tf file to store a repeated value which must be supplied when running terraform plan, apply or destroy for example. Using default values will make automation smoother

  - I used terraform.tfvars to override the variable value specified in variables.tf file

  - I used terraform console -var="host_name=value" to overide the variable value in terraform.tfvars

  - I used Terraform console -var-file="prod.tfvars" to reference the value defined in prod.tfvars and as a result making it take precedence over terraform.tfvars

- I worked with conditionals in Terraform

- I worked with Terraform output for logging important info to the terminal

- I used terraform -refresh-only to apply the latest changes without destroying the current infrastructure

- I studied AWS compute EC2 resources on Cloud Academy.

GitHub link for Terraform project with AWS - https://github.com/Sulaymon333/terraform-with-aws

#linux #linuxsystemadministration #terraform #cloudcomputing #learninpublic
