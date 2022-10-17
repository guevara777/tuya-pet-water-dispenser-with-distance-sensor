# Tuya Pet Water Dispenser with Distance Sensor
I upgraded my Tuya Pet Water Dispenser with an ESP32 and a Distance Sensor to automaticly start the pump if a pet is in front of the dispenser and stop the pump as soon as there is not pet in front of the dispenser for 30 seconds.

![PXL_20221017_202828599](https://user-images.githubusercontent.com/29648553/196281586-7b63e71f-6aa1-4c22-a911-5c76376d48aa.jpg)



## What is this?
I took my Tuya Pet Water Dispenser and replaced the orginal Board inside with an ESP32 and also added a distance sensor and a relay the start / stop the pump.

Now the pump will start as soon as there is an object (e.g. a pet) nearer than 90 cm in front of the pet water dispenser. The pump will run until there is no object 90cm oder nearer in front of it for 30 seconds or more.

## What do i need?
- 1 x Tuya WiFi Cat Water Dispenser 2.5L Automatic Pet Water Feeder (~ 50 € got mine for 35 € - [Link](https://www.aliexpress.com/item/1005003726277303.html?spm=a2g0o.productlist.0.0.f7c72272WTu7qI&algo_pvid=36cb1fd8-b29e-4511-9068-1e09021b52d6&algo_exp_id=36cb1fd8-b29e-4511-9068-1e09021b52d6-14&pdp_ext_f=%7B%22sku_id%22%3A%2212000029712709668%22%7D&pdp_npi=2%40dis%21EUR%2189.16%2149.04%21%21%21%21%21%402100bb5116660393799365670e562b%2112000029712709668%21sea&curPageLogUid=xDwKf8HcFkYT)
- 1 x ESP32-Board (~ 10 Euros - [Link](https://www.amazon.de/dp/B071P98VTG/ref=twister_B07Z6CSD9K?_encoding=UTF8&psc=1))
- 1 x Ultrasonic Range Finder (~5 Euros - [Link](https://www.amazon.de/gp/product/B07TKVPPHF/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&th=1))
- 1 x Relay (~5 Euro - [Link](https://www.amazon.de/gp/product/B07TYG14N6/ref=ppx_yo_dt_b_asin_title_o01_s00?ie=UTF8&th=1))
- 1 x Breadboard (~ 4 Euros - [Link](https://www.amazon.de/gp/product/B07KKJSFM1/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&th=1))
- 1 x USB-Power-Plug and USB-Cable (took one i had laying around here)
- some Jumper wires male-to-male and male-to-female
- Cable-Connectors (Wago-Klemmen)


## Hardware-Setup
All the needed hardware fits perfectly in the space between the water tank an the bottom of the case. I had to drill 3 holes in the case (2 for the ultrasonic sensor, 1 for the second power supply for the pump).
![PXL_20221017_202921697](https://user-images.githubusercontent.com/29648553/196281986-8dee2d7d-365a-4120-aad1-b20a5cae323d.jpg)
![Folie1](https://user-images.githubusercontent.com/29648553/196286765-be07d57a-5710-4a12-bfcf-3e49733f4f33.PNG)

## Software-Setup


### ESPHOME
See [ESPhome-Yaml-Code](https://github.com/guevara777/smart_raised_garden_bed_irrigation/blob/main/esphome_code.yaml) for Water-Level-Sensor 
