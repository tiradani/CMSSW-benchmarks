
There will be an RPM later but for basic deployment :

 * Place H130GGgluonfusion_13TeV_cfi_GEN_SIM.py in /usr/libexec
 * Place cmssw-fastbenchmark-mc in /usr/bin
 * Place 30-benchmark.config in /etc/condor/config.d/ or extract contents to your condor config

Et voila. Once I do this, this is what I get after ~5 min running condor :

[root@compute-10-16 MC]# condor_status -l $HOSTNAME | grep MC
CMSTimePerEventMC = 46.9182
CMSTimePerEventMC = 46.9182
CMSTimePerEventMC = 46.9182
CMSTimePerEventMC = 46.9182

To run it by hand, just run /usr/bin/cmssw-fastbenchmark-mc
