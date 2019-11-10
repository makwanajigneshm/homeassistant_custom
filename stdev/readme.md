This component calculates standard daviations of the input values. Input entity with state unknown are ignored.

Developed based on default  min_max sensor.

How to use this :-
1)   copy thise repo files into <HA_CONFIG>/custom_components/stdev/ folder
2) Modify your configuration.yaml like this.

```
sensor:
  - platform: stdev
    name : temperature_stddev
    entity_ids :
       - sensor.living_room_temperature
       - sensor.room1_temperature
       - sensor.room2_temperature
       - sensor.room3_temperature
```


Above example, takes the all 4 temperatures and calculates standard deviation. 
This value then can be used to control fan to bring the daviation under specific threhold 
