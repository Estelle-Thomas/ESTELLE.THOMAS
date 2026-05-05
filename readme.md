# Python and R project template for Master's internship in human movement sciences

**The heart rate variability (HRV) in Borderline Personality Disorder (BPD) **

# **1. Scientific question**

## **1.1. Introduction**
Le trouble de la personnalité borderline (TPB) est un trouble psychiatrique sévère, chronique, invalidant, caractérisé par une instabilité de la notion de soi, émotionnelle, des relations interpersonnelles, ainsi qu'une impulsivité marquée (Ducasse, 2020)
La dysrégulation du système nerveux autonome (SNA), marquée par une variabilité réduite de la fréquence cardiaque (HRV) au repos, témoin d’un déséquilibre entre les branches sympathique et parasympathique, est associée à l’instabilité émotionnelle et l’impulsivité chez les personnes avec TPB. Elle est également associée à une charge allostatique accrue, reflet d’un vieillissement biologique accéléré, contribuant à la surmortalité cardiovasculair (Bozzattello, 2025)

Heart rate variability (HRV) is a measure of the fluctuation in time interval between consecutive heartbeats (Figure 1). HRV has been thought to provide insight into the tightly regulated signaling pathways of the autonomic nervous system and may serve as a surrogate measure of balance between the brain and the cardiovascular system. Decreased heart rate variability has been associated with autonomic dysfunction in a variety of conditions, likely as a result of an imbalance between parasympathetic and sympathetic input on heart rate and rhythm.

## **1.2. Aim**
The objective of this project is to check that the HRV is reduced in BPD patients compared to healthy controls.

## **1.3. Method**
Each participant will be equipped with a heart rate monitor (Polar H10) for 5 minutes, in rest. With the application *Elite HRV* the R-R intervall is recorded and the Root Mean Square of Successive Differences (RMSSD) will be calculated, with Python. 
The participant should also fill the Borderline Symptom List (BSL-23) questionnaire, which is a self-report measure of the severity of borderline symptoms.

## **1.4. Participants**   
- BDP patients: XX   
- Healthy controls: XX   

## **1.5. Outcome measure**
`HRV = RMSSD` (Root Mean Square of Successive Differences)    
`BSL-23 score = sum of the 23 items`    

<img src="Figure/RR.jpeg" width="50%">

# **2. Python project**     

## **2.1. Aim**    
The objective of Python project is to transform the R-R intervall in text form to RMSSD, for each participants. 
Python is use to obtain values workable for statistical analysis.

## **2.2. Method**   
Using Neurokit2, I will calculate the RMSSD value for each participant, based on the R-R intervall recorded with the Polar H10.


### **2.3. Data organisation**    
The folder `data` contains all file for each participant. 
- `PXX_RR.txt` contains the R-R intervall in text form for participant XX.

### **2.4.Folder organisation**   
`data` folder contains all the data files for each participant.

   
### **2.5. Results**    
Finally, in this Python project, I will obtain a dataframe with the RMSSD value for each participant. 
This table will be used for statistical analysis in R.




# **3. R project**

## **3.1. Aim**
The objective of R project is to compare the RMSSD values between BPD patients and healthy controls, and to check if there is a correlation between RMSSD and BSL-23 score.

## **3.2. Data organisation**
File : `data.csv`
Columns :
  - `ID` of the participant.   
  - `Groupe` (BPD or CONTROL).   
  - `QX` response to question X (from 1 to 23).   
  - `Score_BSL` (sum of the 23 items).   
  - `Score_moyen` (mean of the 23 items).   
  - `Sévérité` (severity of the symptoms, based on the score).   
  - `%`      
    
File : `HRV_results.csv`.     
Columns :
  - `ID` of the participant.   
  - `Groupe` (BPD or CONTROL).      
  - `RMSSD` value for each participant.
  
## **3.3. Results**    
Finally, in this R project, I will obtain a table with the results of the statistical analysis (e.g., p-value, effect size, etc.) and a figure showing the comparison between the two groups.   


## **3.4. Conclusion**    


# **4. Reference**   
1. Ramesh, A., Nayak, T., Beestrum, M., Quer, G., & Pandit, J. A. (2023). Heart rate variability in psychiatric disorders: A systematic review. Neuropsychiatric disease and treatment, 2217-2239.
2. DUCASSE 2020
3. Bozzattello 2025




The `template.ipynb` notebook contains a minimal template for data analysis with python. It includes the following sections:
- **Header:**
  - The first cell will add a header to the notebook with the project title, author, date. 
  - You should edit this cell to add your information.
- **Data Analysis Cells:**
  - The cells you will use for data analysis (e.g., loading data, preprocessing, modeling, etc.) go here.
- **Export Cell:**
  - The last cell will save the notebook as a HTML file next to the notebook file and open it in your web browser. 
  - The HTML will include all the graphics, and will not show the cell numbers. 
  - Cells tagged with `hide` will not be shown in the HTML file. 
    - You can add the `hide` tag to any cell you do not want to appear in the HTML file (e.g., in VSCode, click on  `...` in the icon box in the top left of the cell)

## Requirements
- [A minimal Python environment for reproducible research in human movement sciences](https://github.com/DenisMot/Python-minimal-install) is my preferred solution.
- Any IDE supporting python and jupyter notebooks is an alternative solution. 