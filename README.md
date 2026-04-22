# Open-SDS-PAGE-PhotoPolymer: Glyxon Blue-Light System 🧬💡

[![License: AGPL v3](https://img.shields.io/badge/License-AGPL%20v3-blue.svg)](https://www.gnu.org/licenses/agpl-3.0)

This repository contains the full protocol, Bill of Materials (BOM), and optimized recipes for performing protein electrophoresis (SDS-PAGE) using a **Blue-Light Photopolymerization system (475 nm)**. 

Developed by **Glyxon Biolabs**, this method eliminates reliance on toxic, short-shelf-life reagents like TEMED and APS, replacing them with a robust Riboflavin/EDTA system and low-cost, off-the-shelf hardware.

---

## 🛠️ Bill of Materials (BOM)

### 🖼️ Hardware & Glassware
* **Glass Plates (1.0 mm thickness):** Short and spacer glass plates with integrated spacers.
    * [AliExpress Link - Glass Plates](https://es.aliexpress.com/item/1005008212963394.html)
* **Electrophoresis Combs (10-well, 1mm):** Standard-compatible combs.
    * [AliExpress Link - 10-well 1mm Combs](https://es.aliexpress.com/item/1005009794120855.html)
* **WS2812B RGB LED Matrix (8x8):** 64-pixel addressable LED panel for curing.
    * [AliExpress Link - 8x8 Digital RGB LED Panel](https://es.aliexpress.com/item/1005005937649744.html)
* **Frugal Casting Setup (Alternative):** If a commercial gel caster is unavailable, you can achieve a perfect seal using:
    * **White Electrical Tape:** To seal the sides and bottom of the glass sandwich.
    * **Small Binder Clips:** To maintain uniform pressure. [Example: Officemate Binder Clips](https://www.amazon.com.mx/Officemate-Easy-Grip-met%C3%A1licas-peque%C3%B1as/dp/B008OIB4AK)

### 🧪 Chemical Reagents
* **Acrylamide/Bis-acrylamide 29:1 (30% Solution):** Original Biosharp electrophoresis grade.
    * [AliExpress Link - BIOSHARP 30% Sol.](https://es.aliexpress.com/item/1005008711267671.html?gatewayAdapt=glo2esp)
* **Vitamin B2 (Riboflavin) 100 mg:** Stable photo-initiator capsules.
    * [iHerb Link - Nutricost Vitamin B2](https://mx.iherb.com/pr/nutricost-vitamin-b2-100-mg-30-capsules/145446)
* **EDTA 0.1 M Solution:** Standardized J.T. Baker catalyst.
    * [El Crisol Link - EDTA 0.1M (1L)](https://elcrisol.com.mx/edta-0-1m-de-1l-jt-baker.html)

### 📱 Software & Control
* **Zengge BLE (Bluetooth V2):** Mobile app for precise wavelength and intensity control.
    * [Google Play Store - Zengge BLE](https://play.google.com/store/apps/details?id=com.zengge.blev2&hl=es_MX)

---

## 🧪 Buffer Stock Preparation (30 ml Batches)

| Buffer Type | Concentration | Tris Base Mass | Target pH |
| :--- | :--- | :--- | :--- |
| **Resolving** | 1.5 M | 5.45 g | 8.8 |
| **Stacking** | 0.5 M | 1.82 g | 6.8 |

### Procedure:
1. Dissolve the Tris Base in ~20 ml of deionized water.
2. Adjust pH using concentrated HCl dropwise (Caution: exothermic reaction).
3. Once stabilized, bring the final volume to 30 ml using a volumetric flask or precision cylinder.
4. **Lab Tip:** Store in airtight containers to prevent CO2 absorption, which can shift the pH over time.

---

## 🧪 Master Recipes (Optimized Laemmli System)

### 1. Resolving Gel (12% Acrylamide)
*Total Volume: ~6.0 ml (Optimized for 1.0 mm plates)*

| Component | Volume | Function |
| :--- | :--- | :--- |
| Acrylamide/Bis (30%) | 2.4 ml | Gel matrix |
| Tris-HCl 1.5 M (pH 8.8) | 1.5 ml | Resolving buffer |
| SDS 10% | 60 µl | Denaturing agent |
| Deionized Water | 1.9 ml | Solvent |
| **EDTA 0.1 M** | **50 µl** | Catalyst / Stabilizer |
| **Riboflavin (0.1%)** | **100 µl** | Photo-initiator |

### 2. Stacking Gel (Recommended: 6% Acrylamide)
*Total Volume: ~2.5 ml. Optimized for faster polymerization and rigid well definition.*

| Component | Volume | Function |
| :--- | :--- | :--- |
| Acrylamide/Bis (30%) | **0.5 ml** | Gel matrix (6%) |
| Tris-HCl 0.5 M (pH 6.8) | 0.63 ml | Stacking buffer |
| SDS 10% | 25 µl | Denaturing agent |
| Deionized Water | 1.28 ml | Solvent |
| **EDTA 0.1 M** | **40 - 50 µl** | Catalyst (Increased) |
| **Riboflavin (0.1%)** | **80 - 100 µl** | Initiator (Increased) |

---

## 🏗️ Operational Protocol

### 1. Casting & Photopolymerization
1. **Assembly:** Setup the glass plates. Use **white electrical tape** and **binder clips** for a frugal seal if a commercial caster is not available.
2. **Resolving Gel:** Pour the 12% mix and overlay with **300 µl of Isopropanol** to level the surface.
3. **Exposure I:** Place the LED matrix as close as possible to the glass. Set to **Solid Blue (475 nm)** at 100% intensity via the App. 
   * **Duration:** 45 - 60 minutes.
4. **Washing:** Remove the isopropanol, rinse with distilled water, and dry carefully with filter paper.
5. **Stacking Gel:** Pour the **6% mix**, insert the comb, and expose to blue light again.
   * **Glyxon Pro-Tip:** Increasing EDTA/Riboflavin concentrations in the stacking gel significantly accelerates the process and ensures well integrity.
   * **Duration:** 30 - 45 minutes.



### 2. Running Protocol (Voltage & Timings)
Using **1X Running Buffer (Tris-Glycine-SDS)**:
* **Step 1 (Stacking/Focusing):** Run at **80V** constant until the dye front (Bromophenol Blue) passes the stacking gel and forms a sharp line at the interface (~15-20 min).
* **Step 2 (Resolution):** Increase to **120V** (High Resolution) or **150V** (Fast Run). 
  * *Note: At 150V, monitor for heat generation to protect the silicone gasket or tape seal.*
* **Completion:** Stop the power supply when the dye front is **0.5 cm** from the bottom edge.

---

## 📚 Scientific References
* [ACS Analytical Chemistry - doi:10.1021/ac049686u](https://pubs.acs.org/doi/10.1021/ac049686u)
* [PubMed - PMID: 35895218](https://pubmed.ncbi.nlm.nih.gov/35895218/)

---

## 📩 Contact
For inquiries, collaborations, or technical support: **glyxonbiolabs@gmail.com**

## 📜 License (Technical Sovereignty)
This project is licensed under the **GNU Affero General Public License v3.0 (AGPL-3.0)**. 
> "The science released by Glyxon remains free. Any network-distributed improvements to this software or protocol must be shared under the same terms."

---
**Developed by David J. Castillo - Glyxon Biolabs** 🧪🚀
