# Example of Running PyTorch on Adroit

```
$ ssh <YourNetID>@adroit.princeton.edu
$ git clone
$ cd intro_pytorch/batch_job
$ module load anaconda3/2023.9
$ conda activate /home/jdh4/.conda/envs/torch-env
$ python download_mnist.py
```

Submit the job:

```
$ sbatch --reservation=pytorch job.slurm
```

After the workshop remove `--reservation=pytorch` since it no longer applies.

After the job finishes, you can inspect the output:

```
$ cat slurm-*.out
```
