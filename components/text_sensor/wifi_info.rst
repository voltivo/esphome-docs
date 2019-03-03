WiFi Info Text Sensor
=====================

.. seo::
    :description: Instructions for setting up wifi info text sensors.
    :image: network-wifi.png

The ``wifi_info`` text sensor platform exposes the ESPHome WiFi information.

.. code-block:: yaml

    # Example configuration entry
    text_sensor:
      - platform: wifi_info
        ip_address:
          name: "Current IP Address"
        ssid:
          name: "Current WiFi SSID"
        bssid:
          name: "Current WiFi BSSID"

Configuration variables:
------------------------

- **ip_address** (*Optional*): The text sensor for the current ip address.
  All options from :ref:`Text Sensor <config-text_sensor>`.
- **ssid** (*Optional*): The text sensor for the current connected WiFi SSID.
  All options from :ref:`Text Sensor <config-text_sensor>`.
- **bssid** (*Optional*): The text sensor for the current connected WiFi BSSID.
  All options from :ref:`Text Sensor <config-text_sensor>`.

See Also
--------

- :apiref:`text_sensor/wifi_info.h`
- :ghedit:`Edit`

.. disqus::
