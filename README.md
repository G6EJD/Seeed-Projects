# Seeed-Projects
Using SEEED products to create various projects

1. Installing
2. Start by downloading all files to a folder (Main file e.g. EN1001 or EN04 variant, common, language, credentials)
3. You will need an OpenWeatherMap API key. You get 1000 calls/day free, then if the limit is exceeded you will be charged $0.01 / excess-call. To get the API key, you need to add a payment method to your account, then OWM can charge you should you exceed 1000 calls/day.
4. You will also need to add the following libraries to your IDE:
#include <ArduinoJson.h>  // https://github.com/bblanchon/ArduinoJson needs version v6 or above
#include <WiFi.h>         // Built-in
#include <WiFiClient.h>
#include <HTTPClient.h>
#include "owm_credentials.h"  // See 'owm_credentials' tab and enter your OWM API key and set the WiFi SSID and PASSWORD
#include "common.h"
#include "lang.h"  // Localisation (English)
#include <time.h>  // Built-in
#include <SPI.h>   // Built-in
#define ENABLE_GxEPD2_display 0
#include <GxEPD2_BW.h>
#include <U8g2_for_Adafruit_GFX.h>

The EN1001 has a Green button, press this to refresh the display should you require the current forecast from the last refresh, typically made on the hour (07:00, 08:00...23:00).
The EN04 can be refreshed using the Reset button.

Battery life:
Both units should last for 190-days or about 6-months between battery charging. The EN04 variant battery life, will depend on battery capacity, but will be the same at about 90-days per 1000mAhr battery capacity.

EN1001
7.5" 800x480 E-Paper Layout
![alt text width="600"](/images/EN1001.jpg)

EN04 with Seeed 5.83" epaper panel
7.5" 800x480 E-Paper Layout
![alt text width="600"](/images/EN04.jpg)

For language files see here: https://github.com/G6EJD/ESP32-e-Paper-Weather-Display/tree/master/src

