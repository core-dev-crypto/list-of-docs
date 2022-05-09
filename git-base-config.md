git config --global user.name "Marco Corelli"
git config --global user.email "emme.corelli@gmail.com"
eval `ssh-agent -s`
cd .ssh
cp /.../.ssh/id* ~/.ssh/.
chmod go=- ~/.ssh/*
chmod u=r ~/.ssh/*
ssh-add ~/.ssh/id_rsa
