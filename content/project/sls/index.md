---
title: SLS 3D printer
date: 2018-05-04T08:58:25.233Z
summary: A desktop open source Selective‑Laser‑Sintering 3D printer using mirror
  galvanometer.
draft: false
featured: true
authors:
  - Independently
show_date: false
links:
  - url: https://github.com/qiayuanliao/OpenMGSLS
    name: Source
    icon_pack: fab
    icon: github
image:
  filename: featured.png
  focal_point: Top
  preview_only: true
---
# Motivation

I used to be a 3D printing enthusiast; I reproduced some open-source FDM printers like kossel in middle school and realized the limitations of FDM 3D printers. I learned that SLS is a high-precision 3D printing method and can even print metal. 

![](sls0.jpg "Selective laser sintering process")

So I spent about one year (2017~2018) building a desktop SLS 3d printer all by myself when I was in high school.
Although the project looks pretty naive now, the desktop SLS printer with the laser galvanometer had never been presented to the authors’ best knowledge at that time.

# Parts

## Laser Galvanometer System

The Laser galvanometer works the same as the voltmeter; the volt determines the angle of mirrors that reflect the laser. We use serial to communicate with the computer and receive the GCode(GCode is the most widely used numerical control programming language), process the GCode and plan, calculate the mirrors angle for each movement, use SPI to send the volt data to the DAC module, output the volt and make galvanometer turn to the corresponding angle.

<center>{{< gallery album="sls/mg" >}}</center>

## 2D Sintering Testing Platform

A 2d testing platform with a stage performance-grade galvanometer from AliExpress was made for single layer sintering. The platform and a nylon sintering test result are shown below.

<center>{{< gallery album="sls/test2d" >}}</center>

## Powder Delivery System

The Powder Delivery System shown below, driven by three stepper motors, spreads the powder evenly over the previous layer. Two pistons store the printed part and the powder waiting to be used respectively.

<center>{{< gallery album="sls/powder" >}}</center>

# 3D Printer

Combining Laser Galvanometer and Powder Delivery System, we got an SLS 3D printer.

![](printer.jpg "SLS 3D Printer I build")

A dry run test video is shown below.

{{< youtube qisKUQljb_s >}}

# Print result
I added toner in nylon to improve the ability to absorb laser energy, then printed complex geometric mechanisms, 3DBenchy, small chains to test the performance of the printer.

<center>{{< gallery album="sls/result" >}}</center>

A printing process and small chain videos are shown below.

{{< youtube Q6LMEkzwmUA >}}
