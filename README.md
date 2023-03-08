Here is a fhicl to dump the artroot to a “celltree” format: celltree_protodune.fcl

You need to add a few changes to the default configuration:

```
physics.analyzers.wirecell.saveMC : false
physics.analyzers.wirecell.saveJSON : false
physics.analyzers.wirecell.saveRaw: true
physics.analyzers.wirecell.RawDigitLabel: "tpcrawdecoder:daq"  # label for RawDigits from simulation
```

Here is my ROOT script to read the “celltree” and fill a histogram for waveform: https://www.phy.bnl.gov/~wgu/protodune/celltree/dump_waveform.C
