```
sudo apt update
sudo apt install python2.7 python-pip 
readlink -f $(which python) | xargs -I % sh -c 'echo -n "%: "; % -V'#check the version of python on Ubuntu
git clone -b release_17.09 https://github.com/galaxyproject/galaxy.git
sh /home/yilinxia/galaxy/run.sh #the folder you clone to
http://localhost:8080/or <u>http://127.0.0.1:8080/   # homepage of the galaxy in local PC
use Ctrl+c to terminate the terminal to stop the server
```
