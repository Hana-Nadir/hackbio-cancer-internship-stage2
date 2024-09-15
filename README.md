# **Protein structure modeling, visualaization, and analysis using SWISS-MODEL, AlphaFold, and PyMOL**
## **Authors (@slack): Hanna, BigWils, samar-samir, sarasamer22, DerleenM**

## **Introduction :**
p53, a crucial tumor suppressor protein, plays a pivotal role in maintaining genomic stability and preventing cancer. Often referred to as the "guardian of the genome," p53 regulates cell cycle progression, DNA repair, and apoptosis. Its inactivation or loss can lead to uncontrolled cell growth, genomic instability, and tumor formation. Mutations in the p53 gene are frequently found in human cancers, underscoring its importance in tumor suppression.Mutations in the p53 gene are among the most common genetic alterations found in over 50% of human cancers. This is precisely why we chose to focus our analysis on it.

### **Protein structure feature analysis :**
**P53 Protein main domains:**   Transcription activation (1-44) ,p53 proline-rich domain ,it’s a sequence that lies between amino acids 61 and 94 (out of 393\) .sequence-specific DNA binding domain (center region of the protein) (amino acid residues 100–290 out of 393\) .    homo-oligomerization (residues 319–360 ).  Regulatory domain or C-terminal domain (364-393 residues)  
**P53 cancer-related mutations :**  
Mutations in p53 often occur within the DNA binding domain, disrupting its ability to bind to DNA and regulate target genes. This can lead to loss of p53 function and contribute to cancer development.

### **The three conformation structures :**
we selected three conformations from the Protein Data Bank (PDB):

* **8DC4:** Represents the antagonist conformation, with a single engineered mutation at position 131\.  
* **2OCJ:** Represents the apo conformation, lacking any bound ligands.  
* **6GGB:** Represents the agonist conformation, with EXQ as the main ligand.
  
## **The modeling workflow :**

### **1- Homology modeling by SWISS MODEL :**

SWISS-MODEL successfully predicted the 3D structure of p53. The model is of high quality, with excellent sequence identity and coverage. However, some regions, particularly after residue 200, might require further refinement due to lower structural similarity confidence.

![image](https://github.com/user-attachments/assets/3dc10a93-e86b-48ae-ad56-f0fbce4e76c9)

_**Figure 1: illustrate the GMQE , QMEAN ,identity, coverage parameters of the predicted protein structure.**_


![image](https://github.com/user-attachments/assets/50b9a546-ea85-4920-9816-597c078872c1)

_**Figure 2: visualization of the homology modeling predicted protein structure by PyMOL.**_


### **2- AlphaFold modeling :** 
The predictions from AlphaFold provide insights into the structural properties of p53, such as sequence coverage, predicted IDDT scores, and contact maps

**a- Sequence Coverage :**

![image](https://github.com/user-attachments/assets/60bf8636-a13c-4f09-8f84-e56168494d40)

_**Figure 3: The  sequep53 sequence shows good coverage (mostly green to blue) in the central regions, with highernce identity in the middle (~100 to 300 positions).**_


**b- Predicted IDDT per Position :**

![image](https://github.com/user-attachments/assets/a4e9d0bb-9940-4f24-9320-7be03c7be0a7)

_**Figure 4: The predicted IDDT (Distance Difference Test) per position indicates the confidence of AlphaFold’s predictions for each residue. Higher values (closer to 100\) represent more confident predictions, and lower values indicate less confident predictions.**_


**c- Contact Map for Ranks 1 to 5 :**

![image](https://github.com/user-attachments/assets/11b1a0ac-d156-46e9-b9ce-a37f7e5c46de)

_**Figure5: The contact maps display predicted residue-residue contacts in the protein structure for each rank (1 to 5).Red areas represent low proximity (no close contact), while blue indicates regions where residues are likely in close spatial proximity.**_


![image](https://github.com/user-attachments/assets/1124e26f-d0e8-4f56-8a29-97c74bc563dc)

_**Figure 6 : visualization of the alphafold predicted protein by PyMOL.**_


## **Comparison between the predicted proteins and the ones in the databases :**

According to our finding in Table(1) , it appears that SWISS-MODEL is most likely to generate an antagonist conformation ( RMSD \= 2.059) , and Alphafold is likely to generate an agonist conformation (RMSD \= 0.453). Moreover, the predicted alphafold protein is found to show more similarity to the original P53 structure in the databases( RMSD \= 14.155).


TABLE (1): 
|  **Database protein  ⬇️** | RMSD of ALphaFold GENERATED PEOTEIN aligns  | RMSD of SWISS-MODEL GENERATED PROTEIN aligns  |
| ----- | ----- | :---- |
| | | |
| **P53 Original structure**  | **14.155** | **19.658** |
| **8DC4 structure** (Antagonist)| **0.621** | **2.059** | 
| **6GGB structure**  (Agonist) | **0.453** | **2.136** | 
|  **2OCJ structure** (Apo) | **0.484** | **2.120** | 



![image](https://github.com/user-attachments/assets/2c562206-be8d-4fa6-b4b4-3a2447d346cf)

_**Figure 7 : the alignment between the SWISS-MODEL predicted protein ( green)  and the original p53 structure (purple).**_


![image](https://github.com/user-attachments/assets/1e4c822f-79a6-4ed6-996c-c8548bc5a464)

_**Figure 8 : the alignment between the SWISS-MODEL predicted protein (green) and 8DC4 (purple).**_


![image](https://github.com/user-attachments/assets/b1678193-460c-43e2-8b57-905fae76cf00)

_**Figure 9: the alignment between the SWISS-MODEL predicted protein (green) and 6GGB (purple).**_


![image](https://github.com/user-attachments/assets/d8c53904-7a0e-4825-8d37-f83b0ea6d8d6)

_**Figure 10: the alignment between the SWISS-MODEL predicted protein (green) and 2OCJ (purple).**_


 ![image](https://github.com/user-attachments/assets/f32b6c3a-dc29-4d7f-8d67-ed762983ed09)

_**Figure 11 : the alignment between the alphafold predicted protein (green) and the original P53 structure (purpel).**_


![image](https://github.com/user-attachments/assets/5133910a-f553-40ba-a7a6-ac5c1076797f)

_**Figure 12: The alignment between the alphafold predicted protein (green) and 8DC4 (purple).**_


![image](https://github.com/user-attachments/assets/e3722906-c259-4302-b7bc-f11453c89d3b)

_**Figure 13: alignment between the alphafold predicted protein (green) and 6GGB purple.**_


![image](https://github.com/user-attachments/assets/52968078-4931-4bd3-8f50-9afda32168a5)

_**Figure 14: the alignment between the alphafold predicted protein (green) and 2OCJ purple.**_

 

## **Conclultion :**

SWISS-MODEL and AlphaFold were used  to generate 3D models, further aligned with different conformational states of p53 in addition to its original structure using PyMOL . Overall, AlphaFold tends to offer superior accuracy and coverage compared to SWISS-MODEL, However, both tools are valuable depending on the context and available data.

## **References :**

1. Aubrey, B., Kelly, G., Janic, A. et al. How does p53 induce apoptosis and how does this relate to p53-mediated tumour suppression?. Cell Death Differ 25, 104–113 (2018). https://doi.org/10.1038/cdd.2017.169.  
2. Bauer, M. R., Jones, R. N., Tareque, R. K., Springett, B., Dingler, F. A., Verduci, L., … Spencer, J. (2019). A Structure-Guided Molecular Chaperone Approach for Restoring the Transcriptional Activity of the p53 Cancer Mutant Y220C. *Future Medicinal Chemistry*, *11*(19), 2491–2504. [https://doi.org/10.4155/fmc-2019-0181](https://doi.org/10.4155/fmc-2019-0181)  
3. Chen, X., Zhang, T., Su, W. et al. Mutant p53 in cancer: from molecular mechanism to therapeutic modulation. Cell Death Dis 13, 974 (2022). https://doi.org/10.1038/s41419-022-05408-1.  
4. C J Thut, J L Chen, R Klemin, R Tjian *Science* **267**, 100–104 (1995).  
5. el-Deiry WS, Kern SE, Pietenpol JA, Kinzler KW, Vogelstein B. Definition of a consensus binding site for p53. *Nat. Genet* 1992;1:45-49. doi: 10.1038/ng0492-45. PMID:1301998  
6. Guiley, K. Z., & Shokat, K. M. (2023). A small molecule reacts with the p53 somatic mutant Y220C to rescue wild-type thermal stability. Cancer Discovery, 13(1), 56-69. [https://doi.org/10.1158/2159-8290.CD-22-0381](https://doi.org/10.1158/2159-8290.CD-22-0381)  
7. H Lu, A J Levine *Proc Natl Acad Sci USA* **92**, 5154–5158 (1995).  
8.  Hollstein et al. 1994  
9. Janic, A., Abad, E. & Amelio, I. Decoding p53 tumor suppression: a crosstalk between genomic stability and epigenetic control?. Cell Death Differ (2024). https://doi.org/10.1038/s41418-024-01259-9.  
10. J Bargonetti, J J Manfredi, X Chen, D R Marshak, C Prives *Genes Dev* **7**, 2565–2574 (1994).  
11. Jessica Beck, Casmir Turnquist, Izumi Horikawa, Curtis Harris, Targeting cellular senescence in cancer and aging: roles of p53 and its isoforms, Carcinogenesis, Volume 41, Issue 8, August 2020, Pages 1017–1029, https://doi.org/10.1093/carcin/bgaa071.  
12. Jumper, A., et al. (2021). High-accuracy protein structure prediction with AlphaFold. Nature, 596(7873), 583-589.  
13.  M Clore, J Ernst, R Clubb, J G Omichinski, W M P Kennedy, K Sakaguchi, E Appella, A M Gronenborn *Struct Biol* **2**, 321–332 (1994)  
14. National Center for Biotechnology Information (US). Genes and Disease \[Internet\]. Bethesda (MD): National Center for Biotechnology Information (US); 1998-. The p53 tumor suppressor protein. Available from: https://www.ncbi.nlm.nih.gov/books/NBK22268/  
15. Rodriguez-Pastrana, I., Birli, E. & Coutts, A.S. p53-dependent DNA repair during the DNA damage response requires actin nucleation by JMY. Cell Death Differ 30, 1636–1647 (2023). https://doi.org/10.1038/s41418-023-01170-9  
16.   Schrödinger, LLC. (2023). PyMOL. Retrieved from [https://www.pymol.org/](https://www.pymol.org/)  
17. Waterhouse A, Bertoni M, Bienert S, Studer G, Tauriello G, Gumienny R, Heer FT, de Beer TAP, Rempfer C, Bordoli L, Lepore R, Schwede T SWISS-MODEL: homology modelling of protein structures and complexes.Nucleic Acids Res 46, W296-W303. (2018) 29788355 10.1093/nar/gky427  
18. Y Cho, S Gorina, P D Jeffrey, N P Pavletich *Science* **265**, 346–355 (1994).  
19. Y.  Wang, A.  Rosengarth and H.  Luecke- Structure of the human p53 core domain in the absence of DNA \- Acta Crystallographica Section D 2007;63(3):276-281 \- [https://doi.org/10.1107/S0907444906048499](https://doi.org/10.1107/S0907444906048499)



 







