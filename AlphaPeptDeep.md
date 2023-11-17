 "A modular Python framework built on the PyTorch DL library that learns and predicts the properties of peptides ([https://github.com/MannLabs/alphapeptdeep](https://github.com/MannLabs/alphapeptdeep))"
 - Extensive use of transfer learning obviates the need for large data sets to refine models for particular experimental conditions
 - Predicting retention time, collisional cross sections and fragment intensities are at least on par with existing tools
 - Includes [[HLA]] peptide prediction model
 - ***Question***: what is the specific formatting for ```mod_sites``` and ```mods```
	 - Only example to run off of 
```
	sequence pep_name irt mods mod_sites nAA rt_pred rt_norm_pred irt_pred
	GAGSSEPVTGLDAK RT-pep b 0.00 Phospho@S 5 14 0.266746 0.266746 11.916059
```

