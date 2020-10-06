# OS Management

## Start osms agent

Install package (Oracle Linux 8)

`sudo yum install -y osms-agent`

Check if it is running with...

`ps -elf | grep osms | grep -v grep`

and...

`sudo systemctl status oracle-cloud-agent`

## Create a Dynamic Group

Matching rule: `ALL {instance.compartment.id = '<ocid1.compartment.oc1...>' }`

## Write two policies

`Allow dynamic-group <dynamic-group-name> to use osms-managed-instances in compartment vmartin`

`Allow dynamic-group <dynamic-group-name> to read instance-family in compartment vmartin`

## Check Oracle Linux receive updates from OSMS

`sudo yum repolist`

`This system is receiving updates from OSMS server.`
