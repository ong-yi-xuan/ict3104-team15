# ict3104-team15

## Clone Repository
### Using Github Desktop
1. Launch Github Desktop
2. Click File > Clone Repository

![01 - clone repo](https://github.com/ong-yi-xuan/ict3104-team15/assets/91550661/5e8dd643-e974-43a6-8ab9-be2f2785d92a)


3. Select URL and input the repository URL (https://github.com/ong-yi-xuan/ict3104-team15) as follows:

![02 - github url](https://github.com/ong-yi-xuan/ict3104-team15/assets/91550661/ec031e2a-0689-4212-8742-d05fce9568b6)

4. Click Clone
5. Repository should be successfully cloned into your provided folder
   
## Environment Setup
The Triton library (https://github.com/triton-inference-server/client) used in this project only works in Linux environments. This section details how to run the jupyter notebook from the cloned repository.

### Windows
To run this project on Windows, Windows Subsystem for Linux 2 (WSL 2) will be needed.

1. Open Microsoft Store, search for Ubuntu 20.04 and click Get.

![01 - install ubuntu](https://github.com/ong-yi-xuan/ict3104-team15/assets/91550661/764583ca-ed85-48f9-b655-0fee645212ee)


2. Once the installation is complete, open Windows Start Menu, search for Ubuntu 20.04 and double click to open.

![02 - search ubuntu](https://github.com/ong-yi-xuan/ict3104-team15/assets/91550661/c70c38a2-dca5-46c7-aac1-2ccae79e42cc)


3. A command prompt window should open up as follows. Wait a few minutes for installation to complete.

![03 - command prompt](https://github.com/ong-yi-xuan/ict3104-team15/assets/91550661/99baa5eb-fcbc-4275-b3fc-c7e6309f3628)

4. Configure your username and password.

![04 - set username and pwd](https://github.com/ong-yi-xuan/ict3104-team15/assets/91550661/cab434dd-b971-4d21-8e6a-1a86117dc462)

5. WSL has been installed succesfully.

![05 - installation complete](https://github.com/ong-yi-xuan/ict3104-team15/assets/91550661/ce16bc86-cc80-45f4-bca7-30bd7588c0aa)

6. Ensure the correct version of WSL is used by opening command prompt and running the below command:
```
wsl -l -v
```
![06 - wsl version](https://github.com/ong-yi-xuan/ict3104-team15/assets/91550661/3aff7af9-9d0d-4bfc-a8f7-3b85e20007b1)


7.  Install Python3 and Jupyter on WSL terminal
```
sudo apt update && sudo apt upgrade
sudo apt install python3.8 python3-pip
python3 -m pip install --upgrade pip
pip3 install jupyter
```

8. Locate cloned repository folder in WSL and navigate to it in the WSL terminal
WSL mounts Windows drives under the /mnt/ directory. So, for example:
- C:\ in Windows is available as /mnt/c/ in WSL
- D:\ in Windows is available as /mnt/d/ in WSL

```
cd /mnt/<drive>/<folder-to-repository>/ict3104-team15/
```

9. Install required dependencies from requirements.txt
```
pip3 install -r requirements.txt
```

10. Upgrade Jupyter to ensure compatibility with installed dependencies 
```
pip3 install -U jupyter
```
   
11. Add jupyter command to PATH. First open ~/.bashrc in a text editor:
```
nano ~/.bashrc
```

At the end of the file, add this line
```
export PATH=$PATH:/home/user/.local/bin
```
![07 - add jupyter to path](https://github.com/ong-yi-xuan/ict3104-team15/assets/91550661/a6b5607f-4fee-4d6c-89f5-ab2b8b98cb5f)


Save the file and exit. Then, source the file to apply our changes:
```
source ~/.bashrc
```


## Running Jupyter Notebook
### Windows
1. Navigate to the repository folder in WSL terminal and replace <drive> and <folder-to-repository> as per your setup
```
cd /mnt/<drive>/<folder-to-repository>/ict3104-team15/
```

3. Launch the Jupyter notebook
```
jupyter notebook --no-browser --ip=127.0.0.1
```

4. A URL to the Jupyter notebook should be generated in the format http://127.0.0.1:8888/tree?token=<token-string>.

![01 - generated urls](https://github.com/ong-yi-xuan/ict3104-team15/assets/91550661/0cb046b4-6ee9-4c52-b926-ce357927eda9)

5. Copy the URL and paste it into the browser of your choice

![02 - notebook](https://github.com/ong-yi-xuan/ict3104-team15/assets/91550661/6d0b1422-b0e8-42f8-8587-5c2daa0ce815)

6. Double click on ict3104-team15.ipynb to launch the notebook


