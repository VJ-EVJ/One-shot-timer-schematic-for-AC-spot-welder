# One-shot Timer Schematic for AC Spot Welder

A monostable (one-shot) timer circuit designed to control the weld duration of an AC spot welder through an SSR relay.
It is triggered by a push button and offers an adjustable timing range with two selectable operating modes — automatic and manual.

---

## ⚙️ Overview

This circuit functions as a **monostable timer** designed to control the **weld duration** of an AC spot welding transformer via an **SSR (Solid-State Relay)**.  
It starts timing when the **trigger button (SW1)** is pressed and automatically turns off the SSR after the preset time expires.

---

![Spot Welder Timer Circuit by Vytautas Janusonis (EVJ)](https://github.com/VJ-EVJ/One-shot-timer-schematic-for-AC-spot-welder/blob/main/spot%20welder's%20timer%20circuit%20by%20Vytautas%20Janusonis%20(EVJ)%202021-10-07.jpg)
*Fig. 1 – Spot welder timer schematic (by Vytautas Janusonis / EVJ, 2021-10-07)*

---

## 🧭 Operating Modes (SW3)

### **Mode A – Automatic**
When switch **SW3** is *open*, pressing SW1 even briefly will trigger a full timed weld cycle.  
The SSR output remains active for the entire set duration, regardless of how long the trigger button is held.

### **Mode B – Manual**
When switch **SW3** is *closed*, the SSR turns off immediately if SW1 is released before the timer finishes counting.  
This mode is useful for longer welds (in the range of seconds) when the operator may want to **stop the weld instantly** if the spot begins to overheat or burn.

---

## ⏱ Timing Adjustment (R3 + SW2)

- **R3 potentiometer** provides continuous timing adjustment with an **exponential/logarithmic** increase.
- **SW2** extends the time scale, increasing the range from approximately **415 ms** up to **5.1 s**.

---

## ⚡ Power Supply

- Recommended supply voltage: **12 V DC**
- Operating range: **7–15 V DC**
- ⚠️ Do **not exceed** the maximum supply voltage allowed for the **NE555** timer IC.

---

## 💡 Optional Output Indicator

You can connect an **LED indicator** (with ~1 kΩ series resistor) between **pin 3** of the 555 IC and **GND**.  
This LED will light up while the timer output is active.

---

## 🔌 Output & SSR Connection

The schematic output ends at the **SSR input**.  
The **AC transformer** and **welding electrodes** are **not included** in the schematic — connect them separately according to your welding setup.  
Make sure to use proper electrical isolation and an SSR rated for your transformer’s current and voltage.

---

## 🧰 Notes

- The circuit uses a standard **NE555 timer** IC in monostable configuration.
- Timing components and potentiometer values can be modified to suit your preferred weld duration range.
- SSR type and transformer wiring depend on your particular spot welder design.

---

## ✳️ Author’s Note

This circuit was designed and tuned for consistent and reliable spot welding control.  
I hope it proves useful in your projects!  
Feedback and suggestions are always welcome — feel free to share your results or improvements.

---

## License

This project is licensed under CC BY-NC-SA 4.0. See LICENSE.md for full details.

**Attribution required:** If you use, adapt, or redistribute the schematics, please credit the author with one of the following links:
- https://linkedin.com/in/vytautasjanusonis
- https://github.com/VJ-EVJ

Example attribution:
"Original schematic by EVJ — https://linkedin.com/in/vytautasjanusonis"

---

### 🧰 First version of fully functional spot welder device for battery cells
![First version of fully functional spot welder device for cells of batteries](https://github.com/VJ-EVJ/One-shot-timer-schematic-for-AC-spot-welder/blob/main/Pictures/old_version_of_spot_welder_for_batteries_cells.jpg)

---

### ⚙️ Upgraded version of fully functional spot welder device for battery cells
![Upgraded version of fully functional spot welder device for cells of batteries](https://github.com/VJ-EVJ/One-shot-timer-schematic-for-AC-spot-welder/blob/main/Pictures/finished_spot_welder_for_batteries_cells.jpg)

---

### 🧪 Experimental version of spot welder device for steel sheets
![Experimental version of spot welder device for steel sheets](https://github.com/VJ-EVJ/One-shot-timer-schematic-for-AC-spot-welder/blob/main/Pictures/machine%20for%20welding%20steel%20sheets.jpg)
