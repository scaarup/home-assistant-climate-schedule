# home-assistant-climate-schedule

![image](https://user-images.githubusercontent.com/8055470/136662841-b83203ed-4c2a-41e6-9965-7051898d816f.png)

## Lovelace configuration
![image](https://user-images.githubusercontent.com/8055470/136662928-66a89f16-e579-439a-aec7-6098729cf4f9.png)
:
```yaml
type: grid
square: false
columns: 1
cards:
  - type: button
    tap_action:
      action: toggle
    entity: input_boolean.heating_schedule_global
    name: Tidsplan alle rum
    show_state: true
    icon_height: 50px
  - type: entities
    entities:
      - entity: input_number.heating_target_temp_plan_1_sal
        name: Temp. dagstid
      - entity: input_number.heating_target_temp_noplan_1_sal
        name: Temp. nat
      - entity: input_datetime.heating_schedule_start_1_sal
        name: Dagstid starter
      - entity: input_datetime.heating_schedule_stop_1_sal
        name: Dagstid slutter
      - entity: input_boolean.heating_schedule_1_sal
        icon: mdi:clock-outline
        name: Tidsplan
        state_color: true
    title: Tidsplan, 1.sal
    show_header_toggle: false
```

   
