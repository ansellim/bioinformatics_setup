# bioinformatics_setup

Installation instructions for a VirtualBox Virtual Machine

# System requirements

* Any modern computer capable of running virtualization software.

* You should have more than 16 GB of RAM. Since virtualization software runs with overhead, it's probably good to have >24GB of RAM.

* Your BIOS settings must support virtualization. Secure boot or other UEFI settings may interfere with virtualization. If you don't know what I'm talking about, then don't worry...you probably won't have a problem.

# Installation instructions

1. Download and install the latest version of VirtualBox.

https://www.virtualbox.org/wiki/Downloads

2. Download the Virtual Machine image ("Virtual Appliance") from my Google Drive folder. It's the OVA file located in this folder: [https://drive.google.com/drive/folders/1VENAR4U5u7AtyVfpTDjy-1svyA7QWKZ2?usp=sharing](https://drive.google.com/drive/folders/1VENAR4U5u7AtyVfpTDjy-1svyA7QWKZ2?usp=sharing)

This contains an image of Ubuntu 22.04 LTS with all the preinstalled bioinformatics software required for running SARS-CoV-2 genomics analysis according to the EQA workshop.

3. Import the Virtual Appliance.

When importing the Virtual Appliance, you may change the number of virtual CPUs and the amount of RAM you wish to "allocate" to the virtual machine. By default, I have configured the virtual machine to run with 8 vCPUs and 16GB of RAM. If your physical machine has room to run a more powerful virtual machine, then please go ahead.

4. You are good to go!

* The default password for user is "genomics9800".
* In the home folder, you can find a folder called "eqa_practical" which you can work with.
* I have already created some scripts in the "scripts" subfolder which are based on the work I did following the tutorial ([https://cambiotraining.github.io/sars-cov-2-genomics/08-case_study_eqa.html](https://cambiotraining.github.io/sars-cov-2-genomics/08-case_study_eqa.html)) during the EQA workshop.
* A copy of this folder WITHOUT output/results/analysis has also been created -- look for "eqa_practical_Blank_With_Data". You can use this folder to experiment and to practice the tutorial exercises.
* Note: If you run into memory problems, consider changing the memory allocated to the VM, or changing the max memory usage in the viralRecon.sh script.
