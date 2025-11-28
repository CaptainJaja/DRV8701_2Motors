# Driver DRV8701 – Dual H-Bridge 40 V / 10 A (15 A peak)

> PCB designed with **KiCad** for driving **two brushed DC motors** up to 40 V / 10 A.
> Each channel uses a TI **DRV8701** driver paired with four **TPH1R403NL** power MOSFETs.
> The board integrates **encoder feedback** for PID control, as well as **current regulation** handled directly by the DRV8701.
> The current limit is set to **3 A**: above this value, the driver applies **PWM current chopping** to maintain the current below the set point.

---

## ⭐ Sponsor: PCBWay

This project was **sponsored by PCBWay**, who kindly provided the PCBs for prototyping.
The PCB quality is excellent and the support very responsive.

👉 **PCBWay Link:**
[![PCBWay](https://img.shields.io/badge/PCBWay-Sponsor-orange.svg?style=flat\&logo=data\:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxMjAiIGhlaWdodD0iMzAiIHZpZXdCb3g9IjAgMCAxMjAgMzAiPjx0ZXh0IHg9IjAiIHk9IjIwIiBmb250LXNpemU9IjMwIiBmaWxsPSIjMDBhNjAwIj5QQ0JXYXk8L3RleHQ+PC9zdmc+)](https://www.pcbway.com/)

Thanks again to Liam and the PCBWay team for their support!

---

## Main Specifications

| Parameter                | Value                                        |
| ------------------------ | -------------------------------------------- |
| Supply voltage VM        | 7 – 40 V                                     |
| Continuous current/motor | 10 A (4-layer PCB, 1 oz copper)              |
| Peak current             | 15 A (≤ 100 ms)                              |
| Chopped current limit    | 3 A (via DRV8701)                            |
| Topology                 | 2 × full H-bridge (DRV8701 + 4 MOSFETs each) |
| Control signals          | PH / EN / nSLEEP (TTL 3.3 V / 5 V)           |
| LED indication           | **EN** (active when nSLEEP = HIGH)           |
| NeoPixel indication      | Battery status (>25 V / 23–25 V / <23 V)     |
| PCB dimensions           | 100 mm × 40 mm                               |

---

## Thermal Management

* DRV8701 **exposed pad** connected to the GND plane through thermal vias.
* **TPH1R403NL (SOP-Advance)** MOSFETs soldered onto a large copper area + internal plane for heat spreading.
* Bulk decoupling capacitors: **470 µF / 50 V**, low ESR.

---

## PCB Views

### Component side

![PCB Front](ImageFront.png)

### Bottom copper side

![PCB Back](ImageBack.png)

