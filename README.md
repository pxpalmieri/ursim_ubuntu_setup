## OFFLINE SIMULATOR - CB3 - URSIM-3.15.0 - Installation Guide on Ubuntu 20.04 LTS

This page describes how to have Ursim running in Ubuntu 20.04 LTS.
The latest Ursim could be downloaded from [here](https://www.universal-robots.com/download/software-cb-series/simulator-linux/offline-simulator-cb3-linux-ursim-3150/). Unzip the files using
```
tar -xvf filename.tar
```

### Installing Ursim:

1. You need Java 8 to run Ursim. Update the repositories with
    ```
    sudo apt-get update
    ```
    and install Java 8 with
    ```
    sudo apt-get install openjdk-8-jdk
    ```
2. Make sure the system is sourcing or using java8. This can be done by:
    -   Find the version of java that is running or sourced by
        `java -version`
    -   if there are multiple version use: `sudo update-alternatives --config java`
    -   select the version to be jdk 8.


3. Change the line 70, in ```install.sh``` file to replace
  ```libcurl3``` to ```libcurl4```. A sample file could be found in the repo.

4. Run the following lines to make files executable
```
sudo chmod +x start-ursim.sh
sudo chmod +x starturcontrol.sh
sudo chmod +x stopurcontrol.sh
sudo chmod +x URControl
```

5. Run in the terminal ```bash install.sh``` or ```./install.sh``` from the unzipped folder.

### Running Ursim:
Run ```bash start-ursim.sh``` or ```./start-ursim.sh``` from the unzipped file directory system.
