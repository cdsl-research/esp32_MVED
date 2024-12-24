Create passwords.py to connect your wi-fi network with SSID and password.
# Integrated Folder
Import this folder to your esp32

## boot.py
This file consists with these componensts below:
- Network configulation
- Establish connection
- Flag
- main

### Network configlation
import passwords from your passwords.py. Define your SSID_NAME_*.

### Establish connection
Establish connection with your SSID_NAME_* by executing connect_*_wifi().

connect_*_wifi() calls wifiscan() searchs nearby Wi-Fi signals.

flag() decides whather activate 'cm_main.py' or 'ch_main.py'.

## calc.py
This file normalizes 2 parameter values(battery, number of connectabele nodes) and calculate euclidian distance.

### normalize()
Normalize battery and number of connectable nodes.

Reading battery and number of connectable nodes from 'node_data.csv', normalize these 2 parameters.
Then, write the normalized data to 'normalized_node_data.csv'.

### extract_from_csv()
extract_from_csv() extracts 2 values from 'normalized_node_data.csv' and call sim_score().

### sim_score()
sim_score() calculates euclidian distance using given 2 arguments from extract_from_csv().

## Output sample
<img width="676" alt="image" src="https://github.com/user-attachments/assets/ecbee702-668a-477d-9749-770df69d164a" />


# Files need to be edited
## ID.txt
set unique number

<img width="428" alt="image" src="https://github.com/user-attachments/assets/7b17d52f-69a0-4f93-b287-2510e6bab20f" />


## flag.txt
set "True" for initial cluster head

set "False" for initial cluster member

<img width="428" alt="image" src="https://github.com/user-attachments/assets/9f5edf7d-7572-424f-8bc6-955ff71a65b2" />


## remaining_battery.csv, how_many_times.csv
delete file before starting experiment.
### remaining_battery.csv sample
<img width="405" alt="image" src="https://github.com/user-attachments/assets/5c15f99e-46a8-4d6d-9f9d-039bfe1e05d6" />

### how_many_times.csv sample
<img width="405" alt="image" src="https://github.com/user-attachments/assets/9e4c77a5-3fe4-4c36-a050-c1aaffd2ddcf" />



## cumulative_energy.txt
write "0" or delete file before start experiment 

<img width="365" alt="image" src="https://github.com/user-attachments/assets/6587e861-6244-4e15-bc61-9b794abf0d40" />

