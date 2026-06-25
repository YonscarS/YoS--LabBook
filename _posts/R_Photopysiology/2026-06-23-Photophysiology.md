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
    
    !["Light" algae plate]({{site.baseurl}}/_posts/R_Photophysiology/L_plate.JPG)  

    2.  9 algae samples taken from "dark" habitat  

    !["Dark" algae plate]({{site.baseurl}}/_posts/R_Photophysiology/D_plate.JPG)  

- Specimens were detached from their substrate, placed into labelled zip-lock bags containing habitat water, and transported to the laboratory for analysis.
- Species were identified to genus level using morphological characteristics
- Prior to dark fluorescence measurements, specimens were dark-adapted for 30 min to allow all PSII reaction centres to open  
- PAM fluorometry was used to assess algal photophysiology  
- Two datasets were collected for each group:  
    1. Light-adapted fluorescence measurements  

    !["Light" algae in PAM program]({{site.baseurl}}/_posts/R_Photophysiology/L_PAM.jpg)  
    
    2. Dark-adapted fluorescence measurements  
    
    !["Light" algae in PAM program]({{site.baseurl}}/_posts/R_Photophysiology/D_PAM.jpg)  

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
| Light_1 | 33.2531204083411 | 0.124138383694383 | -0.392076904420246 | 267.871382071536 | Jania | Light |  
| Light_2 | 6.48288440203671 | 0.113757726622265 | -0.0741306420140389 | 56.9885193254898 | Halopteris | Light |  
| Light_4 | 30.1255228905968 | 0.152982833687472 | -0.670135949726572 | 196.920936581291 | Sargassum | Light |
| Light_5 | 23.4097869866794 | 0.163451737165566 | 0.0542624463627908 | 143.221402186547 | Hypnea | Light |  
| Light_6 | 8.82654444134221 | 0.139380135071571 | 0.136145009320897 | 63.3271336464828 | Cudiom | Light |  
| Light_7 | 47.0819454462712 | 0.184118291883532 | -0.556760029066647 | 255.715741030522 | Padina | Light |  
| Light_8 | 13.8867534826263 | 0.142197933425134 | -0.0297035569271432 | 97.6579135022202 | Cistosera | Light |  
| Light_10 | 7.94846412774733 | 0.122375654074901 | -0.120735060877725 | 64.9513515399266 | Galaxaura | Light |  
| Light_11 | 31.1688074950612 | 0.139077573032331 | 0.0540374798749975 | 224.110953444777 | Dictyota | Light |  
| Light_12 | 16.8278798129839 | 0.122772542052393 | -0.135741906425159 | 137.0654995952 | Colpomenia | Light |  
| Light_13 | 17.7312387711855 | 0.0986143115546302 | -0.0853604232877464 | 179.803909713072 | Ulva | Light |  
| Dark_1 | 33.9598582034005 | 0.207569458343549 | -0.344548742966204 | 163.607201533442 | Colpomenia | Dark |  
| Dark_2 | 12.8130742275855 | 0.307942002541703 | 0.251554012389022 | 41.608725415268 | Dictyota | Dark |
| Dark_3 | 5.98163280318466 | 0.2409982994639 | 0.0175071210353956 | 24.820228260908 | Sargassum | Dark |  
| Dark_4 | 40.5690075621483 | 0.215049809647831 | 0.0866373449118526 | 188.649353508309 | Padina | Dark |  
| Dark_5 | 8.78277547839224 | 0.0679029168303748 | -0.144030563256971 | 129.343125278876 | Jania | Dark |  
| Dark_6 | 8.0714269487166 | 0.201499718313963 | 0.0774041065627906 | 40.0567654200899 | Red UNK | Dark |  
| Dark_7 | 17.5998253739184 | 0.14464227722501 | 0.23764429676204 | 121.678292900073 | Ulva | Dark |  
| Dark_8 | 16.8546953797643 | 0.134503884332498 | -0.4276662271526 | 125.31010136554 | Galxaura | Dark |

- **Fig. 1**
![Theoretical quantile]({{site.baseurl}}/_posts/R_Photophysiology/Quantile_DvsL.png)

- **Fig. 2**
![ETR curves]({{site.baseurl}}/_posts/R_Photophysiology/ETR_curves.png)

- **Fig. 3**
![Box plots]({{site.baseurl}}/_posts/R_Photophysiology/Sp_box_DvsL.png)

- **Fig. 4**
![Species difference]({{site.baseurl}}/_posts/R_Photophysiology/Sp_Diff.png)

- **Fig. 5**
![Species difference ratio]({{site.baseurl}}/_posts/R_Photophysiology/Sp_Ratio.png)