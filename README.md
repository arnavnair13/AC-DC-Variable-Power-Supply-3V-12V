⚡ AC-DC Variable Power Supply

A hands-on hardware project where I designed and built a fully functional
regulated power supply from scratch — converting 230V AC mains into a
clean, adjustable 3V–12V DC output.

🔍 Overview

Most electronics projects I work on (ESP32, Arduino, sensors) need a
reliable DC source. Instead of buying an off-the-shelf supply, I built
one — giving me full control over the output voltage and a deeper
understanding of analog power electronics.

The output voltage is continuously adjustable using a potentiometer,
making it useful as a general-purpose bench supply for low-power projects.

🛠️ Tech / Components

- **LM317** – Adjustable linear voltage regulator (core of the design)
- **1N4007 x4** – Full-wave bridge rectifier
- **1000µF Capacitors x2** – Input and output filtering
- **240Ω Resistor + 5KΩ Pot** – Voltage adjustment network
- **Step-down Transformer** – 230V AC → 15V AC
- **LED** – Output power indicator

⚙️ How It Works
230V AC → [Transformer] → 15V AC
→ [Bridge Rectifier] → Pulsating DC
→ [Filter Capacitor] → Smooth DC
→ [LM317 + Resistor Network] → Regulated 3V–12V DC
The LM317 output is governed by:
Vout = 1.25 × (1 + R2/R1)
Where R1 = 240Ω (fixed) and R2 = 0–5KΩ (potentiometer).
Rotating the pot sweeps the output across the full 3V–12V range.

📊 Results

| Parameter | Value |
|-----------|-------|
| Input | 230V AC, 50Hz |
| Transformer Output | 15V AC |
| Rectified Output | ~13V DC (unregulated) |
| Regulated Output Range | 3V – 12V DC |
| Ripple | Minimal (dual 1000µF filtering) |
| Load Regulation | Stable under small load variations |

  What I Learned

- How each stage of a power supply pipeline works in practice
- LM317 datasheet reading and resistor network calculation
- Importance of filtering — observed ripple reduction directly on multimeter
- PCB/breadboard debugging with live AC — taught caution and respect
  for mains voltage

  
![WhatsApp Image 2026-03-23 at 12 05 09](https://github.com/user-attachments/assets/50ffe884-3e1a-4b34-8605-49ae44809478)

![WhatsApp Image 2026-03-23 at 12 05 10](https://github.com/user-attachments/assets/e0a80afe-cc3c-47a2-b4e3-1349037a8cda)

![WhatsApp Image 2026-03-23 at 12 05 10 (1)](https://github.com/user-attachments/assets/d29c39ab-02dc-42bd-ba3b-900b51319fb9)



  
