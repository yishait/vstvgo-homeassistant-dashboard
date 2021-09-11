# vstvgo-homeassistant-dashboard

The following repo was created for watching UStvgo channels via home assistant dashboard, broadcasting to google chromecast. 

Assuming you have a Home Assistant Core (python server) running 
https://www.home-assistant.io/installation/

and you are managing dashboards using YAML files

this project utilizes https://github.com/benmoose39/ustvgo_to_m3u project to get the .m3u streaming files provided by ustvgo.tv, these streams are valid only for ~4 hours and need to be refreshed

when managing the HA dashboards using YAML - no restart is required when refreshing the links in the dashboard.

steps to run:
go to your .homeassistant folder (where the configuration.yaml is)
and run:

'''
git clone https://github.com/yishait/ustvgo-homeassistant-dashboard.git
'''

add your rooms and the devices used in them to the settings.yaml file:
dashboard_settings:
  room1: 
    devices: 
      - device_1
  room2: 
    devices:
      - device_2

if they dont exist - the script will add them to your configuration.yaml used to run Home-assistant 