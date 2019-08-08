* Download VMware workstation 15 and [
ubuntu-16.04.6-desktop-amd64.iso](
http://hr.releases.ubuntu.com/16.04.6/)
* Operations in Ubuntu Terminal
    * Update the install method ```sudo apt update```
    * ```sudo apt install python2.7 python-pip```  install python2.7 which will reach the end of its life on Jan 1st 2020
    * Check the version of python on Ubuntu ```readlink -f $(which python) | xargs -I % sh -c 'echo -n "%: "; % -V'```
    * ```sudo apt install git``` install git
    * ```git clone -b release_17.09 https://github.com/galaxyproject/galaxy.git``` clone galaxy project v17.09
    * ```sh /home/yilinxia/galaxy/run.sh``` directory is the path you clone to . Run galaxy in local PC. will take a little long time to settle up

    * use ```http://localhost:8080/``` or ```http://127.0.0.1:8080/```to accessthe  homepage of the galaxy
    * use ```Ctrl+c``` to terminate the terminal to stop the server
    * clone the mtbls520 repo ```git clone https://github.com/korseby/container-mtbls520.git```
    * Mannually add tools to galaxy: search for file named: ```tool_conf.xml.main``` and add xmls to this file
```
<section name="Eco-Metabolomics" id="ecomet">
    <tool file="ecomet/mtbls520_01_mtbls_download.xml"/>
    <tool file="ecomet/mtbls520_02a_raw_extract.xml"/>
    <tool file="ecomet/mtbls520_02b_qc_extract.xml"/>
    <tool file="ecomet/mtbls520_02_extract.xml"/>
    <tool file="ecomet/mtbls520_03_quality_control.xml"/>
    <tool file="ecomet/mtbls520_04_preparations.xml"/>
    <tool file="ecomet/mtbls520_05a_import_maf.xml"/>
    <tool file="ecomet/mtbls520_05b_peak_picking.xml"/>
    <tool file="ecomet/mtbls520_06_import_traits.xml"/>
    <tool file="ecomet/mtbls520_07_species_diversity.xml"/>
    <tool file="ecomet/mtbls520_08a_species_shannon.xml"/>
    <tool file="ecomet/mtbls520_08b_species_unique.xml"/>
    <tool file="ecomet/mtbls520_08c_species_variability.xml"/>
    <tool file="ecomet/mtbls520_08d_concentration.xml"/>
    <tool file="ecomet/mtbls520_08e_species_features.xml"/>
    <tool file="ecomet/mtbls520_09_species_venn.xml"/>
    <tool file="ecomet/mtbls520_10_species_varpart.xml"/>
    <tool file="ecomet/mtbls520_11_species_nmds.xml"/>
    <tool file="ecomet/mtbls520_12_species_marchantia.xml"/>
    <tool file="ecomet/mtbls520_14_ecology_varpart.xml"/>
    <tool file="ecomet/mtbls520_15_ecology_pca.xml"/>
    <tool file="ecomet/mtbls520_16_ecology_rda.xml"/>
    <tool file="ecomet/mtbls520_17_ecology_splsda.xml"/>
    <tool file="ecomet/mtbls520_18_phylogeny.xml"/>
    <tool file="ecomet/mtbls520_19a_seasons_shannon.xml"/>
    <tool file="ecomet/mtbls520_19b_seasons_unique.xml"/>
    <tool file="ecomet/mtbls520_19c_seasons_variability.xml"/>
    <tool file="ecomet/mtbls520_19d_seasons_concentration.xml"/>
    <tool file="ecomet/mtbls520_19e_seasons_features.xml"/>
    <tool file="ecomet/mtbls520_22_seasons_pca.xml"/>
    <tool file="ecomet/mtbls520_23_seasons_rda.xml"/>
    <tool file="ecomet/mtbls520_24_seasons_nmds.xml"/>
  </section>
```
