## Effect of Habitat on the Photophysiology of Algae Using Pulse-Amplitude Modulated (PAM) Fluorometry
#### Aim

Determine whether habitat influences the photophysiology of algae by comparing chlorophyll fluorescence parameters among algal specimens collected from different environmental conditions. Specifically, Pulse-Amplitude Modulated (PAM) fluorometry was used to quantify photosynthetic efficiency and photoprotective responses in algae originating from a sun exposed "light" habitat compared to a shaded "dark" habitat.

#### Experimental Design
- Comparative study  
- Independent Variable:  
    1. High-light exposure habitat - "light"  
    2. Low-light exposure habitat - "dark"  
- Dependent variables:
    1. Dark-adapted parameters  
        - Minimum fluorescence (Fo)  
        - Maximum fluorescence (Fm)  
        - Variable fluorescence (Fv)  
    2. Light-adapted parameters  
        - Electron transport rate (ETR)  
        - Effective quantum yield (ΦPSII)  
        - Non-photochemical quenching (NPQ)  
    3. Rapid Light Curve (RLC) parameters  
        - Initial slope of Fv/Fm (α or AQY)  
        - Dark respiration (Rd)  
        - Maximum electron transport rate (ETRmax)  
        - Saturation irradiance (Ik or Ek)  
        - Asymptotic maximum (Am) = max photosynthesis (Pmax)  

#### Materials and Methods

- Algae specimens were collected from two habitat types  
- Both habitats were fully subtidal on the tidal platforms of Sdot Yam  
- Pulse-Amplitude Modulated (PAM) measurements were conducted for two groups:  
    1. 12 algae samples taken from "light" habitat   
    
    !["Light" algae plate]({{site.baseurl}}/images/L_plate.JPG)  

    2.  9 algae samples taken from "dark" habitat  

    !["Dark" algae plate]({{site.baseurl}}/images/D_plate.JPG)  

- Specimens were detached from their substrate, placed into labelled zip-lock bags containing habitat water, and transported to the laboratory for analysis.
- Species were identified to genus level using morphological characteristics
- Prior to dark fluorescence measurements, specimens were dark-adapted for 30 min to allow all PSII reaction centres to open  
- PAM fluorometry was used to assess algal photophysiology  
- Two datasets were collected for each group:  
    1. Light-adapted fluorescence measurements  

    !["Light" algae in PAM program]({{site.baseurl}}/images/L_PAM.jpg)  
    
    2. Dark-adapted fluorescence measurements  

    !["Light" algae in PAM program]({{site.baseurl}}/images/D_PAM.jpg)  

> See files "dark.csv" and "light.csv"

- Calculated Parameters:  
    1. Variable Fluorescence -> Fv = Fm − Fo  
    2. Maximum Quantum Yield -> Fv / Fm  
    3. Effective Quantum Yield (ΦPSII) and Electron Transport Rate (ETR) were calculated by the PAM program as raw data.  
- Rapid Light Curve Parameters were drived from R code calculations.  

#### Results

- Raw Data  
    1. [Dark raw data](https://github.com/YonscarS/YoS--LabBook/blob/main/_posts/R_Photopysiology/dark.csv)  
    2. [Light raw data](https://github.com/YonscarS/YoS--LabBook/blob/main/_posts/R_Photopysiology/light.csv)  
- [Metadata](https://github.com/YonscarS/YoS--LabBook/blob/main/_posts/R_Photopysiology/Photophysiology_metadata.csv)  

| **Group** | **Sample** | **Taxon** | **Sample_ID** |  
|-----------|------------|-----------|---------------|  
| Dark | 1 | Colpomenia | Dark_1 |  
| Dark | 2 | Dictyota | Dark_2 |  
| Dark | 8 | Galxaura | Dark_8 |  
| Dark | 5 | Jania | Dark_5 |  
| Dark | 4 | Padina | Dark_4 |  
| Dark | 6 | Red UNK | Dark_6 |  
| Dark | 3 | Sargassum | Dark_3 |  
| Dark | 7 | Ulva | Dark_7 |  
| Light | 8 | Cistosera | Light_8 |  
| Light | 12 | Colpomenia | Light_12 |  
| Light | 6 | Cudiom | Light_6 |  
| Light | 11 | Dictyota | Light_11 |  
| Light | 10 | Galaxaura | Light_10 |  
| Light | 2 | Halopteris | Light_2 |  
| Light | 5 | Hypnea | Light_5 |  
| Light | 1 | Jania | Light_1 |  
| Light | 3 | Namaliun | Light_3 |  
| Light | 7 | Padina | Light_7 |  
| Light | 4 | Sargassum | Light_4 |  
| Light | 9 | Ulva | Light_9 |  
| Light | 13 | Ulva | Light_13 |  

- [Calculated photophysiology parameters](https://github.com/YonscarS/YoS--LabBook/blob/main/_posts/R_Photopysiology/Calc_parameters.csv)

| **Sample_ID** | **Am** | **AQY** | **Rd** | **Ik** | **Taxon** | **Group** |  
|---------------|--------|---------|--------|--------|-----------|-----------|  
| Light_1 | 33.253 | 0.124 | -0.392 | 267.871 | Jania | Light |  
| Light_2 | 6.483 | 0.114 | -0.074 | 56.989 | Halopteris | Light |  
| Light_4 | 30.126 | 0.153 | -0.670 | 196.921 | Sargassum | Light |
| Light_5 | 23.410 | 0.163 | 0.054 | 143.221 | Hypnea | Light |  
| Light_6 | 8.827 | 0.139 | 0.136 | 63.327 | Cudiom | Light |  
| Light_7 | 47.082 | 0.184 | -0.557 | 255.716 | Padina | Light |  
| Light_8 | 13.887 | 0.142 | -0.030 | 97.658 | Cistosera | Light |  
| Light_10 | 7.948 | 0.122 | -0.121 | 64.951 | Galaxaura | Light |  
| Light_11 | 31.169 | 0.139 | 0.054 | 224.111 | Dictyota | Light |  
| Light_12 | 16.828 | 0.123 | -0.136 | 137.065 | Colpomenia | Light |  
| Light_13 | 17.731 | 0.099 | -0.085 | 179.804 | Ulva | Light |  
| Dark_1 | 33.960 | 0.208 | -0.345 | 163.607 | Colpomenia | Dark |  
| Dark_2 | 12.813 | 0.308 | 0.252 | 41.609 | Dictyota | Dark |
| Dark_3 | 5.982 | 0.241 | 0.018 | 24.820 | Sargassum | Dark |  
| Dark_4 | 40.569 | 0.215 | 0.087 | 188.649 | Padina | Dark |  
| Dark_5 | 8.783 | 0.068 | -0.144 | 129.343 | Jania | Dark |  
| Dark_6 | 8.071 | 0.201 | 0.077 | 40.057 | Red UNK | Dark |  
| Dark_7 | 17.600 | 0.145 | 0.238 | 121.678 | Ulva | Dark |  
| Dark_8 | 16.855 | 0.135 | -0.428 | 125.310 | Galxaura | Dark |

- **Fig. 1 - Theoretical quantile slopes**  

![Theoretical quantile]({{site.baseurl}}/images/Quantile_DvsL.png)

- **Fig. 2 - ETR curves of all specimens**  

![ETR curves]({{site.baseurl}}/images/ETR_curves.png)

- **Fig. 3 - Box plots of Light & Dark correlated species**  

![Box plots]({{site.baseurl}}/images/Sp_box_DvsL.png)

- **Fig. 4 - Differences in photophysiology of species**  

![Species difference]({{site.baseurl}}/images/Sp_Diff.png)

- **Fig. 5 - The ratio of species' photophysiology differences**  

![Species difference ratio]({{site.baseurl}}/images/Sp_Ratio.png)