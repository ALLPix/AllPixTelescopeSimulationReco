# AllPixTelescopeSimulationReco
Steering templates and configuration file example for reconstruction of the data simulated with AllPix


source setup_reco.sh to setup EUTELESCOPE environnement 


create the lcio-raw , histo, db, logs, results folders if they to do not exist already, 

put .slcio files in lcio-raw in the following format run%06i.slcio 




Running reconstruction 
----------------------


conversion (create hotpixel-db file )

jobsub.py -c configSimulation.cfg converter RunNumber

clustering 

jobsub.py -c configSimulation.cfg clusearch  runNumber

Hitmaker 

jobsub.py -c configSimulation.cfg hitmaker  runNumber

Fitter 

jobsub.py -c configSimulation.cfg fitter  runNumber
