# Cumene Process Design & Techno-Economic Analysis
Conceptual design, process simulation, equipment sizing, and techno-economic assessment of an industrial cumene production process from benzene and propylene.

This project was developed as a preliminary chemical process design study and covers the complete workflow from process selection and capacity estimation to Aspen HYSYS simulation, mass and energy balances, heat integration, equipment sizing, CAPEX/OPEX estimation, and economic evaluation.

---

## Project Overview

Cumene is produced through the catalytic alkylation of benzene with propylene:

Benzene + Propylene → Cumene

The process was designed based on the Luyben cumene process configuration and simulated using Aspen HYSYS V14.

The final process includes:

- Benzene and C3 feed preparation
- Feed vaporization
- Feed-effluent heat integration
- Kinetic packed-bed reactor
- Pressure reduction and cooling
- Flash separation
- Benzene recovery and recycle
- Cumene purification
- PDIB by-product separation

---

## Process Simulation

The Aspen HYSYS model includes the following components:

- Benzene
- Propylene
- Propane
- Cumene
- Diisopropylbenzene (PDIB)

### Main Simulation Features

- Thermodynamic model: NRTL
- Reactor model: Kinetic Packed-Bed / Plug-Flow Reactor
- Reactor tubes: 1500
- Reactor feed temperature: 358 °C
- Reactor pressure: 25 bar
- Benzene recycle loop
- Flash separation
- Two distillation columns
- Converged Recycle and Adjust operations

---

## Reaction Scheme

### Main Reaction

Benzene + Propylene → Cumene

### Side Reaction

Cumene + Propylene → PDIB

The process was designed to achieve high propylene conversion while limiting the formation of the heavier PDIB by-product.

The main design challenge is therefore not only achieving high conversion, but also maintaining high selectivity toward cumene.

---

## Process Flow
```text
Fresh Benzene + Fresh C3
            |
            v
       Feed Mixing
            |
            v
        Vaporizer
            |
            v
Feed-Effluent Heat Exchanger
            |
            v
       Final Heater
            |
            v
   Packed-Bed Reactor
            |
            v
     Heat Recovery
            |
            v
   Pressure Reduction
            |
            v
         Cooler
            |
            v
      Flash V-100
       /        \
     Gas       Liquid
                 |
                 v
        Benzene Recovery C1
             |
      Benzene Recycle
             |
        C1 Bottoms
             |
             v
      Cumene Column C2
         /         \
      Cumene       PDIB
```

---

## Separation and Benzene Recycle

After the reaction section, the reactor effluent is cooled and sent to Flash V-100.

The flash separator removes the lighter components, mainly propane and residual unreacted propylene.

The liquid stream is then sent to the first distillation column:

### C1 — Benzene Recovery Column

The main purpose of C1 is to recover unreacted benzene.

Recovered benzene is recycled back to the reactor feed, reducing fresh benzene consumption and improving overall process economics.

### C2 — Cumene Purification Column

The bottom stream of C1 is sent to C2.

C2 separates:

- High-purity cumene as the main product
- Heavy PDIB by-product from the bottom

The final cumene product reaches approximately:

99.90 mol% purity

---

## Key Process Results

| Parameter | Result |
|---|---:|
| Fresh benzene feed | 40.00 t/h |
| Fresh C3 feed | 21.94 t/h |
| Cumene production | 56.79 t/h |
| Annual cumene capacity | 449.76 kt/y |
| Cumene purity | 99.90 mol% |
| PDIB production | 1.17 t/h |
| Reactor feed temperature | 358 °C |
| Reactor pressure | 25 bar |
| Cumene-path conversion | 96.62% |
| PDIB formation | 1.493% |
| Benzene recycle | 107.2 kmol/h |
| Flash gas flow | 11.92 kmol/h |
| PDIB bottoms | 1.413 kmol/h |

---

## Heat Integration & Utilities

Heat integration was incorporated into the process to reduce external utility consumption.

The main heat-integration features include:

- Feed-effluent heat exchange
- Reactor heat recovery- Preheating of reactor feed
- Cooling before flash separation
- Condenser duties for both distillation columns
- Reboiler duties for both distillation columns

### Selected Design-Scale Duties

| Equipment | Duty |
|---|---:|
| Vaporizer VAP-100 | 19.23 MW |
| HX2 Cooling | 17.96 MW |
| Reactor heat recovery | 12.95 MW |
| C1 Condenser | 7.46 MW |
| C1 Reboiler | 9.89 MW |
| C2 Condenser | 6.42 MW |
| C2 Reboiler | 5.55 MW |
| HX1 | 1.76 MW |

The reactor is exothermic, and approximately 12.95 MW of heat is potentially recoverable at the final design capacity.

This recovered heat can potentially be used for steam generation or other process heating requirements.

---

## Equipment Sizing

Preliminary equipment sizing was performed for the major process equipment.

The sizing calculations were carried out at the conceptual/preliminary design level.

### Packed-Bed Reactor — PBR-100

- Number of tubes: 1500
- Tube length: 6 m
- Tube internal diameter: 76.2 mm
- Catalyst bed volume: ~41 m³
- Catalyst mass: ~41 tonnes
- Reactor diameter: ~4.4 m
- Total reactor length: ~7.5 m
- Bed void fraction: 0.50

The reactor size was selected to allow high propylene conversion at a relatively moderate temperature while limiting the formation of PDIB.

---

### Benzene Recovery Column — C1

- Actual trays: ~30
- Diameter: ~1.52 m
- Height: ~22.5 m
- Main function: Benzene recovery and recycle

The actual number of trays was estimated from theoretical stages using tray-efficiency correlations.

---

### Cumene Purification Column — C2

- Actual trays: ~37
- Diameter: ~1.49 m
- Height: ~26.35 m
- Main function: Cumene / PDIB separation

The purpose of this column is to obtain high-purity cumene while removing the heavier PDIB by-product from the bottom.

---

### Flash Separator — V-100

- Vessel volume: ~5.0 m³
- Diameter: ~1.17 m
- Length: ~4.67 m
- Approximate residence time: 5 min

The flash separator removes light gases before the liquid stream enters the distillation section.

---

### Heat Exchangers

Preliminary heat-exchanger sizing was carried out using:

- Heat duty
- Overall heat-transfer coefficient
- Log Mean Temperature Difference (LMTD)
- LMTD correction factor
- Pressure-drop considerations

Example calculated heat-transfer areas include:

- FEHE: ~55 m²
- E-101: ~121 m²

Shell-and-tube configurations were selected based on thermal and mechanical design considerations.

---

### Benzene Recycle Pump — P-100

The recycle pump increases the pressure of recovered benzene before returning it to the high-pressure reactor feed section.

Approximate calculated pump head:

~293 m

---

## Mass Balance

At full design capacity:

| Stream | Flow Rate | Annual Flow |
|---|---:|---:|
| Fresh Benzene | 40.00 t/h | 316.80 kt/y |
| Fresh C3 | 21.94 t/h | 173.79 kt/y |
| Cumene Product | 56.79 t/h | 449.76 kt/y |
| PDIB Bottoms | 1.17 t/h | 9.27 kt/y |

The benzene recycle loop reduces feed losses and improves raw-material utilization.

---

## Techno-Economic Evaluation

A preliminary techno-economic analysis was performed using estimated equipment costs, capital investment, operating costs, product revenue, and discounted cash-flow analysis.

### Capital Investment

| Parameter | Result |
|---|---:|
| Fixed Capital Investment (FCI) | ~$18.45M |
| Total Capital Investment (TCI) | ~$21.70M |

Working capital was included in the calculation of total capital investment.

---

### Annual Economic Results

| Parameter | Result |
|---|---:|
| Annual Revenue | ~$116.16M/y |
| Total Production Cost | ~$112.28M/y |
| Gross Profit | ~$3.88M/y |
| Net Profit | ~$2.36M/y |

The economic performance is strongly influenced by feedstock prices, especially benzene and propylene.

---

## Economic Indicators

| Economic Indicator | Result |
|---|---:|
| NPV | ~$1.96M |
| IRR | 21.3% |
| ROI | 20% |
| Payback Period | 7.5 years |
| Minimum Acceptable Rate of Return | 18% |

Under the assumptions used in this preliminary study:

IRR > Minimum Acceptable Rate of Return

and

NPV > 0
Therefore, the project was considered economically feasible under the selected assumptions.
However, the economic margin is sensitive to:

- Benzene price
- Propylene price
- Cumene selling price
- Utility costs
- Financing conditions
- Process selectivity
- PDIB formation

A more detailed sensitivity analysis would be required before an industrial investment decision.

---

## Tools & Methods

### Software

- Aspen HYSYS V14
- Microsoft Excel

### Engineering Methods

- Chemical Process Simulation
- Reaction Kinetics
- Mass Balance
- Energy Balance
- Process Flow Diagram Development
- Packed-Bed Reactor Modeling
- Distillation Design
- Flash Separation
- Heat Integration
- Heat Exchanger Sizing
- Vessel Sizing
- Pump Sizing
- Equipment Cost Estimation
- CAPEX Estimation
- OPEX Estimation
- Discounted Cash Flow Analysis
- NPV Analysis
- IRR Analysis
- ROI Analysis
- Payback Period Analysis

---

## Repository Contents
```text
.
├── hysys/
│   └── cumene-process-hysys.hsc
│
├── report/
│   └── cumene-process-design.pdf
│
├── excel/
│   └── cumene-process-economic-evaluation.xlsx
│
└── README.md
```

---

## Simulation Requirements

The process simulation was developed using:

Aspen HYSYS V14

The .hsc file contains the converged Aspen HYSYS case.

Opening the simulation using another Aspen HYSYS version may require file conversion or compatibility adjustments.

---

## Project Scope

This project represents a:

Preliminary / Conceptual Chemical Process Design

It is not intended to represent a complete detailed engineering package.

Further development would require:

- Detailed mechanical design
- Process control system design
- Dynamic simulation
- HAZOP study
- Relief-system design
- Detailed piping design
- P&ID development
- Instrumentation design
- Utility-network optimization
- Detailed environmental assessment
- Updated equipment quotations
- Detailed market analysis
- Economic sensitivity analysis

---

## Key Engineering Insight

The main technical challenge of the cumene process is not simply achieving high propylene conversion.

The process must simultaneously achieve:

High Conversion + High Cumene Selectivity + Low PDIB Formation

This requires balancing:

- Reactor temperature
- Reactor size
- Benzene-to-propylene ratio
- Benzene recycle
- Separation energy
- Feedstock cost

The technical and economic performance of the process are therefore strongly interconnected.

---

## Reference

The process configuration and kinetic basis were primarily developed based on:

William L. Luyben  
"Design and Control of the Cumene Process"  
Industrial & Engineering Chemistry Research  
2010, 49, 719–734.

---

## Author

Chemical Process Design Project

Aspen HYSYS V14 | Process Simulation | Equipment Sizing | Techno-Economic Analysis
