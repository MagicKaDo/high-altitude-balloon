# First Steps

It is crucial to create a general overview of a project, including its goals and the means to achieve them. Technical details, budget, team roles, and deadlines must also be planned.

These are early ideas from our team:

1. **Sensors**

   * Thermometers (inside and outside)
   * Barometer
   * Hygrometer
   * Accelerometers
   * Camera
   * Photodiodes
   * UV sensor (optional)
   * Geiger counter (optional)
   * Magnetometer (optional)
   * Possibly some sensors integrated in an IMU

2. **Communication**

   * GPS module for position and speed tracking
   * LoRa for sending telemetry data (433 MHz for longer range)
   * GSM for recovery data after landing (e.g., SIM808 with GPS included, optional)
   * Our own communication system (e.g., instead of LoRa, optional, for testing)
   * Omnidirectional antenna on the ground
   * Additional directional antenna on the ground for better range (optional)

3. **Payload Box**

   * Styrodur for the exterior
   * Foam and foil for interior insulation
   * Mylar foil for thermal radiation insulation
   * Pressure vent
   * Parachute

4. **Microcontroller**

   * ESP32, Raspberry Pi Zero W, or STM32 board are considered depending on communication, camera, and power supply needs
   * Must handle sensor logging and communication modules
   * Redundant secondary board

### Atmospheric Data

Sensors will capture and log environmental conditions at different altitudes. Some data could be transmitted if the available bitrate is sufficient.

### Tracking Balloon

GPS will track position and speed. Additional sensors, such as accelerometers, barometers, and magnetometers, could provide complementary data.

### Communication

For long-distance communication, LoRa or another solution can be used. Due to limited bitrate, data packets need to be small and well planned. The main ground antenna could be omnidirectional, while a secondary directional antenna could optionally provide better range.
After the payload lands, a GSM module could be used to send recovery data, logs, or even photos if the signal is sufficient. Telemetry data, photos, and system logs will be saved to two microSD cards for redundancy.

### Board with Microcontroller

There is a need to optimize between power consumption, weight, processing power, and ease of implementation. Raspberry Pi Zero W, ESP32, and STM32 are currently under consideration.

### Payload

Sensors,batteries,  microcontroller boards, and communication modules will be wrapped in foam and foil and placed inside a Styrodur box. Styrodur is lightweight, thermally insulating, widely available, and easy to work with. Additionally, Mylar foil can be used to reduce heat radiation. The exterior of the box will host some sensors, a whip antenna, the parachute, and balloon attachment points. Also, chemical heating pads are considered.