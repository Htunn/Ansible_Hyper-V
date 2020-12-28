# Manage windows machines with ansible

1.Upgrade powershell and .net framework

2.open winrm port with " winrm quickconfig " command in powershell admin

3.install "pywinrm" python module

4.pip3 install pywinrm

5.check ansible python version > 2.7 ( "ansible --version")

6.check windows winrm port connection with
 "ansible host-pattern -m win_ping "


#If having issue on pywinrm

pip3 install pywinrm

cp -r /usr/local/lib/python3.6/site-packages/* /usr/lib/python3.6/site-packages/

cp -r /usr/local/lib64/python3.6/site-packages/* /usr/lib64/python3.6/site-packages/


#ansible python module location 

 /usr/lib/python3.6/site-packages/ansible


# Check winrm 

To view the current listeners that are running on the WinRM service, run the following command:

PS> winrm enumerate winrm/config/Listener

WinRM Service Options

To get an output of the current service configuration options, run the following command:

winrm get winrm/config/Service

winrm get winrm/config/Winrs


# check winrm listener port using netcat

nc -vz windows2016.example.com 5986

nc -vz windows2016.example.com 5985



