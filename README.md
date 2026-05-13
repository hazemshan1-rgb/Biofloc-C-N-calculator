🦠 Biofloc C:N & Alkalinity Calculator
Stop guessing. Start dosing.
A free, research-backed calculator for biofloc shrimp farmers who are tired of ammonia spikes, pH crashes, and dead crops.
Built by: Hazem Shannak · Regenerative Seawater Aquaculture (RSA)
Live demo: yourusername.github.io/biofloc-calculator
Based on: Avnimelech (2009), SRAC 4503, Boyd & Hargreaves
🔥 The Problem This Solves
Every biofloc farmer faces the same daily nightmare:
"How much molasses do I add today?" → You guess. Sometimes it works. Sometimes ammonia spikes and kills 30% of your crop.
"My pH crashed overnight." → You forgot to buffer alkalinity while adding carbon.
"I added carbon but DO dropped." → Bacteria consumed all the oxygen. Your shrimp suffocated.
"I don't know if my C:N ratio is actually 15:1." → You have no nitrogen budget. You're flying blind.
This calculator replaces gut feeling with stoichiometry.
⚡ What It Does
1. Dual-Mode Dosing Engine
Table
Mode	When to Use	Output
Feed-Based Prevention	Daily maintenance	Exact kg of carbon source needed based on today's feeding rate
TAN-Based Correction	Emergency spike	Carbon dose to bring measured TAN down to target level
2. Risk Dashboard
Real-time color-coded risk assessment based on:
TAN (Total Ammonia Nitrogen)
Nitrite (NO₂)
Dissolved Oxygen (DO)
Alkalinity
Risk levels: LOW → MODERATE → HIGH → CRITICAL
Critical triggers emergency action protocols.
3. Application Scheduler
Tells you when to dose, not just how much:
≤2 kg → 2 splits (08:00, 16:00)
≤10 kg → 3 splits (08:00, 12:00, 16:00)
10 kg → 4 splits (06:00, 10:00, 14:00, 18:00)
Plus: "Increase aeration 30 min BEFORE first dose" warnings.
4. Alkalinity Management
Calculates NaHCO₃ needed to reach target alkalinity
Daily maintenance dose based on feed rate (SRAC 4503 guideline: 0.25 kg NaHCO₃ per kg feed)
pH crash warnings when alkalinity < 80 mg/L
5. Oxygen Impact Prediction
Estimates O₂ demand from carbohydrate addition
Predicts post-dosing DO level
Prevents the #1 carbon-dosing mistake: hypoxia
6. Nitrogen Budget
N load from feed (g/day)
Carbon supplied by feed waste vs. supplemental needed
Estimated assimilation efficiency
Residual nitrogen warning
7. Biofloc Biomass Estimation
Predicted bacterial biomass production (g/day)
Estimated TSS contribution
🧪 The Science Behind It
Nitrogen Load from Feed
plain
Copy
N load (g/day) = Feed (kg) × 1000 × (Protein% / 100) / 6.25 × 0.5
Protein is 16% nitrogen (hence ÷ 6.25)
50% of feed nitrogen is excreted as TAN (metabolic + uneaten degradation)
Carbon Requirement
plain
Copy
Total C needed (g) = N load (g) × Target C:N ratio
Supplemental C (g) = Total C needed - Carbon from feed waste
Feed waste provides ~50% of its dry matter as carbon
Dry matter fraction: 90%
Waste fraction (uneaten + feces): 70%
Carbon Source Conversion
plain
Copy
Source mass (kg) = Supplemental C (g) / Source carbon fraction / 1000
Table
Source	Carbon Fraction	Notes
Molasses	22%	Liquid, widely available
Sugar (Sucrose)	42%	Pure, dissolves fast
Tapioca Starch	46%	High C%, popular in SE Asia
Corn Starch	44%	Slow release
Rice Bran	35%	Local, cheap in Asia
Wheat Flour	40%	Moderate solubility
Jaggery	40%	Traditional India
Alkalinity (NaHCO₃)
plain
Copy
NaHCO₃ (kg) = max(0, (Target Alk - Current Alk) × Volume (m³) × 1.5 / 1000)
The 1.5 factor accounts for molecular weight ratio (84/100 = 0.84), reaction efficiency, and ongoing depletion.
Oxygen Demand
plain
Copy
O₂ demand (kg) = Source mass (kg) × Carbon fraction × 1.07
1.07 mg O₂ consumed per mg carbohydrate oxidized (Boyd & Hargreaves)
Biofloc Biomass
plain
Copy
Biomass (g) = Assimilated N (g) / 0.10
Bacterial cells are ~10% nitrogen by weight
Assimilation efficiency: ~80% at optimal C:N
🚀 How to Use
Quick Start
Open the live calculator
Enter your pond volume and water parameters
Enter today's feed rate and protein %
Select your target C:N ratio and carbon source
Click "Calculate Dose"
Follow the split-dose schedule
For Startup BFT (Days 1–30)
Set C:N ratio to 15:1 or 20:1
Use molasses or sugar (fast-dissolving)
Target alkalinity: 120–150 mg/L
Test TAN twice daily
For Mature BFT (Day 30+)
Set C:N ratio to 6:1 or 10:1
Switch to tapioca or corn starch (slow release, cheaper)
Target alkalinity: 100–120 mg/L
Test TAN once daily
Emergency Protocol (TAN > 4 mg/L or NO₂ > 5 mg/L)
The calculator will automatically trigger:
STOP feeding
Double the normal carbon dose — split in 4 applications over 12h
Max out aeration before first dose
Test water again in 4 hours
Prepare for partial harvest if mortality > 5%
📱 Mobile-First Design
This calculator is built for the field:
Works on $100 Android phones
No app download needed — runs in browser
Loads in < 2 seconds on 3G
Offline-capable (cache-enabled)
Large touch targets for wet hands
🎯 Who This Is For
Biofloc shrimp farmers (indoor, outdoor, RAS)
Hatchery operators running maturation BFT
Aquaculture students learning C:N stoichiometry
Extension agents advising small-scale farmers
Feed companies wanting to bundle a value-add tool
⚠️ Disclaimer
This calculator is an educational decision-support tool, not a replacement for professional aquaculture management. Always:
Verify calculations with your farm manager
Test water parameters with a reliable kit
Adjust for local conditions (temperature, salinity, species)
Consult a veterinarian or aquaculture specialist for disease outbreaks
The author assumes no liability for crop loss based on calculator outputs.
🛠️ Tech Stack
Pure HTML/CSS/JS — no frameworks, no dependencies
Vanilla JavaScript — runs in any browser
GitHub Pages — free hosting
MIT License — use it, fork it, improve it
🗺️ Roadmap
[x] Core C:N engine (feed-based + TAN-based)
[x] Risk dashboard with emergency protocols
[x] Alkalinity management
[x] Oxygen impact prediction
[x] Split-dose scheduler
[ ] Multi-pond dashboard (premium)
[ ] Historical data logging (premium)
[ ] WhatsApp summary generator
[ ] Price optimization integration
[ ] Spanish, Portuguese, Bahasa Indonesia, Thai, Vietnamese localization
🤝 Contribute
Found a bug? Want to add a carbon source? Submit a PR:
Fork this repository
Edit index.html
Test your changes
Submit a pull request
Or open an issue with your suggestion.
📬 Connect
LinkedIn: Hazem Shannak
Newsletter: The Seawater Farmer (coming soon)
Consulting: hazem@yourdomain.com (replace with your real email)
Built with 🦐 and stoichiometry.
📚 References
Avnimelech, Y. (2009). Biofloc Technology — A Practical Guide Book. World Aquaculture Society.
Boyd, C.E. & Hargreaves, J.A. (2021). Water Quality and Pond Soil Analyses for Aquaculture. SRAC Publication 4603.
Ebeling, J.M. et al. (2006). Engineering Analysis of the Stoichiometry of Photoautotrophic, Autotrophic, and Heterotrophic Removal of Ammonia-Nitrogen in Aquaculture Systems. Aquacultural Engineering.
QB Labs (2024). Biofloc C:N Ratio Calculator — proprietary tool (inspired independent version).
Global Shrimp Forum (2025). Industry reports on biofloc adoption and farmer pain points.
📄 License
MIT License — see LICENSE file.
"The farmer who measures, manages. The farmer who guesses, gambles."
— Hazem Shannak
