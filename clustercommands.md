

# Submitting jobs 

qsub -j y -o  /gpfs/cbica/home/doiphodn/log.txt /gpfs/cbica/home/doiphodn/model/submitScript.sh 1 /cbica/home/doiphodn/model/2.cnn_cluster.py

To specify type of GPU

qsub -j y -o  /gpfs/cbica/home/doiphodn/log.txt -l V100 /gpfs/cbica/home/doiphodn/model/submitScript.sh 1

/cbica/home/doiphodn/model/2.cnn_cluster.py



# Quick transfer

pscp "F:\NEHAL\UPENNACADS\SEM1\CISBE537\PROJECT\B3537_2018\B3537_2018\test_data_split1.pkl" HsuTs@cbica-cluster.uphs.upenn.edu:/cbica/home/hsuts/data

pscp "C:\Users\Nehal\Desktop" HsuTs@cbica-cluster.uphs.upenn.edu:/cbica/home/hsuts/model/

pscp HsuTs@cbica-cluster.uphs.upenn.edu:/cbica/home/hsuts/figures/* "C:\Users\Nehal\Desktop"

pscp HsuTs@cbica-cluster.uphs.upenn.edu:/cbica/home/hsuts/model/2.cnn_clusterTest3.py "C:\Users\Nehal\Desktop"


# Checking disk space

du -a | sort -n -r | head -n 5

# Checking jobs waiting

To see if it would be possible to ever run the job, if the cluster was completely empty, enter:
qalter -w v JOBID

To get more detail on why a job is not running at the moment, based on the resources in use by all jobs on the cluster, run:
qalter -w p JOBID

jobs in error state
qstat -explain E -j jobID 



