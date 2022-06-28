# Dojo Mini Kafka Platform   

This is a collection of Infrastructure as Code resources which can be used to install, configure and manage the lifecycle of several Kafka components.

# How to do step by step process for setting up Kafka

-> Clone the repo  
    
-> Download the kafka binaries archive from  https://dlcdn.apache.org/kafka/3.2.0/kafka_2.13-3.2.0.tgz

-> Place the kafka archive file in files directory

Links: https://www.apache.org/dyn/closer.cgi?path=/kafka/3.2.0/kafka_2.13-3.2.0.tgz

Update the necessay variables in the -variables.yml
    
    KAFKA_ARCHIVE:      -- latest kafka binary archive 
    INSTALLATION_DIR:   -- Directory archive is expanded to 

    KAFKA_USER:         -- Operating system user who will own the installation
    KAFKA_GROUP:        -- Group who can manage the installation

    ##  ENV Variables
    HOME:               --Home location where installation is present
    BASE:               --common lin to installation

    DATA_DIR:           -- location to store zookeeper and kafka data and logs
   
    
# Prepare inventory

`[kafkaserver1] 
<HOST_IP_ADDRESS> ansible_user=<ANSIBLE_USER> `

NOTE: use __ssh-add__ to add your private key to your ssh-agent

## Running Playbook

`ansible-playbook kafka-main.yml  ( -v for verbose, --step to run interactively)`

###once kafka is installed and configured use below for daily maintenance:
   
`ansible-playbook stop_start_kafka.yml --tag stop (To stop kafka services)`
    
`ansible-playbook stop_start_kafka.yml --tag start (To start kafka services)`

## Example

`ansible-playbook kafka-main.yml -inventory --step -vv`

### Start stop 
`ansible-playbook stop_start_kafka.yml --tag stop (To stop kafka services)`
    
`ansible-playbook stop_start_kafka.yml --tag start (To start kafka services)`