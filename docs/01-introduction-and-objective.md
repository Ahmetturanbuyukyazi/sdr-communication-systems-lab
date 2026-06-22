# 1. Introduction and Objective

Wireless communication systems are used in a wide range of applications, including radio broadcasting, satellite communication, air traffic surveillance, and Internet of Things systems. In traditional communication systems, receiver and transmitter structures are usually implemented with hardware designed for a specific standard. In modern systems, however, many of these operations can be carried out in software. This approach is known as **Software Defined Radio (SDR)**.

SDR makes it possible to work with different communication standards using the same hardware platform, while changing mainly the software processing chain. For this reason, SDR is a very useful tool for both education and research.

In this project, an **RTL-SDR V3** receiver and **GNU Radio Companion** were used to examine different communication signals. The study first focused on observing FM broadcast signals using SDRSharp. Then, the same signals were analyzed and demodulated in GNU Radio.

After testing the built-in WBFM receiver blocks, the FM demodulation process was rebuilt using lower-level GNU Radio blocks. This made it possible to understand the receiver chain more clearly, including frequency translation, filtering, quadrature demodulation, de-emphasis, resampling, and audio output.

In the next stage, **RDS (Radio Data System)** information embedded inside the FM broadcast signal was extracted and decoded. Station name, program type, PI code, and radiotext information were obtained successfully. The internal structure of the FM broadcast signal was also observed in the baseband spectrum, including the mono audio component, pilot tone, stereo subcarrier, and RDS subcarrier.

The project also includes preliminary work on **ADS-B aircraft tracking** and **NOAA weather satellite reception**. ADS-B packets were received and partially decoded using RTL-SDR and Dump1090, while the NOAA reception workflow was prepared using SatDump. These parts are planned to be improved in future updates.

Overall, the objective of this work is to understand how different real-world communication systems can be received, analyzed, and decoded using SDR-based methods.
