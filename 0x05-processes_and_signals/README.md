# Processes and signals

In this project, I learned about handling process ID's and signals in Bash with `ps`, `pgrep`, `pkill`, `pkill`, `exit`, and `trap`.

## Tasks :page_with_curl:

* **0. What is my PID**
  * [0-what-is-my-pid](./0-what-is-my-pid): Bash script that displays its own PID.

* **1. List your processes**
  * [1-list_your_processes](./1-list_your_processes): Bash script that displays a list of currently running processes.
  * Shows all processes for all users, including those not featuring a TTY.
  * Processes are displayed in a user-oriented hierarchy.

* **2. Show your Bash PID**
  * [2-show_your_bash_pid](./2-show_your_bash_pid): Bash script that displays lines containing the `bash` keyword based on the script defined in `1-list_your_processes`.

* **3. Show your Bash PID made easy**
  * [3-show_your_bash_pid_made_easy](./3-show_your_bash_pid_made_easy): Bash script that displays the PID along with the process name of processes who name contains the word `bash`.

* **4. To infinity and beyond**
  * [4-to_infinity_and_beyond](./4-to_infinity_and_beyond): Bash script that displays `To infinity and beyond` indefinitely with a `sleep 2` in between each iteration.

* **5. Don't stop me now!**
  * [5-dont_stop_me_now](./5-dont_stop_me_now): Bash script that kills the [4-to_infinity_and_beyond](./4-to_infinity_and_beyond) process using `kill`.

* **6. Stop me if you can**
  * [6-stop_me_if_you_can](./6-stop_me_if_you_can): Bash script that kills the [4-to_infinity_and_beyond](./4-to_infinity_and_beyond) process using `pkill`.

* **7. Highlander**
  * [7-highlander](./7-highlander): Bash script that displays `To infinity and beyond` indefinitely with a `sleep 2` in between each iteration.
  * Displays `I am invincible!!!` upon receiving a `SIGTERM` signal.


* **8. Beheaded process**
  * [8-beheaded_process](./8-beheaded_process): Bash script that kills the process [7-highlander](./7-highlander).


![alt text](https://s3.amazonaws.com/alx-intranet.hbtn.io/uploads/medias/2020/9/d8ecfe9109334898b9540ffd20cf64d1c06f0c09.jpg?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIARDDGGGOUSBVO6H7D%2F20220722%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20220722T101619Z&X-Amz-Expires=86400&X-Amz-SignedHeaders=host&X-Amz-Signature=8831f4931db87fcebcbad63936313cf1ea4a070d0d73bc8ba8531a85eb862046)

* **9. Process and PID file**
  * [100-process_and_pid_file](./100-process_and_pid_file): Bash script that creates the file `/var/run/myscript.pid` containing its PID and displays `To infinity and beyond` indefinitely.
  * Displays `I hate the kill command` upon receiving a `SIGTERM` signal.
  * Displays `Y U no love me?!` upon receiving a `SIGINT` signal.
  * Deletes the file `/var/run/myscript.pid` and terminates itself upon receiving the `SIGQUIT` or `SIGTERM` signal.


![](https://s3.amazonaws.com/alx-intranet.hbtn.io/uploads/medias/2020/9/37975393ead381f4d27f268f7337c6d3013b4991.jpg?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIARDDGGGOUSBVO6H7D%2F20220722%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20220722T101619Z&X-Amz-Expires=86400&X-Amz-SignedHeaders=host&X-Amz-Signature=ad4edea7cdd7ecaaa7ab06f0cb40c5b269a1c2777a349c54587445b68ff1c304)

* **10. Manage my process**
  * [manage_my_process](./manage_my_process): Bash script that writes `I am alive!` to the file `/tmp/my_process` indefinitely.
    * Sleeps two seconds in between each write.
  * [101-manage_my_process](./101-manage_my_process): Bash script that manages the [manage_my_process](./manage_my_process) script.
  * When passed the argument `start`:
    * Starts [manage_my_process](./manage_my_process).
    * Creates a file containing its PID in `/var/run/my_process.pid`.
    * Displays `manage_my_process started`.
  * When passed the argument `stop`:
    * Stops [manage_my_process](./manage_my_process).
    * Deletes the file `/var/run/my_process.pid`.
    * Displays `manage_my_process stopped`.
  * When passed the argument `restart`:
    * Stops [manage_my_process](./manage_my_process).
    * Deletes the file `/var/run/my_process.pid`.
    * Starts `manage_my_process`.
    * Creates a file containing its PID in `/var/run/my_process.pid`.
    * Displays `manage_my_process started`.
  * Otherwise, displays `Usage: manage_my_process {start|stop|restart}`.


![alt text](https://s3.amazonaws.com/intranet-projects-files/holbertonschool-sysadmin_devops/255/C6mO7b3.jpg)

* **11. Zombie**
  * [102-zombie.c](./102-zombie.c): C program that creates five zombie processes.
  * For every zombie created, displays `Zombie process created, PID: <ZOMBIE_PID>`.
