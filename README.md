# ChromatographicAlignment
An approach for retention time alignment of LC-MS experiments for protein turnover studies from heavy water metabolic labeling

## I. Introduction
In protein turnover studies using atom-based labeling such as deuterium enriched drinking water or 15N labeled diet, the problem of missing values is further confounded. The labeling results in a composite spectrum in MS1, which is the overlap of the mass profiles of labeled and unlabeled forms of a peptide. As the label incorporation increases, the isotope profiles extend into the heavy mass isotopomers. Since the precursor selection in MS is made from the MS1 ions, the mass spectrometer often chooses heavy mass isotopomers for fragmentation. The isotope distributions of resulting fragment ions are different from those obtained from fragmentations of peptides with natural isotope abundances. The database search engines often confidently identify peptides fragmented from their monoisotopic peaks and may miss the identification of peptides that were selected for fragmentation from their label enriched mass isotopomers These two related effects, the changes in the isotope profiles of intact peptides and their fragment ions, lead to higher numbers of missing peptides in mass spectral datasets from metabolically labeled samples.

Here we show that RT alignment followed by feature matching and peptide identification transfer addresses the missing value problem and increases the proteome coverage and the accuracy of the turnover rate estimations in protein turnover studies using metabolic heavy water labeling. The RT is implemented in a software tool, d2ome, which automates the protein turnover rate estimation from samples metabolically labeled with heavy water. It is also available as a standalone tool, ChromatographicAlignment.


## II. Usage
To run the application, first, prepare a text file, [files.txt](https://github.com/rgsadygov/ChromatographicAlignment/blob/main/files.txt), that contains the list of mzML files in chronological order. Then use the following command 

    ```
    ChromatographicAlignment.exe files.txt
    ```

The Chromatographic Alignment application will generate .csv files that contain retention time pair-wise information between two successive experiments.
