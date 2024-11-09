# NiCo_v2


<div align="center">
<img src="Niche_interactions_without_edge_weights_R0.png" alt="" width="640">

</div>



If you want to get barplot in pathway then use display_plot_as='barplot' in the following commands. 

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
