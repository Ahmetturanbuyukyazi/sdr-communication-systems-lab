# SDR Telecommunication Lab

This repository documents a series of Software Defined Radio (SDR) experiments performed with an RTL-SDR V3 receiver. The work focuses on receiving, observing, demodulating and decoding real-world communication signals using SDRSharp, GNU Radio and related SDR tools.

## Project scope

The main goal is to understand how different wireless communication systems can be received and analyzed using a low-cost SDR platform. The experiments start with FM broadcast reception and continue with RDS decoding, FM baseband structure analysis, ADS-B aircraft message reception and NOAA weather satellite signal acquisition.

## Hardware and software

**Hardware**

- RTL-SDR V3 USB receiver
- Telescopic antenna
- Computer

**Software**

- SDRSharp (SDR#)
- GNU Radio Companion
- Dump1090 / tar1090
- SatDump

## Documentation

The report is organized as separate documentation pages:

1. [Introduction and Objective](docs/01-giris-ve-calismanin-amaci.md)
2. [Hardware and Software Setup](docs/02-kullanilan-donanim-ve-yazilim.md)
3. [FM Broadcast Analysis with SDRSharp](docs/03-sdrsharp-ile-fm-yayinlarinin-incelenmesi.md)
4. [FM Analysis with GNU Radio](docs/04-gnu-radio-ile-fm-yayininin-analizi.md)
5. [FM Demodulation and RDS Decoding](docs/05-fm-demodulasyonu-ve-rds-cozumleme.md)
6. [FM Broadcast Baseband Structure](docs/06-fm-yayininin-ic-yapisi.md)
7. [ADS-B Aircraft Tracking](docs/07-ads-b-ile-ucak-takibi.md)
8. [NOAA Weather Satellite Reception](docs/08-noaa-hava-durumu-uydularinin-alinmasi.md)

## Main results

- Several FM broadcast stations were observed using SDRSharp.
- MAX FM at 95.8 MHz was selected as the reference station due to its strong and stable signal.
- FM demodulation was implemented in GNU Radio using both the built-in WBFM Receive block and a custom block-level receiver chain.
- RDS data was decoded successfully, including station name, program type, PI code and radiotext.
- The internal structure of an FM broadcast signal was observed: mono audio, 19 kHz pilot tone, 38 kHz stereo subcarrier and 57 kHz RDS subcarrier.
- ADS-B packets were received at 1090 MHz and decoded using Dump1090.
- NOAA-19 reception was prepared using SatDump, and IQ recording / processing workflow was started.

## Current status

This repository is a work in progress. The FM and RDS parts are functional and documented. ADS-B reception is partially successful, but aircraft positions could not be displayed reliably due to antenna and signal limitations. NOAA APT image processing is planned as the next step.

## Author

Ahmet Turan Büyükyazı  
Hacettepe University, Department of Electrical and Electronics Engineering

## Advisor

Prof. Dr. Cenk Toker
