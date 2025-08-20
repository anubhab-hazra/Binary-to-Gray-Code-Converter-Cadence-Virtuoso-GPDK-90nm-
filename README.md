# Binary to Gray Code Converter — Cadence Virtuoso (GPDK 90nm)

Design and implementation of a **Binary to Gray code converter** using **NAND-based XOR gates** in **Cadence Virtuoso (GPDK 90nm)**.  
The project was developed step by step: NAND gate → XOR gate (using NAND) → 4-bit Binary to Gray converter. Each block was designed, symbolized, tested with a testbench, and functionally verified.

---

## 📌 Short description
A 4-bit Binary-to-Gray code converter built in **Cadence Virtuoso (GPDK 90nm)**. The design was implemented at the transistor level, starting from basic NAND gate construction, then building XOR from NAND, and finally assembling the full converter.  

---

## 📝 Key results
- **NAND gate:**  
  - Designed at transistor level (PMOS + NMOS).  
  - Created symbol for hierarchical use.  
  - Verified functionality with testbench.  

- **XOR gate (NAND-based):**  
  - Implemented XOR using 4 NAND gates.  
  - Generated symbol and validated logic through testbench simulation.  

- **Binary to Gray Code Converter (4-bit):**  
  - Built using three XOR gates.  
  - Verified outputs against truth table.  
  - Functional simulation waveforms match expected Gray code behavior.  

- **Technology:** GPDK 90nm (VDD = 1.2V default).  
- **DRC / LVS:** Clean, no errors.  

---

## 📐 Design methodology
1. **NAND Gate Design** — built using 180nm CMOS, 1.8V VDD.  
2. **NAND-based XOR Gate** — XOR function realized using 4 NAND gates.  
3. **Binary → Gray Logic** — implemented using XOR chaining:
   - G1 = A  
   - G2 = A ⊕ B  
   - G3 = B ⊕ C  
   - G4 = C ⊕ D  
4. **Full 4-bit Converter** — constructed using three XOR gates, tested against truth table.  
5. **Validation** — transient analysis + truth table comparison ensured correctness.  

---

## 🛠 Tools & environment
- **Cadence Virtuoso** (schematic, layout, simulation)  
- **Layout XL** (for DRC & LVS checks)  
- **Spectre ADE** (transient simulations)  
- **GPDK 90nm PDK**  

