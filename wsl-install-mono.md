sudo apt update
sudo apt upgrade
sudo apt install git
sudo apt install apt-transport-https dirmngr gnupg ca-certificates
lsb_release -a
exit
lsb_release
sudo lsb_release
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
echo "deb https://download.mono-project.com/repo/debian stable-stretch main" | sudo tee /etc/apt/sources.list.d/mono-official-stable.list
sudo apt update
sudo apt install mono-devel