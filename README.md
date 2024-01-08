# LKS Provinsi Bidang Cloud Computing 2023

## Code Program Arduino
<p>Edit the variable marked with XXXX</p>

## Install Dependencies
`pip install python-dotenv`

## Code Program Pyhton
<p>For the python code, edit the variable marked with XXXXX</p>
<p>Update the environment</p>
MQTT_BROKER=XXXXXXX <br/>
MQTT_PORT=1883<br/>
MQTT_TOPIC=rumah/+ <br/>
AWS_ACCESS_KEY=XXXXXXXXXXXXXX <br/>
AWS_SECRET_KEY=XXXXXXXXXXXXXXXXXX <br/>
AWS_SESSION_TOKEN=XXXXXXXXXXXXXXXXXX<br/>
S3_BUCKET=XXXXXXXXXXXXXXXXXX <br/>
S3_REGION=us-west-2 <br/>
DYNAMODB_TABLE=XXXXXXXXXXX <br/>
DYNAMODB_REGION=us-east-1<br/>
MQTT_USERNAME=XXXXXXXXX <br/>
MQTT_PASSWORD=XXXXXXXXX <br/>

```sh
#!/bin/bash
yum install -y gcc-c++ make git
pip install python-dotenv
pip3 install boto3 paho-mqtt
git clone https://github.com/handipradana/lksprov.git
touch /home/ec2-user/lksprov/.env
printf "MQTT_BROKER=XX\n" >> /home/ec2-user/lksprov/.env
printf "MQTT_PORT=1883\n" >> /home/ec2-user/lksprov/.env
printf "MQTT_TOPIC=rumah/dht22\n" >> /home/ec2-user/lksprov/.env
printf "AWS_ACCESS_KEY=XXX\n" >> /home/ec2-user/lksprov/.env
printf "AWS_SECRET_KEY=XXX\n" >> /home/ec2-user/lksprov/.env
printf "AWS_SESSION_TOKEN=XXXX\n" >> /home/ec2-user/lksprov/.env
printf "S3_BUCKET=XXX\n" >> /home/ec2-user/lksprov/.env
printf "S3_REGION=us-east-1\n" >> /home/ec2-user/lksprov/.env
printf "DYNAMODB_TABLE=XXX\n" >> /home/ec2-user/lksprov/.env
printf "DYNAMODB_REGION=us-east-1\n" >> /home/ec2-user/lksprov/.env
printf "MQTT_USERNAME=XXX\n" >> /home/ec2-user/lksprov/.env
printf "MQTT_PASSWORD=XXX\n" >> /home/ec2-user/lksprov/.env
cat /home/ec2-user/lksprov/.env
echo "0 * * * * /usr/bin/python3 /home/ec2-user/lksprov/codepy.py"
sudo crontab -
sudo crontab -l
```
