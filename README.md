# NiCo_v2

In the original version of NiCo cell type niche interactions plot was not good due to darker color used in the color map. 
There is a way to make the color opacity reduced using `alpha` value and change the colormap using `input_colormap`
and it can be used in the following way. 

```
celltype_niche_interaction_cutoff=0.1
saveas='png'
transparent_mode=False

sint.plot_niche_interactions_without_edge_weight(niche_pred_output,
niche_cutoff=celltype_niche_interaction_cutoff,
saveas=saveas,
transparent_mode=transparent_mode,
showit=True,
figsize=(10,7),
dpi=300, #Resolution in dots per inch for saving the figure.
input_colormap='jet', #Color map for node colors, based on matplotlib colormaps.
with_labels=True, #If True, displays cell type labels on the nodes.
node_size=500,  #Size of the nodes. 
linewidths=0.5, #Width of the node border lines. 
node_font_size=6, #Font size for node labels.
alpha=0.5, #Opacity level for nodes and edges. Maximum value 1 use full colors and 0 value use no colors. 
font_weight='bold' # Weight of the font for node labels is in bold letters. Other option is 'normal' 
)
```

<div align="center">
<img src="niche_interactions/Niche_interactions_without_edge_weights_R0.png" alt="" width="640">
</div>


```
sint.plot_niche_interactions_with_edge_weight(niche_pred_output,
niche_cutoff=celltype_niche_interaction_cutoff,
saveas=saveas,
transparent_mode=transparent_mode,
showit=True,
figsize=(10,7),
dpi=300,
input_colormap='winter',
with_labels=True,
node_size=300,
linewidths=1,
node_font_size=8,
alpha=0.1,
font_weight='normal',
edge_label_pos=0.35, #locations of the weight label from edge end 
edge_font_size=3 # font size of edge label 
)
```

<div align="center">
<img src="niche_interactions/Niche_interactions_with_edge_weights_R0.png" alt="" width="640">
</div>




If you want to get barplot in pathway then use `display_plot_as='barplot'` in the following commands. 

```
scov.pathway_analysis(cov_out,
choose_celltypes=['Stem/TA'],
NOG_pathway=50,
choose_factors_id=[2],
positively_correlated=True,
savefigure=True,
saveas='pdf',
correlation_with_spearman=True,
rps_rpl_mt_genes_included=False,
circlesize=12,
pathwayCutoff=0.5,
pathwayorganism='Mouse',
display_plot_as='barplot',
fontsize=12,
database=['GO_Biological_Process_2021','BioPlanet_2019','Reactome_2016'])
```


<div align="center">
<img src="Pathway_figures/posFa2_Stem_TA_c76_GO_Biological_Process_2021.png" alt="" width="640">
<img src="Pathway_figures/posFa2_Stem_TA_c76_BioPlanet_2019.png" alt="" width="640">  
<img src="Pathway_figures/posFa2_Stem_TA_c76_Reactome_2016.png" alt="" width="640">  
</div>


In the earlier dotplot you can control the size of dot using `circlesize=10` command. 
```
scov.pathway_analysis(cov_out,
choose_celltypes=['Stem/TA'],
NOG_pathway=50,
choose_factors_id=[2],
positively_correlated=True,
savefigure=True,
saveas='png',
correlation_with_spearman=True,
rps_rpl_mt_genes_included=False,
circlesize=10,
pathwayCutoff=0.5,
pathwayorganism='Mouse',
display_plot_as='dotplot',
fontsize=12,
database=['BioPlanet_2019'])
```

The output for circlesize 10 and 20 as follows. 
<div align="center">
<img src="Pathway_figures/posFa2_Stem_TA_c76_BioPlanet_2019_10.png" alt="" width="640">  
<img src="Pathway_figures/posFa2_Stem_TA_c76_BioPlanet_2019_20.png" alt="" width="640">  

</div>
