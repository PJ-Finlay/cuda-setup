# CUDA Setup for Ubuntu 20.04
** Warning uninstalls Xorg, and is designed for use on a server**
```
# Install CUDA
sudo apt-get update
sudo apt-get install -y vim git wget python3 python3-pip python-is-python3 python3-virtualenv
wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu2004/x86_64/cuda-ubuntu2004.pin
sudo mv cuda-ubuntu2004.pin /etc/apt/preferences.d/cuda-repository-pin-600
wget https://developer.download.nvidia.com/compute/cuda/11.2.0/local_installers/cuda-repo-ubuntu2004-11-2-local_11.2.0-460.27.04-1_amd64.deb
sudo dpkg -i cuda-repo-ubuntu2004-11-2-local_11.2.0-460.27.04-1_amd64.deb
sudo apt-key add /var/cuda-repo-ubuntu2004-11-2-local/7fa2af80.pub
sudo apt-get update
sudo apt-get -y install cuda

# Uninstall Xorg
sudo apt-get remove -y xserver-xorg-core

```
Run in one command:
```
curl https://raw.githubusercontent.com/PJ-Finlay/cuda-setup/main/cuda-setup.sh | sh
```
## Optional
### Reboot
```
curl https://raw.githubusercontent.com/PJ-Finlay/cuda-setup/main/cuda-setup.sh | sh && sudo reboot
```
### Configure Git
```
git config --global user.name "P.J. Finlay"
git config --global user.email "pjappdevelopment@gmail.com"
git config --global core.editor "vim"
```
