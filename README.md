# BootCon-Project
Tshark.sh Code

#!/bin/bash
current_date_time=$(date)

echo "Traffic captured on date: $current_date_time" > tshark_network_logs.csv
sudo tshark -i lo -a duration:10 -T fields -E header=y -E separator=/t -e _ws.col.Time  -e ip.src -e ip.dst -e tcp.srcport -e tcp.dstport -e http.request.method -Y "http.request and ip.dst == 127.0.0.1"  >> tshark_network_logs.csv &

#tshark.csv is capturing the relevant data needed for basic web traffic analysis. 

echo "Traffic captured on date: $current_date_time" > tshark_attack.csv
sudo tshark -i lo -a duration:10 -T fields -E header=y -E separator=/t -e http.request.uri -e ip.src -e http.request.method -e http.file_data -Y "http.request and ip.dst == 127.0.0.1" >> tshark_attack.csv &

#tshark2.csv is filtering for specific traffic and potential XSS attacks.

sudo tshark -i lo -a duration:10 > tshark_splunk.csv

#tshark3.csv is creating a file without headers to import into SPLUNK


#lo interface = loopback interface. 

#T-Shark options

#-i = Interface selection

#-T = sets format of decoded packet

#-e = field identifier

#separator=/t = separating the fields by a tab

#header=y = creating headers for each of the following specified fields.

#sudo = privilege escalation

#echo = creating time stamps for files.

#NOTE: Ideally created file names should represent content.

