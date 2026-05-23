# <center>Phylogenetic Tree Construction Using MEGA</center>

1. **Install MEGA**  
If you don’t have MEGA installed, download and install it from the [official site](https://www.megasoftware.net/).

2. **Prepare sequence data**  
Collect DNA sequences for the target species and closely related species.

3. **Open MEGA**  
Open MEGA software.
From the main menu, choose: Align → Edit/Build Alignment. Create a new alignment. Choose DNA. 

4. **Import sequences**  
In the Alignment Explorer window: Edit → Insert Sequence from File.  
Make sure: 
    - Each sequence has a clear species/sample name.
    - All sequences are in the same orientation.
    - No sequence is accidentally duplicated.
    - No sequence contains large unknown regions marked as NNNNN.

5. **Perform multiple sequence alignment**  
In the Alignment Explorer window, choose: Alignment → Align by ClustalW

6. **Save the alignment**  
Save the alignment file: Data → Save Session

7. **Open the alignment for tree construction**
    - Return to the main MEGA window.
    - Choose: File → Open a File/Session
    - Analyse this data? Yes

8. **Choose phylogenetic tree method**  
From the main MEGA menu, choose:  
Phylogeny>Construct/Test Neighbour-Joining Tree 
    - Test of phylogeny: Bootstrap method
    - No. of bootstrap replications: 1000
    - Substitution model: Kimura 2-parameter
    - Rates among sites: Uniform rates
    - Gaps/missing data treatment: Pairwise deletion or Partial deletion  
    ![Tree method.jpg]({{site.baseurl}}/images/Tree%20method.JPG)

9. **Run the tree analysis:** Compute

10. **Interpret the tree**  
Examine whether the target species clusters with expected related species.
    - Bootstrap values above 70% provide reasonable support for a clade.
    - Bootstrap values below 50% should be interpreted cautiously.

11. **Edit and label the tree**  
In the Tree Explorer window, you can adjust the display. Useful options:  
    - View → Show/Hide Bootstrap Values
    - View → Show/Hide Branch Lengths
    - Subtree → Compress/Expand
    - Image → Export Current Tree Image

12. **Save and export the tree**  
Save the tree session: File → Save Session

