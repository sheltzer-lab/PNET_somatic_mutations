# Somatic mutational profiling identifies aggressive and indolent disease phenotypes in well-differentiated pancreatic neuroendocrine tumors

## Data Availability

Below is a breakdown of the data that this project relies upon, specifically what it represents and whether it is publicly available.

+ `450-panel.txt`: The gene panel used by PanOrigiMed -- 450 genes, see Table S1 of https://doi.org/10.1634/theoncologist.2019-0236
+ `gene_panels/`: The gene panels used across cBioPortal, available through https://github.com/cBioPortal/datahub
+ `regional LN.csv`: Supplemental data from MSK-MET, https://doi.org/10.1016/j.cell.2022.01.003
+ `Updated PNET case list.csv`: Manually curated data regarding PNET cases gathered from individual reports

All other data is available via download from cBioPortal using the following study IDs:
+ PANET ARCNET 2017: `panet_arcnet_2017`
+ PANET JHU 2011: `panet_jhu_2011`
+ MSK-IMPACT: `msk_impact_2017`
+ MSK-MET: `ms_met_2021`
+ PANET MSK ERC 2023: `panet_msk_erc_2023`
+ PANET Shanghai: `panet_shanghai_2013`
+ PCAWG: `pancan_pcawg_2020`
+ MET500: `metastatic_solid_tumors_mich_2017`
+ OrigiMed: `pan_origimed_2020`

## System Requirements
### Software Dependencies

This project uses `renv` for dependency management. It should be sufficient to first install `renv` from within an R console:

```r
install.packages("renv")
```

Then to install all dependencies, from an R console in the root of this project:

```r
renv::restore()
```

This will install the specified versions of dependencies as listed in the `renv.lock` file, placing them in a directory under `renv/library/` -- which will often be loaded by default upon opening the RProject, but can be forced via `source("renv/activate.R")` from within an R console. The dependency installation process can take up to an hour if compiling all dependencies from source, but typically takes less than 30 minutes.

### Operating Systems

This project has been successfully run on Windows, Linux (Ubuntu family), and MacOS (Intel based) distributions. 

### Hardware

No non-standard hardware is required to run this project.

## Running the Project

If you have RStudio installed, you can double-click the `PNET_somatic_mutations.Rproj` file to open the project from your file manager. Once the project is open in RStudio, open the `wgd_disparities.Rmd` file. Just above where the file opens there will be a button labeled `Knit` -- clicking this button will run the code and produce an HTML report called `wgd_disparities.html`. Open this report in your preferred web browser to read the report. Running the project can take 20-40 minutes on a normal desktop computer.
