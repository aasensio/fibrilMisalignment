# fibrilMisalignment

Bayesian hierarchical model for estimating the misalignment between magnetic fields and chromospheric fibrils.
This repository contains only the Stan (https://mc-stan.org) code to carry out the hierarchical
inference. Given the large number of variables during the Bayesian analysis, we use the automatic
variational approximation available in Stan. The code can be run using

    ./hierAzimuthVM_mixture init="0" variational eta=0.5 adapt engaged=0 tol_rel_obj=0.001 data file=penumbra.data output file=penumbra.csv
    sed '1,31d' penumbra.csv > penumbraFinal.csv

The files with the data are not provided in this repository because of their size. Send me an e-mail if
you want the data (aasensio@iac.es)