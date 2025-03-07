################################################################
### readme.txt #################################################
################################################################

For: 'Connecting complex and simplified models of tipping elements: a nonlinear two-forcing emulator for the Atlantic meridional overturning circulation'

Amaury LARIDON1, Victor COUPLET2, Justin GERARD2, Wim THIERY1, Michel CRUCIFIX2

1Vrije Universiteit Brussel, Department of Water and Climate, Brussels, Belgium
2Université catholique de Louvain (UCLouvain), Earth and Life Institute ELI), 1348 Louvain-la-Neuve, Belgium

################################################################
05/03/2025 -- readme.txt file creation (J.G.)
05/03/2025 -- added files (J.G.)
05/03/2025 -- finalized (J.G.)
################################################################

Provided are the configuration files necessary to run:
        A] AMOC collapse simulation set

All experiments are run from: $HOME/cgenie.muffin/genie-main
(unless a different installation directory has been used) 

################ A] AMOC collapse ###############

# Main initial condition (preindustrial climate)
./runmuffin.sh cgenie.eb_go_gs_ac_bg.worjh2.BASES PUBS/published/Laridon_et_al_2025 JG.worjh2.main_eq.SPIN 15000

# Small perturbation of the AMOC with freshwater forcing
./runmuffin.sh cgenie.eb_go_gs_ac_bg.worjh2.BASES PUBS/published/Laridon_et_al_2025 JG.worjh2.fw_zigzag.SPIN 10000 JG.worjh2.main_eq.SPIN

# CO2 collapse
./runmuffin.sh cgenie.eb_go_gs_ac_bg.worjh2.BASES PUBS/published/Laridon_et_al_2025 JG.worjh2.T_collapse.SPIN 20000 JG.worjh2.main_eq.SPIN

# Freshwater collapse
./runmuffin.sh cgenie.eb_go_gs_ac_bg.worjh2.BASES PUBS/published/Laridon_et_al_2025 JG.worjh2.fw_collapse.SPIN 20000 JG.worjh2.main_eq.SPIN

# Hybrid collapse
./runmuffin.sh cgenie.eb_go_gs_ac_bg.worjh2.BASES PUBS/published/Laridon_et_al_2025 JG.worjh2.hybrid_collapse.SPIN 20000 JG.worjh2.main_eq.SPIN

################################################################
################################################################
################################################################
