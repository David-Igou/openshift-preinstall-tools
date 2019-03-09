Getting ready to install Openshift can be painful and tedious. You are either given machines ridden with agents and tweaks that will cause you issues, or super vanilla boxes which require lots of manual tweaks to get ansible running smoothly. These help ease that pain.

For less pain: `export ANSIBLE_HOST_KEY_CHECKING=0`

#add-service-account-with-sudo.yml

Adds a service account with the name "openshift" - Grants it ssh auth and ttyless sudo

#docker-scratch-aws-storage-setup.yml
#docker-scratch-storage-setup.yml
#execute-setup-docker-storage.yml

Docker storage stuff. Run the setup, follow with execute.

#enable-repos.yml

enable openshift 3.11 repos. Adjust as needed.

#prepare-ansible-bastion.yml

Install random openshift client stuff because I always forget to

#register-servers-into-rhsm.yml
#satellite_register.yml

Used to register systems with RHSM, to Redhat or Satellite as named.

#turn-off-configuration-agents.yml

If this is the first time you are installing Openshift in an environment, it is highly advised to get a working baseline with as little deviations from vanilla RHEL as possible, and then incrementing your way to turning all your agents and stuff back on. You will save massive amounts of time doing this. When troubleshooting problems early on think of every deviation from vanilla adding another layer of potential troubleshooting, which must be reconsidered with each issue you see. 

Getting a baseline and introducing deviations in small iterations to QA their changes is the shortest and least frustrating path 100% of the time.
