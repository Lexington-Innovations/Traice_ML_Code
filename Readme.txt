# TRAICE ML

## Step 1: Download the traice.sql data model file from sync repository.

## step 2: Clone this repository and rund the following command in the current directory terminal: pip3 install -r requirements.txt

## step 3: Run command in the terminal: python traice_batch.py {database_username} {database_password}n the following

## step4: The trace_batch.py process takes a long time to run. To allow quicker re-runs, it has been divided into ten steps. For details on each step, consult traice_batch.py or the underlying modules in the traice package:

Load
Merge
Breakout
Aggregate
Fit
HitList
HitListExp
KRIDetails
WellBeing
BranchBin
AML

Every time a step is run, its results are pickled to PICKLED_DIR, and a "completion" file for the step is written to the COMPLETION_DIR. If a completion file exists for a given step, it will not be re-run if traice_batch.py is triggered again. This allows the traice_batch.py to be re-run multiple times in case of failures or to perform analysis, without repeating work needlessly.

To "release" a step and allow it to run again, simply delete the corresponding completion file.
