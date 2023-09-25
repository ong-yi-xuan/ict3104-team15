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
pip3 install jupyter
```
