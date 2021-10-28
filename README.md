## Finding additional segmentations (WIP)

Many institutions have published their own segmentations as NIfTI, NRRD or RAW files.

In this table we curate a few segmentations including their source(s), and link (in the **files** field of the table) to their folders in this repository.

| Name | Organism | Source | Format | Ref. space | Voxel dim. | Dir. | Ontology | Files | Ref | 
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ABA Human Half | _H. sapiens_ | [source](https://community.brain-map.org/t/allen-human-reference-atlas-3d-2020-new/405) | NIfTI | MNI152 | 500 &mu;m | RAS | [ontology](http://help.brain-map.org/display/api/Downloading+an+Ontology%27s+Structure+Graph) | [files](https://github.com/langleylab/coldcuts_segmentations/tree/main/ABA_Human_full) | [Ding et al.](https://pubmed.ncbi.nlm.nih.gov/27418273/) _J. Comp. Neurol._ 2016 |
| ABA Human Full | _H. sapiens_ | [source](https://community.brain-map.org/t/allen-human-reference-atlas-3d-2020-new/405) | NIfTI | MNI152 | 500 &mu;m | RAS | [ontology](http://help.brain-map.org/display/api/Downloading+an+Ontology%27s+Structure+Graph) | [files](https://github.com/langleylab/coldcuts_segmentations/tree/main/ABA_Human_half) | [Ding et al.](https://pubmed.ncbi.nlm.nih.gov/27418273/) _J. Comp. Neurol._ 2016 |
| Hammersmith Atlas | _H. sapiens_ | [source](http://brain-development.org/brain-atlases/adult-brain-atlases/adult-brain-maximum-probability-map-hammers-mith-atlas-n30r83-in-mni-space/) | NIfTI | MNI152 | 1 mm | LAS | custom ontology | [files](https://github.com/langleylab/coldcuts_segmentations/tree/main/Hammersmith) | [Hammers et al.](http://www.ncbi.nlm.nih.gov/pubmed/12874777) _Human Brain Mapping_ 2003, [Gousias et al.](http://www.ncbi.nlm.nih.gov/pubmed/18234511) _NeuroImage_ 2007, [Faillenot et al.](http://doi.org/10.1016/j.neuroimage.2017.01.073) _NeuroImage_ 2017, [Wild et al.](http://doi.org/10.1371/journal.pone.0180866) PLoS ONE 2017, | 
| HCP MMP 1.0 | _H. sapiens_ | [source](https://neurovault.org/collections/1549/) | NRRD | MNI152 | 500 &mu;m | RAS | custom ontology | [files](https://raw.githubusercontent.com/langleylab/coldcuts_segmentations/tree/main/HCP_MMP) | [Glasser et al.](http://doi.org/10.1038/nature18933) _Nature_ 2016 |
| ABA Mouse CCF2017 | _M. musculus_ | [source](http://download.alleninstitute.org/informatics-archive/current-release/mouse_ccf/annotation/ccf_2017/structure_masks/) | NRRD | CCFv3 | 50 &mu;m | PIR | [ontology](http://help.brain-map.org/display/api/Downloading+an+Ontology%27s+Structure+Graph) | [files](https://github.com/langleylab/coldcuts_segmentations/tree/main/ABA_Mouse_CCFv3) | [Lein et al.](https://www.nature.com/articles/nature05453) _Nature_ 2007 |
| Drosophila JRC2010 | _D. melanogaster_ | [source](https://www.janelia.org/open-science/jrc-2018-brain-templates) | NRRD | JRC2010 | 38 &mu;m | RAS | custom ontology | [files](https://raw.githubusercontent.com/langleylab/coldcuts_segmentations/tree/main/Drosophila_JRC2010) |  [Bogovic et al.](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0236495) _PlOS ONE_ 2020, [Ito et al.](https://www.cell.com/neuron/fulltext/S0896-6273(13)01178-1) _Neuron_ 2014 |
| Chimpanzee Davi130 Juna.Chimp | _P. troglodytes_ | [source](https://www.chimpanzeebrain.org/node/2347) | NIfTI | Juna.Chimp | 500 &mu;m | LAS | custom ontology | [files](https://github.com/langleylab/coldcuts_segmentations/tree/main/Chimp_Davi130) | [Vickery et al.](https://pubmed.ncbi.nlm.nih.gov/33226338/) _eLife_ 2020 |

 
In this section we present some curated segmentations that have already been processed through `coldcuts` and are available as `segmentation` class objects.

## ABA Human (half and full)

This segmentation was released by the Allen Institute as a volume file for either half emisphere or the full cerebrum, registered to the MNI152 reference space. It is based on the work by Ding et al. 

It contains **141** annotated structures, both subcortical and cortical. The structure ontology was provided by the Allen Institute, and the segmentation follows the original ABA color scheme.

The RDS file contains the `segmentation` class object, with maximum projections for all structures in all planes.

<p float="left">
  <img src="https://raw.githubusercontent.com/langleylab/coldcuts_segmentations/main/ABA_Human_half/ABA_Human_half_sagittal_mp.png" width="450" />
  <img src="https://raw.githubusercontent.com/langleylab/coldcuts_segmentations/main/ABA_Human_full/ABA_Human_full_sagittal_mp.png" width="450" /> 
 </p>

<p float="left"> 
  <img src="https://raw.githubusercontent.com/langleylab/coldcuts_segmentations/main/ABA_Human_half/ABA_Human_half_coronal_mp.png" width="450" />
  <img src="https://raw.githubusercontent.com/langleylab/coldcuts_segmentations/main/ABA_Human_full/ABA_Human_full_coronal_mp.png" width="450" /> 
</p>

<p float="left"> 
  <img src="https://raw.githubusercontent.com/langleylab/coldcuts_segmentations/main/ABA_Human_half/ABA_Human_half_axial_mp.png" width="450" />
  <img src="https://raw.githubusercontent.com/langleylab/coldcuts_segmentations/main/ABA_Human_full/ABA_Human_full_axial_mp.png" width="450" /> 
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/langleylab/coldcuts_segmentations//main/ABA_Human_half/ABA_Human_ontology.png" width="900" />
</p>

## Hammersmith Atlas

This segmentation was released by the Computational BioImage Group at Imperial College London as a volume file and is based on the work by Hammers et al., Gousias et al., Faillenot et al., and Wild et al. It contains the full cerebrum, registered to the MNI152 reference space. The volume is originally LAS oriented, but was rotated to RAS before drawing. . 

It contains **95** annotated structures, both cortical and subcortical, divided in left and right. The structure ontology is custom, largely based on the Supplementary Table A2 from [Yaakub et al. 2020](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7028906/) and grouped according to lobes and brain developmental origin. The segmentation follows a "hierarchical random" color scheme.

The RDS file contains the `segmentation` class object, with maximum projections for all structures in all planes.

<p align="center">
  <img src="https://raw.githubusercontent.com/langleylab/coldcuts_segmentations/main/Hammersmith/Hammersmith_Human_sagittal_mp.png" width="600" />
  <img src="https://raw.githubusercontent.com/langleylab/coldcuts_segmentations/main/Hammersmith/Hammersmith_Human_coronal_mp.png" width="600" /> 
  <img src="https://raw.githubusercontent.com/langleylab/coldcuts_segmentations/main/Hammersmith/Hammersmith_Human_axial_mp.png" width="600" />
  <img src="https://raw.githubusercontent.com/langleylab/coldcuts_segmentations/main/Hammersmith/Hammersmith_Human_ontology.png" width="900" />
</p>


## HCP MMP 1.0

This segmentation was released by the Department of Neuroscience, Washington University Medical School, St. Louis, MO, USA as a volume file and is based on the work by Glasser et al. It contains the full cerebrum, registered to the MNI152 reference space. As explained [here](https://figshare.com/articles/dataset/HCP-MMP1_0_projected_on_MNI2009a_GM_volumetric_in_NIfTI_format/3501911?file=5534024) it should be **used with care**.

It contains **180** annotated structures, only cortical. The structure ontology is custom, largely based on the Supplementary Table A2 from Glasser et al. and grouped according to lobes and brain developmental origin. **Please note that custom ontologies may not be correct in their higher order grouping**. The segmentation follows a "hierarchical random" color scheme.

The RDS file contains the `segmentation` class object, with maximum projections for all structures in all planes.

<p align="center">
  <img src="https://raw.githubusercontent.com/langleylab/coldcuts_segmentations//main/HCP_MMP/HCP_MMP1_Human_sagittal_mp.png" width="600" />
  <img src="https://raw.githubusercontent.com/langleylab/coldcuts_segmentations//main/HCP_MMP/HCP_MMP1_Human_coronal_mp.png" width="600" /> 
  <img src="https://raw.githubusercontent.com/langleylab/coldcuts_segmentations//main/HCP_MMP/HCP_MMP1_Human_axial_mp.png" width="600" />
  <img src="https://raw.githubusercontent.com/langleylab/coldcuts_segmentations//main/HCP_MMP/HCP_MMP1_Human_ontology.png" width="900" />
</p>

## ABA Mouse CCF2017

This segmentation was released by the Allen Institute as a volume file, registered to the CCFv3 reference space. It is based on the work by Lein et al. 

It contains **670** annotated structures, both cortical and subcortical. The structure ontology was provided by the Allen Institute, and the segmentation follows the original ABA color scheme. The original volume is PIR oriented, but was rotated to RAS before drawing.

The RDS file contains the `segmentation` class object, with maximum projections for all structures in all planes.


<p align="center">
  <img src="https://raw.githubusercontent.com/langleylab/coldcuts_segmentations/main/ABA_Mouse_CCFv3/ABA_mouse_50um_sagittal_mp.png" width="600" />
  <img src="https://raw.githubusercontent.com/langleylab/coldcuts_segmentations/main/ABA_Mouse_CCFv3/ABA_mouse_50um_coronal_mp.png" width="600" /> 
  <img src="https://raw.githubusercontent.com/langleylab/coldcuts_segmentations/main/ABA_Mouse_CCFv3/ABA_mouse_50um_axial_mp.png" width="600" />
  <img src="https://raw.githubusercontent.com/langleylab/coldcuts_segmentations/main/ABA_Mouse_CCFv3/ABA_mouse_50um_ontology.png" width="900" />
</p>

## Drosophila JRC2010

This segmentation was released by the Janelia Research Campus, Howard Hughes Medical Institute, Ashburn, VA, USA as a volume file, registered to the JRC2010 reference space. It is based on the work by Bogovic et al. and Ito et al.

It contains **75** annotated structures, divided in left and right. The structure ontology is custom, largely based on the Table 1 from Ito et al. **Please note that custom ontologies may not be correct in their higher order grouping**. The segmentation follows a "hierarchical random" color scheme.

The RDS file contains the `segmentation` class object, with maximum projections for all structures in all planes.

<p align="center">
  <img src="https://raw.githubusercontent.com/langleylab/coldcuts_segmentations/main/Drosophila_JRC2010/Drosophila_JRC2010_sagittal_mp.png" width="600" />
  <img src="https://raw.githubusercontent.com/langleylab/coldcuts_segmentations/main/Drosophila_JRC2010/Drosophila_JRC2010_coronal_mp.png" width="600" /> 
  <img src="https://raw.githubusercontent.com/langleylab/coldcuts_segmentations/main/Drosophila_JRC2010/Drosophila_JRC2010_axial_mp.png" width="600" />
  <img src="https://raw.githubusercontent.com/langleylab/coldcuts_segmentations/main/Drosophila_JRC2010/Drosophila_JRC2010_ontology.png" width="900" />
</p>

## Chimpanzee Davi130 Juna.Chimp

This segmentation was released by the National Chimpanzee Brain Resource (USA) as a volume file, registered to the Juna.Chimp reference space. It is based on the work by Vickery et al. It contains **130** annotated structures, divided in left and right. The structure ontology is custom, largely based on the Table 1 from Ito et al. **Please note that custom ontologies may not be correct in their higher order grouping**. The segmentation follows a "hierarchical random" color scheme. The original volume is LAS oriented, but was rotated to RAS before drawing.

The RDS file contains the `segmentation` class object, with maximum projections for all structures in all planes.

<p align="center">
  <img src="https://raw.githubusercontent.com/langleylab/coldcuts_segmentations/main/Chimp_Davi130/Chimp_Davi130_sagittal_mp.png" width="600" />
  <img src="https://raw.githubusercontent.com/langleylab/coldcuts_segmentations/main/Chimp_Davi130/Chimp_Davi130_coronal_mp.png" width="600" /> 
  <img src="https://raw.githubusercontent.com/langleylab/coldcuts_segmentations/main/Chimp_Davi130/Chimp_Davi130_axial_mp.png" width="600" />
  <img src="https://raw.githubusercontent.com/langleylab/coldcuts_segmentations/main/Chimp_Davi130/Chimp_Davi130_ontology.png" width="900" />
</p>


