# WHOI-ROS

ROS 2 drivers, messages and vehicle tools from the Woods Hole Oceanographic Institution.

**The code lives on WHOI's GitLab: <https://git.whoi.edu/whoi-ros>.**
This GitHub repository is only a signpost. Please open issues and merge requests on git.whoi.edu.

## Repositories

### Core libraries

- [wr2_asio](https://git.whoi.edu/whoi-ros/wr2_asio): ROS 2 port of ds_asio.
- [wr2_base](https://git.whoi.edu/whoi-ros/wr2_base): Shared node scaffolding, partly ported from ds_base.
- [wr2_sensor_base](https://git.whoi.edu/whoi-ros/wr2_sensor_base): Base classes for sensor drivers.

### Messages and parsers

- [wr2_msgs](https://git.whoi.edu/whoi-ros/wr2_msgs): Every message, service and parser the stack uses.

### Vehicle components and navigation

- [wr2_components](https://git.whoi.edu/whoi-ros/wr2_components): Nodes that give every vehicle the same ROS API for shared jobs.
- [wr2_nav](https://git.whoi.edu/whoi-ros/wr2_nav): Rotate-and-sum dead-reckoning navigation for AUVs, plus PHINS nav, local frame conversion, water velocity and bathymetry estimator nodes.

### Navigation sensors

- [wr2_phins_ins](https://git.whoi.edu/whoi-ros/wr2_phins_ins): PHINS inertial navigation system driver, ported from the DS_ROS driver.
- [wr2_nortek_dvl](https://git.whoi.edu/whoi-ros/wr2_nortek_dvl): Parses DF21 binary bottom-track and water-track records over serial or UDP.
- [wr2_rdi_dvl](https://git.whoi.edu/whoi-ros/wr2_rdi_dvl): Separate nodes for the PD0 and PD5 output formats, over serial or UDP.
- [wr2_sonardyne_usbl](https://git.whoi.edu/whoi-ros/wr2_sonardyne_usbl): Parses PSONLLD position strings and publishes each beacon fix as sensor_msgs/NavSatFix.
- [wr2_nmea_gps](https://git.whoi.edu/whoi-ros/wr2_nmea_gps): GPS driver over serial, UDP or string input, with a fake NMEA generator for testing.
- [wr2_paro_depth](https://git.whoi.edu/whoi-ros/wr2_paro_depth): Parses Digiquartz pressure strings and publishes DepthPressure, using the wr2_sensor_base depth class for pressure-to-depth conversion.
- [wr2_keller_pressure](https://git.whoi.edu/whoi-ros/wr2_keller_pressure): Pressure sensor driver over serial or UDP, with unit tests.

### Science sensors

- [wr2_sbe_ctd](https://git.whoi.edu/whoi-ros/wr2_sbe_ctd): CTD driver over serial or UDP.
- [wr2_nbosi_ct](https://git.whoi.edu/whoi-ros/wr2_nbosi_ct): Conductivity and temperature driver.
- [wr2_anderaa_optode](https://git.whoi.edu/whoi-ros/wr2_anderaa_optode): Parses AADI MEASUREMENT and OXYGEN strings and publishes oxygen concentration, air saturation and temperature.
- [wr2_svp70](https://git.whoi.edu/whoi-ros/wr2_svp70): Sound speed from the AML, Valeport or Reson output formats, published as SoundSpeed with range clamping.
- [wr2_aps_mag](https://git.whoi.edu/whoi-ros/wr2_aps_mag): Three-axis magnetic field in nanotesla and sensor temperature, over serial or UDP.

### Sonar and imaging

- [wr2_iss360_sonar](https://git.whoi.edu/whoi-ros/wr2_iss360_sonar): Scanning sonar driver over Ethernet, built on a bundled snapshot of the Impact SDK 3.1.6.
- [wr2_sonoptix_fls](https://git.whoi.edu/whoi-ros/wr2_sonoptix_fls): Python node that drives the forward-looking sonar through its web interface and publishes MultibeamImage.
- [wr2_mst_sas](https://git.whoi.edu/whoi-ros/wr2_mst_sas): Python node that switches pinging through the sonar's web API, and a C++ node that feeds it vehicle navigation.
- [wr2_kraken_sas](https://git.whoi.edu/whoi-ros/wr2_kraken_sas): Synthetic aperture sonar driver on wr2_sensor_base.
- [wr2_voyis_insight](https://git.whoi.edu/whoi-ros/wr2_voyis_insight): Integration of the Voyis Insight imaging system as it runs on the WHOI REMUS 600 back-seat computers.
- [wr2_sonar_visualizers](https://git.whoi.edu/whoi-ros/wr2_sonar_visualizers): Turns sonar data into sensor_msgs/Image for display.

### Power and propulsion

- [wr2_tdk_lambda_ps](https://git.whoi.edu/whoi-ros/wr2_tdk_lambda_ps): Merges the two DS_ROS drivers for different firmware revisions.
- [wr2_vesc](https://git.whoi.edu/whoi-ros/wr2_vesc): Thruster driver for Orpheus over serial or CAN.

### Simulation and tools

- [wr2_sim](https://git.whoi.edu/whoi-ros/wr2_sim): Gazebo Harmonic plugins, worlds and launch files for vehicles that use WHOI ROS 2 messages, plus wr2_ocean, a standalone model of waves, currents, wind and the forces they put on a hull.
- [wr2_timegen](https://git.whoi.edu/whoi-ros/wr2_timegen): Broadcasts NMEA $GPZDA time strings at 1 Hz over UDP, TCP, serial or ROS raw to keep sensor clocks in step.
- [wr2_utils](https://git.whoi.edu/whoi-ros/wr2_utils): Small vehicle tools.
- [wr2_docs](https://git.whoi.edu/whoi-ros/wr2_docs): Hosts the group wiki, including the full getting-started guide and git credential setup.

## Getting access

The whoi-ros projects are public to read. To contribute, ask a maintainer of the
[whoi-ros group](https://git.whoi.edu/whoi-ros) for a git.whoi.edu account and project access.
