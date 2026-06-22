# 2. Hardware and Software Setup

This project used a low-cost SDR receiver together with open-source and SDR-oriented software tools. The main setup consisted of an RTL-SDR V3 receiver, a telescopic antenna, SDRSharp, GNU Radio Companion, Dump1090/Tar1090, and SatDump.

## 2.1 RTL-SDR V3

The **RTL-SDR V3** is a low-cost software defined radio receiver that can receive RF signals over a wide frequency range. In this project, it was used to receive FM broadcast signals, RDS data, ADS-B messages, and NOAA satellite signals.

The RTL-SDR converts the received RF signal into digital IQ samples. These samples can then be processed by software tools such as GNU Radio or SDRSharp.

## 2.2 Antenna system

A telescopic antenna was used with the RTL-SDR receiver. The antenna length was adjusted depending on the target frequency band. For FM broadcast reception, this setup was sufficient to observe and demodulate strong local stations.

For ADS-B at 1090 MHz, however, the antenna was not ideal. This limitation affected the reliability of position decoding and map visualization.

## 2.3 GNU Radio Companion

**GNU Radio Companion (GRC)** is an open-source graphical environment for building signal processing flowgraphs. In this work, GNU Radio was used for:

- FM demodulation
- Custom FM receiver design
- RDS signal extraction and decoding
- FM composite baseband analysis

GNU Radio was especially useful because it allowed the receiver chain to be examined block by block.

## 2.4 SDRSharp (SDR#)

**SDRSharp** is an SDR receiver and spectrum analysis software. It was used in the first stage of the project to observe FM broadcast stations, compare signal strengths, and analyze spectrum/waterfall views.

SDRSharp provided a quick way to verify that the RTL-SDR hardware and antenna were working correctly before moving to GNU Radio.

## 2.5 Other tools

For the later stages of the project, additional tools were used:

- **Dump1090** for ADS-B packet reception and decoding
- **Tar1090** for map-based aircraft visualization
- **SatDump** for NOAA satellite reception and APT processing workflow preparation
