# <center>Primer design for algal species</center> 

1. Choose the target organism or species you want to identify.  

2. Choose a conserved gene that is commonly used for species identification.
    - Prokaryota: 16SrRNA, etc.
    - Eukaryota: 18S rRNA, etc.
    - Chloroplast genes: rbcL, tufA, etc.
    - Mitochondrial genes: COX, etc.  

3. Open [NCBI National Center for Biotechnology Information (nih.gov)](https://www.ncbi.nlm.nih.gov/), and select Nucleotide.

4. Search for your organism gene and select the appropriate search result.

5. View and copy the nucleotide sequence:
    - Click on the FASTA option to get the sequence.

6. Repeat this process to obtain sequences for at least three (or more) species closely related to the species you are interested in identifying.

7. Multiple Sequence Alignment Using ClustalW (either through website: Multiple Sequence Alignment - CLUSTALW ) or MEGA software. 
 
8. Visit the ClustalW website: ClustalW.
- Prepare for alignment:
    - Copy the sequences, including their titles, into the “Enter your sequences” window.
    - Set the sequence type to DNA.
    - Execute the alignment by clicking “Execute Multiple Alignment”. (Shown above)

9. Save the alignment result to a text editor (MS word or Notepad) for further analysis.

10. Selection of Regions for Primer Design
    - Review the multiple sequence alignment. Identify two conserved regions that flank a variable region. The conserved regions will be used as primer-binding sites, while the variable region between them should contain SNPs or indels useful for distinguishing the target species from closely related species.
    - If no suitable conserved flanking regions or variable internal regions are present, choose another barcode gene or add more closely related species to the alignment.

11. Navigate to the Primer3 website: Primer3.
    - Input the chosen sequence: Primer3 should receive a single clean DNA sequence, not a ClustalW alignment with gaps, stars, spaces, or multiple species.
    - Design the primers: Click “Pick Primers” to generate possible primer pairs.
- Make sure:
    - Primer length: 18-25 nucleotides
    - Melting temperature (Tm): 50-60°C
    - GC content: 40-60%
    - Avoid secondary structures (hairpins, dimers)
    - Ensure primers are specific to the target species
    
12. Verification of Primer Specificity with Primer-BLAST
    - Open NCBI Primer-BLAST and enter the forward and reverse primer sequences designed by Primer3.  

    ![Primer Ver1]({{site.baseurl}}/images/Primer%20Ver1.JPG)  

    - Select an appropriate database, such as the nucleotide collection or RefSeq representative genomes, depending on the organism.  

    ![Primer Ver2]({{site.baseurl}}/images/Primer%20Ver2.JPG)  
 
13. First, check that the primers amplify the expected region in the target species. Then repeat the search against closely related species, the same genus, or a broader taxonomic group to detect possible non-target amplification.  
If the primers amplify several closely related species, they may still be acceptable for species identification if the amplified region contains enough SNPs or indels and the product will be sequenced.
 
> The biggest conceptual point is this: for species identification, conserved primers are often used to amplify a variable barcode region; the species is then identified from the amplicon sequence, not necessarily from PCR amplification alone.












