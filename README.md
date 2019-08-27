# Home-Assistant

I have adapted the fantastic code from @kloggy to an ESP32 and an 8 relay board to have up to 8 zones. I have 2 separate ESPs for a total of 16 zones configured the same way (only different names for the zones). One activates the "West" area, the other the "East". Also not using the Weather-related watering adjustments. No need given the weather patterns where I live :) 

Parts : 

https://www.amazon.com/gp/product/B07QCP2451/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1

https://www.amazon.com/gp/product/B07C8LSXKC/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1

https://www.amazon.com/gp/product/B07Q29CD7J/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1

Software Requirements: 
Requires the following custom cards to be installed and working
- toggle-lock-entity-row
- config-template-card
- fold-entity-row
- toggle-lock-entity-row

Setup the ESP32 with ESPHome
 - esp32_1.yaml for my example of how the ESP is configured to handle 8 zones
 - I have a second one configured the same way, just different names for the zones

Changes to configuration :
1.   Add following line in configuration.yaml 
     packages: !include_dir_named packages
2. Have the following directory : 
     /config/packages/garden
3. Place the 3 files in the config/packages/garden
   - garden_global.yaml
   - garden_irrigation.yaml
   - garden_master_control.yaml
4. changes to lovelace
   - see lovelace.yaml for the additional code to be added to lovelace to add the additional tab

   See here for more information in the OP - https://community.home-assistant.io/t/my-garden-irrigation/99686

