# Liquid Argon Experiment tune with experimental INCL "FSI" model

This is a copy of the AR23 physics model but instead of using the hA FSI model, we use Liang Liu's experimental INCL model:
repo:https://github.com/LiangLiu212/Generator/tree/feature/genie-incl634-sbnd
sha:6f99d2bd754d72cb71dea53eed217c9b9db15195

INCL is supposed to have a more sophisticated model for de-exciting the nucleus and predicts deuteron, alpha, etc emission.
GENIE handling of de-excitation photons is off because we offload de-excitation physics to INCL.

What follows is copied from AR23:

This configuration is the result of requests from SBN and DUNE collaborations.
It is designed to serve as baseline model for SBN analyses. 

The physics content is the following
 - Valencia model for 1p1h, using z-expansion
 - SuSAv2 model for 2p2h
 - Spectral function like approach for the Local Fermi Gas
    - Includes events with SRC-like missing momentum within the bulk of the $p_{miss}$ distribution, 
      but not extending pass the LFG cutoff in $p_{miss}$.
 - The parameters related to pion production are taken from the G18_10a_02_11b tune in order to ensure a better starting point. 
 - De-exitation photons are enabled for Argon
