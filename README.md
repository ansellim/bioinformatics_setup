# About

Simple installation instructions for an Ubuntu 22.04 Virtual Machine running on VirtualBox which allows a user to run bioinformatics analyses in a virtual environment. This means that your bioinformatics analysis is "containerized" -- and minimal setup is required. Furthermore, you can replicate your setup easily across all the machines you have in your laboratory, by simply "rinsing and repeating".

Time required: Less than 30 minutes.

Author: Ansel Lim (ansellim@gmail.com).

# System requirements

* Any modern computing machine capable of running virtualization software. Windows, Mac, Linux...it's all OK.

* You should have more than 16 GB of RAM to run the virtual machine. Since virtualization software runs with overhead, it's probably good to have >24GB of RAM.

* Your BIOS settings must support virtualization. Secure boot or other UEFI settings may interfere with virtualization. If you don't know what I'm talking about, then don't worry...you probably won't have a problem.

# Installation instructions

1. Download and install the latest version of VirtualBox from the official website: [https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads)

2. Download the Virtual Machine image ("Virtual Appliance") from my Google Drive folder. It's the OVA file located in this folder: [https://drive.google.com/drive/folders/1VENAR4U5u7AtyVfpTDjy-1svyA7QWKZ2?usp=sharing](https://drive.google.com/drive/folders/1VENAR4U5u7AtyVfpTDjy-1svyA7QWKZ2?usp=sharing)

This contains an image of Ubuntu 22.04 LTS with all the preinstalled bioinformatics software required for running SARS-CoV-2 genomics analysis according to the EQA workshop.

3. Import the Virtual Appliance.

When importing the Virtual Appliance, you may change the number of virtual CPUs and the amount of RAM you wish to "allocate" to the virtual machine. By default, I have configured the virtual machine to run with 8 vCPUs and 16GB of RAM. If your physical machine has room to run a more powerful virtual machine, then please go ahead.

4. You are good to go!

* The default password for user is `genomics9800`.
* In the home folder, you can find a folder called `eqa_practical` which you can work with.
  * I have already created some scripts in the `scripts` subfolder which are based on the work I did following the tutorial ([https://cambiotraining.github.io/sars-cov-2-genomics/08-case_study_eqa.html](https://cambiotraining.github.io/sars-cov-2-genomics/08-case_study_eqa.html)) during the EQA workshop.
  * In the `viralrecon.sh` pipeline, the default number of CPUs is 8 and the max memory is 15 GB. If you allocated more than 8 CPUs and/or allocated more than 16GB of RAM to the virtual machine during setup, then feel free to increase these parameters to speed up your analysis. Just for fun, I noted that with 100 GB of RAM and 16 vCPUs on my desktop, it took 16 minutes (wall-clock time) to run the viralrecon pipeline for 6 EQA samples.
* A copy of this folder WITHOUT output/results/analysis has also been created -- look for the `eqa_practical_Blank_With_Data` folder. You can use this folder to experiment and to practice the tutorial exercises.
* Note: If you run into memory problems, consider changing the memory allocated to the VM, or changing the max memory usage in the `viralRecon.sh` script.
