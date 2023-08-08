**Gateway Setup Document**
--------------------------------------------------------------------
**Commands**
---------------------------------------------------------------------
 - mkdir test
 - ls
 - cd test/
 - git clone 
 - ls
 - git clone https://github.com/iam-rnd/tagid-trial-theft-identity.git
 - ls
 - cd tagid-trial-theft-identity/
 - ls
 - git checkout 1-create-pos-selling-api 
 - ls
 - python3 -m venv venv
 - ls
 - cat requirements.txt 
 - ls
 - pip3 install -r requirements.txt 
 - source venv/bin/activate
-  pip3 install -r requirements.txt 
 - ls
 - sudo cp trial_theft_identity.servic /etc/systemd/system/
 - sudo systemctl enable trial_theft_identity.service 
 - sudo systemctl start trial_theft_identity.service 
 - journalctl -u trial_theft_identity.service -f
 - nano trial_theft_identity.service 
 - pwd
 - nano trial_theft_identity.service - If Requred to cahnge the path of servece file 
 - cat trial_theft_identity.service -
 - sudo cp trial_theft_identity.service /etc/systemd/system/
 - sudo systemctl enable trial_theft_identity.service 
 - sudo systemctl start trial_theft_identity.service 
 - journalctl -u trial_theft_identity.service -f
 - ls
 - nano config.json 
 - sudo systemctl restart trial_theft_identity.service 
 - journalctl -u trial_theft_identity.service -f
 

---------------------------------------------------------

**service sample file**

###### Reference
###### https://github.com/torfsen/python-systemd-tutorial

[Unit]
Description=Trial Theft Identity

[Service]
# Command to execute when the service is started
User=pi
Group=pi
WorkingDirectory=home/pi/tagid-trial-theft-identity
ExecStart=/home/pi/tagid-trial-theft-identity/venv/bin/python3  /home/pi/tagid-trial-theft-identity/main.py
Environment="INSTALL_PATH=/home/pi/iam-gateway"

[Install]
WantedBy=default.target

---------this file extension is .service --------------

