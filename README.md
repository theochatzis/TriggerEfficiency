## Trigger Efficiencies using the Orthogonal Dataset Method



## Setup:
```
cmsrel CMSSW_13_3_1_patch1
cd CMSSW_13_3_1_patch1/src
cmsenv
git clone https://github.com/cms-nanoAOD/nanoAOD-tools.git PhysicsTools/NanoAODTools
scram build -j 4

git clone https://github.com/theochatzis/TriggerEfficiency.git
cd TriggerEfficiency
```

## Usage of codes:

Python scripts use NanoAOD data files. 
Scripts are of two types:

- `getEff*`: Those scripts make the production of histograms from the NanoAOD files applying the corresponding quality cuts for offline objects. There are histograms of "numerators" passing the triggers and "denominator" passing the reference `HLT_IsoMu24 || HLT_Mu50`
- `plot*Eff*`: These scripts calculate the efficiencies and do the plotting. Plots are stored in the `plots` directory.

There are different cases of analysis use cases:

- `Had`: corresponds to study of high pT AK8 triggers.
- `PFMET`, `PFMETNoMu`: Study of MET triggers.
- `PFHT`: Hadronic energy sum HT triggers.  
