# easymocap_win_install
Repository to help installing easymocp on windows

The video tutorial for installation of Easymocap on windows system.
https://www.patreon.com/posts/easymocap-raw-04-50646448

The video with the calibration to use on Easymocap
https://www.patreon.com/posts/easymocap-raw-04-50646809


To do the manual calibration you can use the labelme package

install it using 

`pip install labelme`

if you are a linux user, maybe this command will be better to install labelme (thanks to HacktopS https://twitter.com/HacktopS for the tip)

`sudo apt-get install labelme`


Attention

There is a huge thing that the tutorial We've done is missing, to say that you should run the installation script for easymocp

https://github.com/zju3dv/EasyMocap/blob/master/doc/installation.md#3-install

that says to run this line
`python3 setup.py develop --user`


## IMPORT Information
The new version of easymocap, has the option to create the data needed to import in the addon MOCAP_IMPORT, you just have to add this command `--write_smpl_full` when running easymocap.

For example, it you used to run this:
`python apps/demo/mv1p.py 0_input/sample --out 1_output/sample/smplx2 --undis --sub_vis 1 7 13 19 --body bodyhandface --model smplx --gender male`

You will have to run this:
`python apps/demo/mv1p.py 0_input/sample --out 1_output/sample/smplx2 --undis --sub_vis 1 7 13 19 --body bodyhandface --model smplx --gender male --write_smpl_full`

And in Mocap import, you will hve to import the folder `SMPL_FULL`



## Installing Pythorch 1.4 

### Steps to Install PyTorch 1.4.0
#### [Optional] Check if CUDA is installed
#### It is strongly recommended that you have CUDA 10.1 installed. Because PyTorch 1.4.0 does not support CUDA 10.2 or CUDA 11.0. Click here to install CUDA 10.1.
####
#### Once/If you have it installed, you can check its version here.
####
#### [For conda on Ubuntu/Linux and Windows 10]
#### Run conda install and specify PyTorch version 1.4.0
#### CUDA 10.2 is not officially supported, you have to install CUDA 10.1.
#### CUDA 10.1: `conda install pytorch==1.4.0 torchvision==0.5.0 cudatoolkit=10.1 -c pytorch`
#### CUDA 10.0: `conda install pytorch==1.4.0 torchvision==0.5.0 cudatoolkit=10.0 -c pytorch`
#### CUDA 9.2: `conda install pytorch==1.4.0 torchvision==0.5.0 cudatoolkit=9.2 -c pytorch`
#### CPU Only (your PyTorch code will run slower):
`conda install pytorch==1.4.0 torchvision==0.5.0 cpuonly -c pytorch`
