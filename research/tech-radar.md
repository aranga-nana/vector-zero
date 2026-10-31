# Tech radar

Technologies Vector-Zero uses, is trialling, or is watching.

**Rings**
- **Adopt:** the default choice; proven in our projects.
- **Trial:** use it on a real project to learn it.
- **Assess:** worth investigating; not yet used.
- **Hold:** avoid for new work (outdated, unreliable, or superseded).

> The rings are Claude's starting positions, based on general hobbyist experience. Nothing has been used in a Vector-Zero project yet. Rings move when projects prove or disprove something, or when the owner agrees. News alone only produces a *suggested* move (see below).
>
> Last full sweep: **2026-10-31**. Versions come from web sources linked in Notes. Where a source was secondary or unclear, the entry says so.

## Suggested ring moves (owner to confirm)

_None pending._

## Ring change log

| Date | Technology | Change | Why | Approved by |
|---|---|---|---|---|
| 2026-10-31 | Google Coral Edge TPU | Assess → **Hold** | Retailers list it as retired. The last Edge TPU runtime is from 2022 and the GitHub repos are archived (secondary sources; no official Google EOL notice found). The Hailo-based AI HAT+ 2 is the supported path on Pi. | Owner |
| 2026-10-31 | ESP32-S31 | added at **Assess**; candidate for Trial on the first suitable project | In mass production. It looks like the new "do everything" ESP32 (Wi-Fi 6, BLE 5.4, Thread/Zigbee, Gigabit Ethernet). | Owner |
| 2026-10-31 | Raspberry Pi 5 | stays Trial, with a **price-check every time** rule | DRAM-driven price rises: 2GB is now $77.50 and 4GB is $110. Use an MCU, or the 1GB model ($45), when Linux isn't needed. | Owner |
| 2026-10-31 | ExpressLRS | stays Assess, with a **4.x migration warning** | 4.0 isn't backward compatible: both TX and RX must be reflashed. STM32 hardware and SPI receivers were dropped. | Owner |

## Radar

| Area | Technology | Ring | Why | Latest known version / status | Last checked | Notes / links |
|---|---|---|---|---|---|---|
| MCU | ESP32-S3 | Trial | Wi-Fi + BLE, USB, vector instructions for TinyML, cheap and everywhere | Current, well supported in ESP-IDF 6.0 and Arduino core 3.3.x | 2026-10-31 | |
| MCU | ESP32-S31 | Assess (Trial candidate) | Dual-core 320 MHz RISC-V with SIMD, Wi-Fi 6, BLE 5.4 (LE Audio + Classic), Thread/Zigbee, Gigabit Ethernet MAC, camera/LCD, 60 GPIO | Announced 2026-03-26; mass production ~July 2026; chip ~$4.51; dev board ~$20 | 2026-10-31 | [Espressif](https://www.espressif.com/news/ESP32_S31_Release), [Hackster](https://www.hackster.io/news/espressif-s-esp32-s31-dual-core-edge-smarts-microcontroller-hits-the-mainstream-launches-at-4-51-f616e6fc1716.amp), [Circuit Digest](https://circuitdigest.com/news/espressif-begins-mass-production-of-esp32-s31-risc-v-soc) |
| MCU | ESP32-C3 / C6 | Assess | Low-cost RISC-V; C6 adds Wi-Fi 6 + Thread/Zigbee | Current | 2026-10-31 | |
| MCU | ESP32-C5 | Assess | Dual-band (2.4 + 5 GHz) Wi-Fi 6, BLE, 802.15.4 | Mass production since Apr 2025; stable in ESP-IDF 6.0; DevKitC-1 at distributors | 2026-10-31 | [CNX: IDF 6.0](https://www.cnx-software.com/news/firmware/page/4/?amp=1), [Mouser](https://www.mouser.co.uk/c/semiconductors/?q=esp32) |
| MCU | ESP32-P4 | Assess | High-performance RISC-V, no radio (pair with a C6); MIPI camera and display, for vision/HMI | Chip rev 3.x changes the pinout (pin 54 becomes a power rail), so check the rev before designing a PCB. Older P4NRW32 reportedly EOL (forum claim). | 2026-10-31 | [esp32.com forum](https://esp32.com/viewtopic.php?p=155374) |
| MCU | ESP32-H4 | Assess | Low-power dual-core RISC-V, 802.15.4 + BLE 5.4 | Samples only; ESP-IDF 6.0 preview support. Not for projects yet. | 2026-10-31 | [Espressif](https://www.espressif.com/en/node/78) |
| MCU | RP2040 / RP2350 (Pico 2 / 2 W) | Trial | Great docs, PIO for odd protocols, Arm or RISC-V cores, very cheap ($7 Pico 2 W) | No new Pico variants found in 2026. RP2350 is now a Betaflight target. | 2026-10-31 | [TechRadar](https://www.techradar.com/pro/raspberry-pis-usd7-pico-2-w-adds-wireless-connectivity-for-iot-projects) |
| MCU | nRF54L15 (Seeed XIAO nRF54L15) | Assess | BLE 6.0, Thread, Zigbee, Matter; very low power; tiny XIAO form factor ($9.90, Sense $15.99 with mic + IMU) | Shipping; Zephyr / nRF Connect SDK / PlatformIO support | 2026-10-31 | [Zephyr board docs](https://docs.zephyrproject.org/latest/boards/seeed/xiao_nrf54l15/doc/index.html), [CNX](https://www.cnx-software.com/2025/07/31/seeed-studio-xiao-nrf54l15-usb-c-boards-support-matter-thread-zigbee-and-amazon-sidewalk/) |
| MCU | STM32 (F4/G4/H7) | Assess | Industrial-grade; heavier toolchain | Not checked this sweep | | |
| MCU | ESP8266 | Hold | Superseded by ESP32-C3 at similar cost | Still gets ESPHome support | 2026-10-31 | |
| SBC | Raspberry Pi 5 | Trial | Vision, edge compute, embedded Linux. **Re-check the price before every BOM**, and use an MCU or the 1GB model if Linux isn't needed. | Pi 6 not before 2028. **Prices as of 2026-10-01:** 1GB $45, 2GB $77.50, 4GB $110, 8GB $180, 16GB $305. | 2026-10-31 | [Phoronix](https://www.phoronix.com/news/Raspberry-Pi-5-2GB-Price-77.50), [Tom's Hardware](https://www.tomshardware.com/raspberry-pi/component-shortages-drive-raspberry-pi-prices-up-by-up-to-23-percent-escalating-lpddr4-lpddr5-costs-trigger-the-third-price-hike-of-the-year), [OMG! Ubuntu: Pi 6](https://www.omgubuntu.co.uk/2026/05/raspberry-pi-6-2028-no-npu) |
| SBC | Raspberry Pi Zero 2 W | Assess | Small, low-power Linux | Reported in short supply | 2026-10-31 | [Recalbox](https://www.recalbox.com/blog/2026-06-03-sortie-raspberry-pi-6-5-recalbox-retrogaming-actualites-news/) |
| SBC | Raspberry Pi Compute Module 5 | Assess | Custom carrier boards for products | Current industrial offering | 2026-10-31 | |
| Firmware | ESP-IDF | Assess | Full control on ESP32 | **v6.0** stable (2026-03-27): breaking changes, Picolibc default, new installer. v6.1 is on the schedule. v5.5.x is still supported. | 2026-10-31 | [ESP-IDF versions](https://github.com/espressif/esp-idf/blob/ae876915/docs/en/versions.rst), [CNX](https://www.cnx-software.com/news/firmware/page/4/?amp=1) |
| Firmware | Arduino core for ESP32 | Trial | Fastest path to a working prototype | **3.3.x** (3.3.12 the newest seen) | 2026-10-31 | [Espressif registry](https://components.espressif.com/components/espressif/arduino-esp32/versions/3.3.12/readme) |
| Firmware | PlatformIO | Trial | Reproducible builds across MCUs | ⚠ Espressif stopped adding new chips to official PlatformIO, so new ESP32s (C5, C6, P4, S31) depend on the community **pioarduino** fork. Fine for RP2040/STM32/nRF. | 2026-10-31 | [GitHub issue](https://github.com/platformio/platform-espressif32/issues/1225), [CNX: pioarduino](https://cnx-software.com/2024/08/27/platform-espressif32-fork-platformio-arduino-esp32-c6-esp32-c5-esp32-h2-esp32-p4) |
| Firmware | ESPHome | Assess | Fast Home Assistant devices with YAML | **2026.7.0** seen (remote build server, S31 Gigabit Ethernet). Since 2026.1: ESP-IDF is the default on ESP32 and the API requires an encryption key. | 2026-10-31 | [Changelog](https://esphome.io/changelog/2026.7.0/), [2026.1.0](https://esphome.io/changelog/2026.1.0/) |
| Firmware | Zephyr RTOS | Assess | Portable RTOS; steeper learning curve; native home for nRF54 | **4.4.2** (2026-08-07); now a twice-yearly release cadence | 2026-10-31 | [GitHub releases](https://github.com/zephyrproject-rtos/zephyr/releases) |
| Comms | MQTT (Mosquitto) | Trial | Simple pub/sub for IoT | **2.1.2** (2026-02-09). 2.1 adds an HTTP API/dashboard and a SQLite persistence plugin, and drops TLS 1.1. | 2026-10-31 | [Mosquitto blog](https://mosquitto.org/blog/2026/01/version-2-1-0-released/) |
| Comms | LoRa / LoRaWAN (SX1262) | Assess | Long range, low power | SX1262 is still the hobbyist standard | 2026-10-31 | |
| Comms | Semtech LR2021 (LoRa Plus, Gen 4) | Assess | Backward-compatible LoRa plus FLRC up to 2.6 Mbps and LR-FHSS | Eval kit only (with XIAO nRF54L15); no hobbyist breakout found yet | 2026-10-31 | [Semtech](https://www.semtech.com/products/wireless-rf/lora-plus/lr2021), [Mouser EVK](https://www.mouser.com/new/semtech/semtech-lr2021-transceiver) |
| Comms | Meshtastic | Assess | Off-grid LoRa mesh | App 2.7.x / 2.8.1 seen; device firmware version not confirmed | 2026-10-31 | [APKMirror](https://www.apkmirror.com/apk/meshtastic/meshtastic-2/meshtastic-2-7-12-29319940-google-release/) |
| Comms | Thread / Matter | Assess | Interoperable smart home | **Matter 1.6** (2026-06-17, per secondary sources). 1.5 added cameras, closures and soil sensors. Thread 1.4 is required for border routers from 2026. | 2026-10-31 | [Wikipedia](https://en.wikipedia.org/wiki/Matter_(standard)), [bbox-mag](https://www.bbox-mag.fr/divers/objets-connectes/matter-1-5-maison-connectee/45879507) |
| Comms | ESP-NOW | Assess | Low-latency peer-to-peer between ESP32s | Not checked this sweep | | |
| Home automation | Home Assistant | Trial | Central hub for DIY devices | **2026.10** (2026-10-07). Manual MQTT publish now needs admin. Cloud is being renamed "Home Assistant Link" in Dec. | 2026-10-31 | [Changelog](https://www.home-assistant.io/changelogs/core-2026.10/) |
| Drones | ArduPilot | Assess | Mature, broad hardware support, rich failsafes | **4.7.0** stable for all vehicles (2026-07-21); Copter 4.7.2 tag seen. ⚠ Upgrade notes: ATC_INPUT_TC needs about 33% scaling, and LittleFS logs are erased on upgrade. | 2026-10-31 | [Copter-4.7.0](https://github.com/ArduPilot/ardupilot/releases/tag/Copter-4.7.0), [Forum](https://discuss.ardupilot.org/t/copter-4-7-0-released/144650) |
| Drones | PX4 | Assess | Modern architecture, strong ROS 2 integration | **v1.17.0** stable: Zenoh/rmw_zenoh into ROS 2, experimental TFLM neural controller. ⚠ Breaking: RC deadzone and servo trim params changed; MAVLink v1 is opt-in only. | 2026-10-31 | [Release notes](https://docs.px4.io/v1.17/en/releases/1.17), [GitHub](https://github.com/PX4/PX4-Autopilot/releases/tag/v1.17.0) |
| Drones | Betaflight | Assess | FPV freestyle/racing | **2025.12.x** (2025.12.2 by Feb 2026); **2026.6** next in the twice-yearly cadence. Adds RP2350 targets and fixed-wing features. | 2026-10-31 | [Release notes](https://betaflight.com/docs/wiki/release/Betaflight-2025-12-Release-Notes), [GitHub](https://github.com/betaflight/betaflight) |
| Drones | ExpressLRS | Assess | Low-latency, long-range RC link. **Pick 4.x-compatible (ESP-based) hardware for new builds.** | **4.0.x** (4.0.0 ~Feb 2026, 4.0.1 ~May 2026). ⚠ Not compatible with 3.x; drops STM32/R9M/Ghost; SPI receivers stuck on 3.x; channel remaps; alternative arming needs EdgeTX ≥ 2.11. | 2026-10-31 | [Oscar Liang](https://oscarliang.com/expresslrs-4/) |
| Drones | MAVLink | Assess | Standard telemetry protocol | v2 is the default (PX4 1.17 makes v1 opt-in) | 2026-10-31 | |
| Robotics | ROS 2 | Assess | Standard robotics middleware | **Lyrical Luth** LTS (2026-05-22, supported to May 2031), on Ubuntu 26.04. Fast DDS is still the default. | 2026-10-31 | [Release page](https://docs.ros.org/en/lyrical/Releases/Release-Lyrical-Luth.html) |
| AI/ML | LiteRT for Microcontrollers (ex-TFLite Micro) | Assess | TinyML on MCUs | Renamed in 2024; many tools still say "TFLM" | 2026-10-31 | [Google Coral docs](https://developers.google.com/coral/guides/software/lite-rt-delegate) |
| AI/ML | Edge Impulse | Assess | Fast TinyML data-to-deploy pipeline | Owned by Qualcomm (2025). Free "Developer Plan" is the default tier; third-party hardware is still supported. | 2026-10-31 | [Edge Impulse blog](https://edgeimpulse.com/blog/introducing-the-developer-plan/) |
| AI/ML | Ultralytics YOLO26 | Assess | Edge-first object detection, no NMS, claimed ~43% faster on CPU (vendor claim) | Released; official Raspberry Pi tutorial | 2026-10-31 | [Raspberry Pi blog](https://www.raspberrypi.com/news/object-detection-with-ultralytics-yolo26-on-raspberry-pi/) |
| AI/ML | Raspberry Pi AI HAT+ 2 (Hailo-10H) | Assess | 40 TOPS INT4 with its own 8GB RAM; runs vision plus small LLMs/VLMs (~6B) locally | Launched Jan 2026; in production until at least Jan 2036; official price $200 (retailers vary) | 2026-10-31 | [Raspberry Pi](https://www.raspberrypi.com/products/ai-hat-plus-2/), [CNX](https://www.cnx-software.com/2026/01/15/raspberry-pi-ai-hat-2-targets-generative-ai-llm-vlm-with-hailo-10h-accelerator/?amp=1&noamp=mobile) |
| AI/ML | Google Coral Edge TPU | **Hold** | Was the cheap vision accelerator; use AI HAT+ 2 (Hailo) instead | Retired at retailers; runtime frozen since 2022 (secondary sources) | 2026-10-31 | [Core Electronics](https://core-electronics.com.au/google-coral-usb-accelerator.html.plain.md), [AI wiki](https://aiwiki.ai/wiki/edge_tpu) |
| PCB | KiCad | Trial | Free, open, industry-capable | **10.0.x** (10.0 in Mar 2026; 10.0.6 in Aug; 10.0.7 RC in Sep). Design variants, graphical DRC rule editor, STEP-only 3D models. | 2026-10-31 | [KiCad 10 release](https://www.kicad.org/blog/2026/03/Version-10.0.0-Released/), [10.0.6](https://www.kicad.org/blog/2026/08/KiCad-10.0.6-Release/) |
| PCB | EasyEDA + JLCPCB | Assess | Fastest path to assembled boards | Not checked this sweep | | |
| CAD | FreeCAD | Assess | Free, open parametric CAD | **1.1.x** (1.1 on 2026-03-24; 1.1.1 on 2026-04-15): live fillet/chamfer drag, better assembly | 2026-10-31 | [FreeCAD blog](https://blog.freecad.org/2026/03/25/freecad-version-1-1-released/) |
| CAD | Autodesk Fusion (personal use) | Assess | Most capable free-for-hobby CAD/CAM | No confirmed 2026 change found. Limits: non-commercial, under $1k revenue, 10 editable docs, reduced CAM/sim. | 2026-10-31 | [StackSheriff](https://stacksheriff.com/3d-printing/fusion-360-free-personal-license/) (secondary) |
| CAD | Onshape | Assess | Browser CAD; free plan is public docs only | Not checked this sweep | | |
| Power | LiPo / Li-ion 18650 + BMS | Trial | Standard portable power | | | |
| Power | LiFePO4 | Assess | Safer chemistry for solar and stationary | Not checked this sweep | | |
| Power | Sodium-ion cells | Assess | Cold-tolerant, cheap chemistry; ~3.0 V nominal needs its own BMS thresholds | Small-quantity 18650s exist, but supply, brands and BMS options are thin. 32140 may become the common format. | 2026-10-31 | [Sodium-ion tips + KiCad](https://zff.dev/TholinVali/sodium-ion-tips), [EEVblog](https://www.eevblog.com/forum/projects/sodium-ion-battery-evaluation/) |

## Regulations

**Owner location: Australia.** `/tech-watch` checks Australian rules. Always confirm the details below on the official sites before acting; most come from secondary sources.

| Area | Rule (as understood 2026-10-31) | Source / confidence |
|---|---|---|
| Drones (CASA) | Recreational drones over 250 g need **registration** (myCASA, renewed every 12 months) and free online **operator accreditation** (valid 3 years). Standard rules apply to all weights: ≤120 m AGL, VLOS, 30 m from people, not over populous areas, 5.5 km from controlled aerodromes. The fee is reported inconsistently (AUD 20 vs 40), so check myCASA. | [pickdrones](https://pickdrones.com/australia-casa-drone-rules/) (secondary); medium |
| Drones (CASA) | **Part 101 reform pending**: may change sub-250 g rules and bring in **Remote ID around 2027**. Watch it: it affects build choices (GPS + RID module). | [pickdrones](https://pickdrones.com/australia-casa-drone-rules/) (secondary); low, timeline may slip |
| Drones (CASA) | FPV: goggles-only flight breaks VLOS. A spotter keeping visual line of sight is needed. Club or approved fields are the safe default. | General CASA rules; check before flying |
| RF (ACMA) | LoRa and other ISM devices run under the **LIPD Class Licence 2015** in **915–928 MHz**: max 1 W EIRP, with spectral-density limits for digital modulation. Use **AU915** for LoRaWAN and the **ANZ** region for Meshtastic. Never use US915 or EU868 configs. | [legislation.gov.au](https://legislation.gov.au/F2016L00636/asmade/2016-05-03/es/original/pdf), [TTN forum](https://thethingsnetwork.org/forum/t/how-does-the-things-network-comply-with-australian-legislation/71036); medium |
| RF (ACMA) | 2.4 GHz (Wi-Fi, BLE, ELRS 2.4) and 5.8 GHz video are LIPD bands with power caps. High-power 5.8 GHz VTX settings (e.g. 800 mW+) can exceed the class licence. Check the VTX power table. Amateur bands need a licence. | Check the LIPD schedule; medium |
| Batteries | **NSW**: mandatory testing, certification and marking for e-micromobility lithium-ion products since Feb 2026. **National**: the ACCC is developing an e-bike / e-micromobility standard (announced Aug 2026). No national mandatory standard for loose lithium-ion cells yet. | [NSW Gov](https://www.nsw.gov.au/housing-and-construction/safety-home/electrical-safety/lithium-ion-battery-safety/new-standards-for-lithium-ion-batteries-e-micromobility-devices), [Treasury](https://ministers.treasury.gov.au/ministers/andrew-leigh-2025/media-releases/stronger-product-safety-standards-e-bikes); high for NSW |
| Mains (230 V) | In Australia, **fixed mains wiring must be done by a licensed electrician** (AS/NZS 3000). DIY home-automation designs must stay on the low-voltage side: plug-in certified smart plugs or relays, or have a sparky install fixed wiring. | Long-standing state law; high |

## Not checked this sweep
STM32, ESP-NOW, EasyEDA/JLCPCB, Onshape, LiFePO4 and the LiPo/BMS entries. These change slowly; check them next sweep.
