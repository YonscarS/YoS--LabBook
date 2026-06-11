## Heat Shock effect on Lionfish Using targeted genes expression

In the last few decades, the highly invasive lionfish *Pterois miles* has established its population in the eastern Mediterranean. To understand better their capability to withstand the hot summer and cold winter in the Levant basin a test of gene expression is possible to understand the fish's ability to adjust with seasonal thermal differences.

#### Experiment

- Lionfish will be collected in summer time (July-August) and winter time (January-February), and as control also spring time (April-May).
- DNA will be extracted from different tissues from each season specimen.
- RT-qPCR will be conducted to quantify the expression of regulatory genes.
- Targeted genes expression will be calculated compared to reference genes.
- Quantification calculation.

#### Genes

**Housekeeping (HK) Genes:**  

- Elongation factor 1 alpha (EF-1α) - delivering aminoacyl-tRNAs to the ribosome during protein synthesis.
- Actin - muscle contraction, cell structure, and motility.

Stable and highly conserved genes for the normalization analysis in order to identify expression pattern of genes in teleost fishes. According to the [literature](https://doi.org/10.1016/j.fsi.2020.01.018) those tow genes are the most stable for using as reference genes out of the traditional HK genes.  
Becaus some [HK genes](https://doi.org/10.1016/j.fsi.2012.06.027) in fish may slightly change their expression, a second one is used.

**Expressed Genes:**

- Cytochrome c oxidase (cox) - the final step of the electron transport chain.
- Lactate Dehydrogenase (ldh-b) - shift lactate to pyruvate.

Two mitochondrial genes that are critical in energy production, homeostasis, and metabolic adaptation to environmental stress.  
Both genes induce their activity in colder water temperatures in order to enhance mitochondrial activity and energy production in the cell. Therefore, the hypothesis is to see higher expression from specimens collected during the winter than those collected during summer.  

#### Relative quantification

From qPCR results we need to extract the cycle Threshold (Ct) of each gene.
 
 1. Subtracting reference gene's Ct from the target gene's Ct.  
 > Δ𝐶𝑡=𝐶𝑡(target)−𝐶𝑡(reference)  
 2. Subtracting target gene's control Ct from the treatment Ct.  
 > ΔΔ𝐶𝑡=Δ𝐶𝑡(experimental)-Δ𝐶𝑡(control)  
 3. Powering two by negative delta delta Ct.
 > Fold Change = 2^( −ΔΔCt)  
 4. Bar plot of the calculated fold change will give a visual understanding of up-regulated (>~1.5) and down-regulated (<~0.5) genes.

 **Example**  
1. ![Initial Ct results]({{site.baseurl}}/images/Ct1.JPG)  
2. ![Calculated delta Ct]({{site.baseurl}}/images/Ct2.JPG)  
3. ![Calculated delta delta Ct]({{site.baseurl}}/images/Ct3.JPG)  
4. ![Calculated Fold change]({{site.baseurl}}/images/Ct4.JPG)  
5. ![Fold change graph]({{site.baseurl}}/images/Ct5.JPG)  

After calculation it may be seen that under treatment the genes "ascs", "foxS", and "NGN" were up-regulated, while "opt" was down-regulated compared to HK gene "Tubulin". 