# SpatialMoranModel

Goal: Simulate finite populations of cells on a 1D lattice that have some probability of losing a plasmid at each division.

Create cell objects with attributes for their division time and spatial location.

Cells divide at either exponentially distributed times with rate a_m/tau for plasmid free cells or a_w/tau for plasmid containing cells, or they divide deterministically once they reach age a_m or a_w.

When a cell divides, one daughter takes the place of the mother and the other daughter takes the place directly to the right or to the left of the mother. The probability of going right or left depends on the location of the mother cell. If the daughter takes the place on the right, the cells with higher location tags get shifted up one location and the cell with the highest tag gets removed. If the daughter takes the place on the left, the cells with lower location tags get shifted down one location and the cell with the lowest tag gets removed.

Figures: 
 - single trajectories for number of plasmid free cells and plasmid containing cells over time, and single trajectories for fraction of plasmid free cells over time, for both exponentially distributed and delta distributed division times
 - Histograms depicting frequency of plasmid-free cell takeover times for 1000 simulations (takes a long time to run) compared to theoretical takeover time pdf for mother machiene for delta distributed division times

