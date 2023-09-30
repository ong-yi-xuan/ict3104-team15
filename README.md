# ict3104-team15

## Clone Repository
### Using Github Desktop
1. Launch Github Desktop
2. Click File > Clone Repository
3. Select URL and input the repository URL (https://github.com/ong-yi-xuan/ict3104-team15) as follows:
4. Click Clone
5. Repository should be successfully cloned into your provided folder

![Step-By-Step Clone Repo](https://github.com/ong-yi-xuan/ict3104-team15/assets/91550661/5e8dd643-e974-43a6-8ab9-be2f2785d92a)
![Input Github Repo URL](https://github.com/ong-yi-xuan/ict3104-team15/assets/91550661/ec031e2a-0689-4212-8742-d05fce9568b6)


## Environment Setup
The Triton library (https://github.com/triton-inference-server/client) used in this project only works in Linux environments. This section details how to run the jupyter notebook from the cloned repository.

<details>
  <summary><h3>Linux</h3></summary>
   1. Install Python3 and Jupyter
   ```
   sudo apt update && sudo apt upgrade
   sudo apt install python3.8 python3-pip
   python3 -m pip install --upgrade pip
   pip3 install jupyter
   ```
   
   2. Locate cloned repository folder and navigate to it in the terminal
   ```
   cd /<folder-to-repository>/ict3104-team15/
   ```
   
   3. Install required dependencies from requirements.txt
   ```
   pip3 install -r requirements.txt
   ```
   
   4. Upgrade Jupyter to ensure compatibility with installed dependencies 
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
   
   Save the file and exit. Then, source the file to apply our changes:
   ```
   source ~/.bashrc
   ```
</details>
      
<details>
  <summary><h3>Windows (via WSL2)</h3></summary>
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
   ![Add Jupyter to PATH](https://github.com/ong-yi-xuan/ict3104-team15/assets/91550661/a6b5607f-4fee-4d6c-89f5-ab2b8b98cb5f)
   
   
   Save the file and exit. Then, source the file to apply our changes:
   ```
   source ~/.bashrc
   ```
</details>

<details>
  <summary><h3>Windows/MacOS (via Google Colab)</h3></summary>
   
   1. Go to the Google Colab website: https://colab.research.google.com/
   
   2. Click on the Upload tab in the pop-up dialogue.
   
   3. Click on the Choose File button and navigate to the cloned repository folder where your Jupyter notebook is located and select it.
   
   4. Wait for the notebook to upload. Once uploaded, it will open in a new tab.
   ![Upload Jupyter Notebook to Google Colab](https://github.com/ong-yi-xuan/ict3104-team15/assets/91550661/37f72d8e-5aec-427a-b062-be8203f0015b)
   ![Jupyter File Successfully Uploaded on Google Colab](https://github.com/ong-yi-xuan/ict3104-team15/assets/91550661/2633d186-1d76-48b2-bed9-9b66c35eef02)
   
   5. Change the runtime type setting under "Runtime" > "Change runtime type" to the following:

      Runtime type: Python 3
      
      Hardware accelerator: T4 GPU
      
      ![Change Runtime Type](https://github.com/ong-yi-xuan/ict3104-team15/assets/91550661/2f22d1b3-e47e-4252-921f-81c454776fea)


   7. Downgrade Python version to 3.8 using the provided commands:
    ```
    # Downgrade Python by reinstalling pip and distutils
    !apt-get install python3.8 python3-pip python3.8-distutils
    !update-alternatives --install /usr/local/bin/python3 python3 /usr/bin/python3.8 1
    
    # Check the result
    !python --version
    ```
    
   7. Run the next cell to create button to upload requirements.txt
   ```
   from google.colab import files
   uploaded = files.upload()
   ```
   
   8. This will give you a button to "Choose Files." Click on it and select the requirements.txt file.
   ![Choose File](https://github.com/ong-yi-xuan/ict3104-team15/assets/91550661/73dd952c-bd36-41db-a104-8c22468c4a40)
   ![Requirements.txt Uploaded](https://github.com/ong-yi-xuan/ict3104-team15/assets/91550661/275bfad6-584d-4a5c-be26-59dbaa570663)
   
   9. After uploading the requirements.txt file, you can install the packages specified in that file. Run the next cell:
   ```
   !python -m pip install -r requirements.txt
   ```
      
</details>

## Running Jupyter Notebook
<details>
  <summary><h3>Linux</h3></summary>
   
1. Locate cloned repository folder and navigate to it in the terminal
   ```
   cd /<folder-to-repository>/ict3104-team15/
   ```

2. Launch the Jupyter notebook
   ```
   jupyter notebook
   ```

3. Jupyter notebook should be opened successfully in a new page on your default web browser.
   
</details>

<details>
  <summary><h3>Windows (via WSL2)</h3></summary>
      
   1. Navigate to the repository folder in WSL terminal and replace <drive> and <folder-to-repository> as per your setup
   ```
   cd /mnt/<drive>/<folder-to-repository>/ict3104-team15/
   ```
   
   3. Launch the Jupyter notebook
   ```
   jupyter notebook --no-browser --ip=127.0.0.1
   ```
   
   4. A URL to the Jupyter notebook should be generated in the format http://127.0.0.1:8888/tree?token=<token-string>.

   ![Jupyter Notebook URL](https://github.com/ong-yi-xuan/ict3104-team15/assets/91550661/0cb046b4-6ee9-4c52-b926-ce357927eda9)
   
   5. Copy the URL and paste it into the browser of your choice
   
   ![Notebook Preview](https://github.com/ong-yi-xuan/ict3104-team15/assets/91550661/6d0b1422-b0e8-42f8-8587-5c2daa0ce815)
   
   6. Double click on ict3104-team15.ipynb to launch the notebook
</details>

<details>
  <summary><h3>Windows/MacOS (via Google Colab)</h3></summary>
      
   1. Navigte to your Google Drive and open the uploaded Jupyter notebook
   2. Press the "Run" button beside each cell to run the code/commands
      
</details>
