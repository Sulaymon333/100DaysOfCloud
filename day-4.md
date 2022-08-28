# Day 4 of #100daysofcloud

### I did some daemon hunting in Linux and I continued with my Terraform with AWS project

- I learned systemd is the service manager for all services/daemons in Linux and it is the first init process to start, which later fork to start other daemons/processes

- To interact/manage different daemons/units via systemd, I used systemctl command with arguments like start, stop, status, restart, reload, reload-or-restart, disable, enable, is-enabled, is-active, list-units, list-units --all, list-unit-files, and so on

- There are many other types of daemons in Linux. Some of them are device, mount, socket, target, timers, etc

- I learned about journalctl (log for systemd activities), and how to restart it with sudo systemctl restart systemd-journald command, I used a couple of flags with journalctl (-xe, -f, -k, -n, --since, -r, --version, --help etc)

- I worked with ps command with appropriate flags like -aux and grep command to narrow down the specific process ( instance of a program I am interested in). I used pgrep as well.

- I created and manage more aws resources (vpc, subnet, internet gateway, route table, route table assoc., and security group) using terraform commands from the CLI

- I am still researching the best platform to use for a structured learning for my cloud journey and cloud certifications. I discovereed main two options (A Cloud Guru | A Pluralsight Company and Cloud Academy). I am considering Cloud Academy since they seems to have richer content. All suggestions and recommendations are welcomed in the comment section below.

#linux #linuxsystemadministration #terraform #cloudcomputing #learninpublic
