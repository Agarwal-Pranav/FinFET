#Interface Trap Analysis in Multi-Fin FinFET Technology
#Project Overview
This project investigates the impact of Interface Traps on the reliability of single and multi-fin FinFET structures. Specifically, it focuses on Negative Bias Temperature Instability (NBTI), a critical degradation mechanism in modern sub-10nm nodes.By modeling these structures using Silvaco TCAD, we analyzed how trap-induced shifts affect both DC (threshold voltage, drain current) and AC (transconductance, capacitance) parameters, providing a dataset suitable for training Machine Learning models to predict device aging.
#Key FeaturesDevice Modeling:
Full 3D simulation of single-fin and multi-fin FinFET geometries.
#Reliability Focus:
Detailed analysis of NBTI-induced degradation.Parameter Extraction: Comparison of $V_{th}$ shift, $I_{on}/I_{off}$ ratios, and gate capacitance ($C_{gg}$).Scalability Analysis: Evaluation of how multi-fin configurations mitigate or exacerbate trap sensitivity compared to single-fin counterparts.Technical Methodology1. TCAD Simulation (Silvaco)The devices were modeled using the Silvaco TCAD suite (Victory Device/Atlas).
#Physics Models: 
Drift-Diffusion, Fermi-Dirac statistics, and mobility degradation models.Trap Modeling: Interface traps ($N_{it}$) were introduced at the $Si/HfO_2$ interface to simulate the NBTI effect.
