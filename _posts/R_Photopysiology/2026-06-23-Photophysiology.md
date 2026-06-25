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
        - Maximum electron transport rate (ETRmax) = Asymptotic maximum (Am) = max photosynthesis (Pmax)   
        - Saturation irradiance (Ik or Ek)  

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
- Prior to dark fluorescence measurements, specimens were adapted in a dark room for 30 min to allow all PSII reaction centres to open  
- PAM fluorometry was used to assess algal photophysiology  
- Two datasets were collected for each group:  
    1. Light-adapted fluorescence measurements  

    !["Light" algae in PAM program]({{site.baseurl}}/images/L_PAM.jpg)  
    
    2. Dark-adapted fluorescence measurements  

    !["Light" algae in PAM program]({{site.baseurl}}/images/D_PAM.jpg)  

> See files "dark.csv" and "light.csv"

- The raw data was analyzed using R studio version 2026.04.0-526.
- R packages used for analyzing proccess:
    1. "lubridate" - format date data
    2. "hms" - format time data
    3. "dplyr" - data manipulation
    4. "tidyr" - data manipulation
    5. "purrr" - data manipulation
    6. "broom" - data manipulation
    7. "ggplot2" - graphics
    8. "patchwork" - graphics
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

- **Fig. 1 - ETR curves of light algae specimens**  

![Light ETR]({{site.baseurl}}/images/L_ETR.png)
 Electrom transport rate (ETR; calculated by PAM program) in relation to photosynthetically Active Radiation (PAR; µmol photons m⁻² s⁻¹) for twelve algae genus. Curves show how photosynthetic electron transport responds to increasing light intensity.  


- **Fig. 2 - ETR curves of dark algae specimens**  

![ETR curves]({{site.baseurl}}/images/ETR_curves.png)  
 Electrom transport rate (ETR; calculated by PAM program) in relation to photosynthetically Active Radiation (PAR; µmol photons m⁻² s⁻¹) for eight algae genus. Curves show how photosynthetic electron transport responds to increasing light intensity.  

- **Fig. 3 - ETR curves of light & dark specimens**  

![ETR curves]({{site.baseurl}}/images/ETR_curves.png)  
 Electrom transport rate (ETR; calculated by PAM program) in relation to photosynthetically Active Radiation (PAR; µmol photons m⁻² s⁻¹) for twelve light algae genus in the left and eight algae genus in the right. Curves show how photosynthetic electron transport responds to increasing light intensity.  

- **Fig. 4 - Box plots of Light & Dark correlated species**  

![Box plots]({{site.baseurl}}/images/Sp_box_DvsL.png)  
Comparison of four photosynthetic parameters between Light and Dark treatments for six algae genus that were collected from both sites. Top-left; Asymptotic maximum (AM), top-right; Apparent quantum yield (AQY), bottom-left; Saturation Irradiance (Ik), bottom-right; Dark Respiration (Rd).  
Lower box line represents the first quartile (Q₁ - The lower 25th percentile). Bold line in the box represents the Median (The 50th percentile).Upper box line represents the third quartile (Q₃ - The upper 75th percentile).  

- **Fig. 5 - Differences in photophysiology of species**  

![Species difference]({{site.baseurl}}/images/Sp_Diff.png)  
Differance of four photosynthetic parameters between Light and Dark treatments' values ("Light" minus "Dark") for six algae genus that were collected from both sites. Top-left; Asymptotic maximum (AM), top-right; Apparent quantum yield (AQY), bottom-left; Saturation Irradiance (Ik), bottom-right; Dark Respiration (Rd).  

#### Interpretation  
###### Figures 1 - 3    
All species show a similar response and a typical shape of photosynthesis–irradiance (PI) curve:
- ETR increases rapidly at low irradiance.
- The rate of increase slows at intermediate irradiance.
- A maximum ETR is reached.
- Some species plateau while others decline slightly at high irradiance.

"Light" algae generally shows higher maximum ETR values, higher saturation irradiance, and greater photosynthetic capacity compared to "Dark" algae that shows lower ETR values, earlier saturation, and more sensitivity to increasing irradiance.  

The species differ substantially in photosynthetic capacity. Out of all species measured in this experiment, *Padina* consistently exhibits the highest ETR and therefore the greatest capacity for electron transport and photosynthesis capability.

###### Figure 4  
**Am** represents the maximum electron transport rate (ETRmax), which means that higher values indicate greater photosynthetic capacity and higher productivity.  
The higher Am values of the Light-acclimated specimens indicates for the possession of greater photosynthetic capacity.  

**AQY** is the initial slope of the light-response curve and it represents the efficiency of light utilisation under low irradiance.  
The higher AQY values of the Dark-acclimated algae indicates for more efficiency at capturing and using low levels of light, probably due to their adaptation to shaded conditions.  

**Ik** is the irradiance level at which photosynthesis becomes light-saturated, which means that higher Ik indicates for better adaptation to strong light, and for the ability of plants to continue increasing photosynthesis at higher irradiance.  
From the plots it seems that the Light-acclimated algae require higher irradiance before saturation occurs and therefore their tolerance for strong light is better then the Dark-acclimated algae.  

**Rd** estimates the respiration losses. The greater negative the values points on more carbon consumption through respiration.
It is observed that the Light-acclimated algae tend to have more negative Rd values, and therefore higher metabolic activity.

###### Figures 5  
Difference bar plot for values demonstrating the photophysiology addaption of each algae genus.  
Thee different plots for each parameter shows the difference in values, thus helps us with assumptions of how each alge is addapting itself to the different habitat.  
*Colpomenia* is demonstrating different results from the rest suggesting an option of swap between the habitat specimens.  

###### conclousion
PAM fluorometry revealed the variation in photophysiological performance. Overall, species differed considerably in their responses, suggesting habitat-specific physiological adaptations. Light-acclimated algae exhibited higher maximum electron transport rates and saturation irradiances, whereas dark-acclimated algae displayed higher apparent quantum yields.  
These results suggest that habitat light conditions strongly influence algal photosynthetic acclimation, and that different genus might preforme their addaption in different photophysiological preformences.

#### Follow-Up Experiment: Comparison of Photophysiological Performance Among Macroalgal Divisions  
The present study demonstrated significant differences in photophysiological performance among macroalgal genera. A new experiment would therefore investigate photophysiological performance at a higher phylogenetic level by comparing few representatives of the three major macroalgal divisions:  
- Chlorophyta (green algae)  
- Phaeophyceae/Ochrophyta (brown algae)  
- Rhodophyta (red algae)  

**Hypothesis** - Photophysiological parameters differ among macroalgal divisions because each lineage has evolved distinct photosynthetic pigments, light-harvesting mechanisms, and ecological adaptations.  

At least three species from each division sould be collected from similar habitats to minimise environmental variation. For example:

| Division	| Example Species |
|-----------|-----------------|
| Chlorophyta |	Ulva, Codium, Caulerpa |
| Phaeophyceae | Padina, Dictyota, Sargassum |
| Rhodophyta | Jania, Galaxaura, Hypnea |