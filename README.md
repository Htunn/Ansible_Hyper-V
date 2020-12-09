# Manage windows machines with ansible

1.Upgrade powershell and .net framework \n
2.open winrm port with " winrm quickconfig " command in powershell admin \n
3.install "pywinrm" python module \n
4.pip3 install pywinrm \n
5.check ansible python version > 2.7 ( "ansible --version") \n
6.check windows winrm port connection with \n
 "ansible host-pattern -m win_ping " \n


If having issue on pywinrm \n

pip3 install pywinrm \n

cp -r /usr/local/lib/python3.6/site-packages/* /usr/lib/python3.6/site-packages/ \n
cp -r /usr/local/lib64/python3.6/site-packages/* /usr/lib64/python3.6/site-packages/ \n


ansible python module location = /usr/lib/python3.6/site-packages/ansible \n


# Check winrm  \n

To view the current listeners that are running on the WinRM service, run the following command: \n

PS> winrm enumerate winrm/config/Listener \n

WinRM Service Options \n

To get an output of the current service configuration options, run the following command: \n

winrm get winrm/config/Service \n
winrm get winrm/config/Winrs \n


# check winrm listener port using netcat \n

nc -vz windows2016.example.com 5986 \n
nc -vz windows2016.example.com 5985 \n


