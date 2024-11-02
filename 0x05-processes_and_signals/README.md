# Processes and Signals

A collection of Bash scripts and C programs demonstrating process management and signal handling in Linux.

## Description

This project contains scripts that handle:
- Process identification (PID)
- Process listing
- Signal handling
- Daemon processes
- Zombie processes

## Scripts

* `0-what-is-my-pid` - Displays its own PID
* `1-list_your_processes` - Displays a list of currently running processes
* `2-show_your_bash_pid` - Displays lines containing the bash word
* `3-show_your_bash_pid_made_easy` - Displays the PID of processes containing "bash"
* `4-to_infinity_and_beyond` - Displays "To infinity and beyond" indefinitely
* `5-dont_stop_me_now` - Stops 4-to_infinity_and_beyond process
* `6-stop_me_if_you_can` - Stops 4-to_infinity_and_beyond process without kill
* `7-highlander` - Displays "To infinity and beyond" with sleep 2
* `8-beheaded_process` - Kills the process 7-highlander

### Advanced Tasks
* `100-process_and_pid_file` - Creates PID file and handles multiple signals
* `101-manage_my_process` - Init script to manage daemon processes
* `102-zombie.c` - C program that creates 5 zombie processes

## Environment
* Ubuntu 20.04 LTS
* Bash
* shellcheck version 0.7.0

## Author
Shighi
