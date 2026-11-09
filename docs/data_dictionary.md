# Data Dictionary

## File inventory

The zip contains 38 files: 36 data files (listed in the paper's S1 Appendix)
and 2 documents (`appendix.docx`, `marked_manuscript.docx`).

## Hurst Files ('Hurst_[patientID].txt)

Shape: 
    
    - H12 and P11: (17000,2)
    - all other patients: (17000,32)
Locations of F3 hurst values:m\
    
    - H12 and P11, column 0 (1st column)
    - all other patients: column 2 (3rd column)
Locations of all channels (author clarification needed):
    
    - for now assumed to follow the order of the figures in the appendix, which is: Fp1, Fp2, F3, F4, C3, C4, P3, P4, O1, O2, F7, F8, T7, T8, P7, P8, Fz, Cz, Pz, Oz, FC1, FC2, CP1, CP2, FC5, FC6, CP5, CP6, TP9, TP10, POz. 
    - ECG is almost certainly row 31, as it's Hurst value is far outside the range of the previous 31 values 

## EEG files ('[PatientID].txt')

Shape:
    
    - (32,50000)
Locations of F3: 
    
    -c olumn 2 (0 indexed) aka the 3rd row of each original data file has the EEG data for F3.
Locations of all channels (author clarification needed): 
    
    - Rows 0–30 follow order of the figures in the appendix: Fp1, Fp2, F3, F4, C3, C4, P3, P4, O1, O2, F7, F8, T7, T8, P7, P8, Fz, Cz, Pz, Oz, FC1, FC2, CP1, CP2, FC5, FC6, CP5, CP6, TP9, TP10, POz. Row 31 is ECG.
        - this was spot checked by looking at figures where P11 (P6 in the figure) have almost no variation (have a flat line instead of a standard box in the box and whisker plots). These rows with minimal variation match the channels that have a flat P6 boxplot. 
    - Row 31 is ECG
        - Row 31 has much higher magnitude than any others

Unit of measurement: 
    
    - Most likely µV. Indicated 
    the box and whisker plot that matches the data on fig 1 would indicate that the unit of measurement is 0.1 µV, but this is likely a mistake 
