sudo tee /etc/wsl.conf > /dev/null << EOF
[network]
generateResolvConf=false
EOF

echo -e 'nameserver 8.8.8.8\nnameserver 8.8.4.4' | sudo tee /etc/resolv.conf > /dev/null;
sudo chattr -f +i /etc/resolv.conf;