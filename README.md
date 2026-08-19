# Multimodal Arc Analysis in HyperFill GMAW

Experimental and computational study of arc behaviour in **HyperFill Twin-Wire Pulsed Gas Metal Arc Welding (TWGMAW-P)**, focusing on electrical waveform characterization and computational methods for optical arc and plasma diagnostics.

## Overview

This project was carried out as part of a Summer Research Internship at the **Smart Welding and Additive Manufacturing (SWAAM) Laboratory, IIT Tirupati**, under the guidance of **Dr. D. V. Kiran**.

The work involved experimental characterization of HyperFill GMAW using synchronized current-voltage measurements, followed by computational studies of optical diagnostic techniques including **Abel inversion** and the **Fowler-Milne method**.

The project also involved studying **high-speed imaging as a multimodal diagnostic technique** for future arc characterization and applying **multiple linear regression in Minitab** for welding-parameter analysis.

## Objectives

* Characterize the electrical behaviour of HyperFill twin-wire pulsed GMAW.
* Analyse current-voltage waveforms at different nominal welding conditions.
* Identify pulse peaks, baseline behaviour, waveform periodicity and frequency.
* Study optical diagnostic methods for reconstructing radial arc properties.
* Investigate Abel inversion for radial emissivity or irradiance reconstruction.
* Study the Fowler-Milne method for plasma-temperature diagnostics.
* Explore high-speed imaging for time-resolved arc characterization.
* Analyse relationships between welding parameters and measured responses using multiple linear regression in Minitab.

## Experimental Setup

The HyperFill experiments were conducted using:

* **Welding Process:** HyperFill Twin-Wire Pulsed GMAW (TWGMAW-P)
* **Power Source:** Lincoln Electric Power Wave S500
* **Consumable:** ER70S-6 solid welding wire
* **Wire Diameter:** 1 mm
* **Workpiece:** Low-carbon steel, 10 mm thickness
* **Shielding Gas:** 80% Ar + 20% CO₂
* **Data Acquisition:** Dewesoft X
* **Nominal Current:** 150 A, 200 A and 250 A
* **Set Voltage:** 22.5 V, 23.9 V and 25.3 V
* **CTWD:** 20 mm
* **Polarity:** DCEP

The experimental campaign consisted of three bead-on-plate HyperFill trials.

## Electrical Waveform Analysis

Current and voltage signals were acquired using **Dewesoft X** and analysed to characterize the pulsed electrical response of the HyperFill process.

Key observations included:

* Instantaneous current peaks in the approximate range of **550–600 A**.
* Current baseline increasing with nominal operating current.
* Corresponding voltage response during current pulses.
* Increasing apparent pulse frequency with increasing nominal current.

For the three trials, the reported current peaks were approximately:

| Nominal Current | Current Peak | Voltage Peak | Frequency |
| --------------: | -----------: | -----------: | --------: |
|           150 A |        588 A |      40.66 V |   16.8 Hz |
|           200 A |        577 A |      39.75 V |  50–53 Hz |
|           250 A |        578 A |      40.53 V |  66–70 Hz |

The higher-frequency values were estimated from the waveform records and require verification against the raw Dewesoft X time-series data.

## High-Speed Imaging

High-speed imaging was considered as part of the **multimodal arc-characterization workflow** for resolving transient arc behaviour, arc geometry and metal-transfer phenomena.

The supplied HyperFill experimental report notes that a high-speed camera was **not available during the three reported HyperFill trials**. Therefore, this repository does not claim synchronized high-speed imaging results for those three experiments.

Where applicable, high-speed imaging analysis can be used alongside electrical measurements to investigate transient arc behaviour and establish correlations between waveform events and visual arc phenomena.

## Abel Inversion

A MATLAB implementation of **Abel inversion** was studied for reconstructing radial emissivity or irradiance distributions from line-of-sight optical intensity measurements.

### Workflow

1. Load arc/plasma image
2. Select the sampling region
3. Extract a one-dimensional intensity profile
4. Normalize the intensity distribution
5. Construct the discretized inverse problem
6. Perform numerical inversion
7. Obtain the radial emissivity/irradiance profile
8. Apply filtering and post-processing

The supplied implementation used a discrete area-matrix approach rather than directly evaluating the continuous Abel inversion equation.

## Fowler-Milne Plasma Diagnostics

The **Fowler-Milne method** was studied as a spectroscopic technique for estimating plasma temperature from suitable optical emission measurements.

The computational workflow involved:

* Optical emission data
* Intensity normalization
* Reference Fowler-Milne relationship
* Temperature mapping
* Spatial interpretation of the resulting temperature distribution

The method was studied using a separate arc/plasma dataset and was not applied to the three HyperFill electrical trials.

## Multiple Linear Regression

**Minitab** was used for multiple linear regression analysis to investigate relationships between welding parameters and measured response variables.

The regression workflow includes:

* Defining welding parameters as predictor variables
* Selecting the measured response
* Fitting a multiple linear regression model
* Evaluating coefficient significance
* Examining model fit
* Identifying influential process variables
* Interpreting parameter-response relationships

The regression analysis is intended to provide a statistical basis for understanding how process parameters influence the measured welding response.

## Tools & Technologies

**Welding & Instrumentation**

* Lincoln Electric Power Wave S500
* HyperFill TWGMAW-P
* Dewesoft X
* High-Speed Imaging

**Numerical & Data Analysis**

* MATLAB
* Minitab
* Multiple Linear Regression
* Abel Inversion
* Fowler-Milne Method

**Engineering Domain**

* Gas Metal Arc Welding
* Twin-Wire Pulsed GMAW
* Arc Characterization
* Electrical Waveform Analysis
* Optical Plasma Diagnostics

## Repository Structure

```text
Multimodal-Arc-Analysis-in-Hyper-Fill-GMA/
│
├── MATLAB/
│   ├── Abel_Inversion/
│   └── Fowler_Milne/
│
├── Minitab/
│   └── Regression_Analysis/
│
├── Waveform_Analysis/
│   ├── Current/
│   ├── Voltage/
│   └── Results/
│
├── High_Speed_Imaging/
│   └── README.md
│
├── Results/
│   ├── Figures/
│   └── Tables/
│
├── Report/
│   └── Internship_Report.pdf
│
└── README.md
```

## Key Outcomes

* Characterized the pulsed electrical response of HyperFill TWGMAW-P at three nominal current conditions.
* Identified instantaneous current peaks of approximately **550–600 A**.
* Analysed changes in current baseline, voltage response and pulse frequency.
* Studied MATLAB-based **Abel inversion** for radial optical-profile reconstruction.
* Studied the **Fowler-Milne method** for plasma-temperature diagnostics.
* Applied **multiple linear regression in Minitab** for welding-parameter correlation.
* Established a computational foundation for future multimodal arc characterization combining electrical, optical and imaging measurements.

## Project Context

This repository accompanies the Summer Research Internship:

**Multimodal Arc Stability Study in HyperFill GMAW**
Smart Welding and Additive Manufacturing Laboratory
Indian Institute of Technology Tirupati
May 2026 – August 2026

**Academic Supervisor:** Dr. D. V. Kiran
