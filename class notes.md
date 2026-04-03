class notes

4/3/26

conda activate genomics

cd ~/project repo

## make output directories. only need to do this once
mkdir -p poly-G-trimmed html results metadata data/fastqs

## New polyG filter only
cd data/fastqs

## set a variable, copied from qime2_parameters.sh
polyg_len=200 

## trim up fastqs : run polyG filter which removes PolyG tails and also filters out reads that are too short 
chmod +x ../code/polyGfilter.sh
../code/polyGfilter.sh ${polyg_len}

## or can just do:
../code/polyGfilter.sh 200

## remove empty files before qime import




