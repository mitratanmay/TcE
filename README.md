1. Open VMD TkConsole and provide the following command (after adjusting the path accordingly): source "C:/Users/tmitr/Downloads/1_TcE_SAXS_updated_files_R/TcE_SAXS/Format-A_complex/TCL_codes/anti-HER2_aligned/alignment_FormatA_Complex.tcl"
It saves the aligned PDB files in the pdb directory itself, where the original multistate pdb files are stored (e.g., in this case "C:/Users/tmitr/Downloads/1_TcE_SAXS_updated_files_R/TcE_SAXS/Format-A_complex/10best_multistate_pdbs")
2. source "C:/Users/tmitr/Downloads/1_TcE_SAXS_updated_files_R/TcE_SAXS/Format-A_complex/effective_weights_unique_pdbs_ALIGNED.tcl"
It saves a csv file having the effective weights for unique PDB files in a desired folder (in this case, "C:/Users/tmitr/Downloads/1_TcE_SAXS_updated_files_R/TcE_SAXS/Format-A_complex/unique_pdbs_effective_weights.csv") based on the ensemble weights of the best 10 multistate models as given in 10best_MS_weights.txt file.
3. Figure for distances: Base path: 'C:/Users/tmitr/Downloads/1_TcE_SAXS_updated_files_R/TcE_SAXS/Format-%s_complex/TCL_Codes/anti-HER2_aligned/HER2_aHER2_axis/anchordistance_each_weight.csv'
To generate anchordistance_each_weight.csv : For Format A (and do similar for other formats according to the path)source "C:/Users/tmitr/Downloads/1_TcE_SAXS_updated_files_R/TcE_SAXS/Format-A_complex/TCL_Codes/anti-HER2_aligned/HER2_aHER2_axis/anchor_distance.tcl"
To create figure: matlab file - compare_formats_complex_distance.m (in C:/Users/tmitr/Downloads/1_TcE_SAXS_updated_files_R/TcE_SAXS)
4. Figure for RG: Base path for the file containing information on RG of the complexes:  'C:/Users/tmitr/Downloads/1_TcE_SAXS_updated_files_R/TcE_SAXS/Format-%s_complex/TCL_Codes/anti-HER2_aligned/HER2_aHER2_axis/angles_COMdistances_flexibility_rg_weight.csv'
To generate angles_COMdistances_flexibility_rg_weight.csv in specific folders (such as folder for complex A): source "C:/Users/tmitr/Downloads/1_TcE_SAXS_updated_files_R/TcE_SAXS/Format-A_complex/TCL_Codes/anti-HER2_aligned/HER2_aHER2_axis/Normalized_Angles_DistancesfromCOM_Flexibility_RG.tcl"
For generating figure in matlab - compare_formats_complex_RG.m(in C:/Users/tmitr/Downloads/1_TcE_SAXS_updated_files_R/TcE_SAXS)
5. Figure for CoM Flexibility:
For generating figure in matlab - compare_formats_complex_distanceflex.m(in C:/Users/tmitr/Downloads/1_TcE_SAXS_updated_files_R/TcE_SAXS)
It is also based on the following file types - angles_COMdistances_flexibility_rg_weight.csv
6. Figure for Rotational Flexibility:
For generating figure in matlab - compare_formats_complex_AngFlex.m(in C:/Users/tmitr/Downloads/1_TcE_SAXS_updated_files_R/TcE_SAXS)It is also based on the following file types - angles_COMdistances_flexibility_rg_weight.csv

7. Figure for Shannon Entropy:
Base path = 'C:/Users/tmitr/Downloads/1_TcE_SAXS_updated_files_R/TcE_SAXS/Format-%s_complex/TCL_Codes/anti-HER2_aligned/HER2_aHER2_axis/domain_analysis_results_rms_rmsd_new.csv';

Plot (matlab) - entropy_paper_plot_complex.m (in C:/Users/tmitr/Downloads/1_TcE_SAXS_updated_files_R/TcE_SAXS)
To generate Format specific domain_analysis_results_rms_rmsd_new.csv (in C:\Users\tmitr\Downloads\1_TcE_SAXS_updated_files_R\TcE_SAXS\Format-A_complex\TCL_codes\anti-HER2_aligned\HER2_aHER2_axis) :
Run Normalized_Metrics_All_New.m in C:\Users\tmitr\Downloads\1_TcE_SAXS_updated_files_R\TcE_SAXS\Format-A_complex\TCL_codes\anti-HER2_aligned\HER2_aHER2_axis (this utilizes angles_COMdistances_flexibility_rg_weight.csv and hence, this has to be generated earlier)
For shannon entropy, we are using Entropy_Flex, Flex is defined as the product of angles and distanceflex

8. Tilt angles - radial_hist_one_hemi_weight_new3.m (in C:\Users\tmitr\Downloads\1_TcE_SAXS_updated_files_R\TcE_SAXS\Format-A_complex\TCL_codes\anti-HER2_aligned\HER2_aHER2_axis)
This uses tiltangles_localtransformedHER2_each_weight.csv(the file is in C:\Users\tmitr\Downloads\1_TcE_SAXS_updated_files_R\TcE_SAXS\Format-A_complex\TCL_codes\anti-HER2_aligned\HER2_aHER2_axis)
To generate tiltangles_localtransformedHER2_each_weight.csv : source "C:/Users/tmitr/Downloads/1_TcE_SAXS_updated_files_R/TcE_SAXS/Format-A_complex/TCL_Codes/anti-HER2_aligned/HER2_aHER2_axis/Normalized_Metrics.tcl"



**Please adjust accordingly for the formats only (non complex) after adjusting the files based on suitable domain information and path.
Use 1_TcE_SAXS_updated_files for TcE formats only and 1_TcE_SAXS_updated_files_R for TcE complexes.**











