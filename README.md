# tablo: A simple PC dashboard accessory

A device that connects to a PC via USB and displays various metrics, such as CPU and RAM usage, temperature, time etc.
A host control "app" is used to gather data and push it over serial interface (currently Linux only).
Displayed information is fully configurable on the host.
Several built-in data sources. Shell source can be used to display arbitrary user-defined data.
Buttons of the device can be used to run user-defined commands on the host.

Originally developed as a course project for the "Computer Systems" course at [Kharkiv National University of Radio Electronics](https://nure.ua).

## Usage:

Build the host appliction with the following command:
```
gcc -Wall main.c info_sources.c -o tabloctl
```
Lanuch it
```
tabloctl
```
Launch in the background (daemonize):
```
tabloctl -d
```
Config can be updated while the application is running:
```
pkill -SIGUSR1 tabloctl
```
