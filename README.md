# Data Outputs and Links for a Phylogenetic Regionalization of the World's Turtles
Created by Dillon Jones. Contact: dilljone96@gmail.com

!["Results. The entire world is divided into various regions. Colors are unique for each region, and the hues correspond to various realms"](https://github.com/dilljone/Turtle-Phyloregionalization/blob/main/entire_world_no-label.jpg)
Masters Thesis for completion of the Evolutionary Biology Program at San Diego State University

The data and code provided herein do not include specific geographic occurrence records for the turtles (e.g. presence-absence matrices, individual taxa range maps) out of an abundance of caution for conservation.

# Important Links

Alongside the summary files, an interactive R shiny visualizer was created and can be found at: https://dillon-jones.shinyapps.io/Phyloregion_Visualizer_turt/

This thesis heavily compares the phyloregions to the Taxonomic regions created by Ennen et al. 2020. See their publication here: https://doi.org/10.1016/j.biocon.2019.108323
and their Region visualization here: https://tnaci-fin.tnaqua.org/arcgis/apps/View/index.html?appid=9addfcaf1e1043df85d6498d7d105540

We also compare heavily to the ecoregions provided by the World Wildlife Fund. An ArcGIS app with those regions can be found here: https://www.arcgis.com/apps/View/index.html?appid=d60ec415febb4874ac5e0960a6a2e448

# Table of Contents
## S1 - Taxonomy-Constraints-TACT.csv 
Description: A .csv file of taxonomic constraints for feeding into TACT. Columns indicate the following taxonomic ranks: order, suborder, superfamily, superfamily_clade, family, family_clade, genus, clade, taxon. Columns with the _clade suffix were used to constrain taxa within a particular rank.

## S2 - phyloregion_summary_stat_full.csv = A .csv file that contains all the summary statistics for the phyloregions. Columns with their descriptions are as follows
  - **realm**:
    One of Six Realms the phyloregion belongs to. PALE = Palearctic; SSAF = SubSaharan Africa; NOAM = North America; SOAM = South America; ASIA = IndoMalaya-Asia; AUST = Australasia
   - **cluster**:
     Which phyloregion did it belong to (i.e. cluster 37 is equal to PR37)
  - **n_taxa**:
    Number of taxa detected within the phyloregion
  - **n_edge**:		
  Number of EDGE taxa within the phyloregion
  - **mean_edge**:
  Mean EDGE score for the phylroegion
  - **n_lc**:		
  Number of Least Concern taxa according to IUCN
  - **n_nt**:
  Number of Near Threatened taxa according to IUCN
  - **n_vu**:
  Number of Vulnerable taxa according to IUCN
  - **n_en**:
  Number of Endangered taxa according to IUCN
  -	**n_cr**:
  Number of Endangered taxa according to IUCN
  -	**n_hydro**:
  Number of Hydrobasin units in the Phyloregion
  -	**area_km2**:
  Area of phyloregion in Square Kilometers
  -	**end_per**:
  Percent of area with significant phylogenetic endemism
  -	**end_km2**:
  Area with significant phylogenetic endemism as square kilometers
  -	**No_end_km2**:
  Area with NO significant phylogenetic endemism as square kilometers
  -	**neoend_per**:
  Percent of area with significant phylogenetic neo-endemism
  -	**neoend_km2**:
  Area with significant phylogenetic neo endemism as square kilometers
  -	**paleoend_per**:
  Percent of area with significant phylogenetic paleo endemism
  -	**paleoend_km2**:
  Area with significant phylogenetic paleo endemism as square kilometers
  -	**mixedend_per**:
  Percent of area with significant phylogenetic mixed endemism
  -	**mixedend_km2**:
  Area with significant phylogenetic mixed endemism as square kilometers
  -	**superend_per**:	
  Percent of area with significant phylogenetic super endemism
  -	**superend_km2**:
  Area with significant phylogenetic super endemism as square kilometers

## S3 - threat_levels_taxa.csv
A .csv file containing each taxon in this study and their associated threat metrics.
- taxon: Taxon name
- Order: Taxonomic Order of the taxon
- Family: TaxonomicFamily of the taxon
- genus: Taxonomic genus of the taxon
- clade: The species-level clade used in the TACT addition tree
- IUCN: IUCN threat level
- TFTSG: Threat level provided by the TFTSG. When not provided, it is the same threat level as the IUCN
- Threat: The Threat level used for EDGE calculation
- Threat_code: A 2-letter code corresponding to the Threat column
- EDGE_Scores: The EDGE score calculated for the taxa
- EDGE_species: A column determining if a taxon is an EDGE taxon or not.
- TACT-addition: Cells marked with an X indicate the taxon was added via the TACT method.

## S4 - ecoregion_prop.csv
  A .cscv file containing the degree by which World Wildlife Fund Ecoregions overlap with Phyloregions as a decimal proportion. Column headings correspond with Phyloregion cluster number, while row names correspond to the WWF ecoregion. 
