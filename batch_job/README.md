# Example of Running PyTorch on Adroit

```
$ ssh <YourNetID>@adroit.princeton.edu
$ git clone https://github.com/PrincetonUniversity/intro_pytorch
$ cd intro_pytorch/batch_job
```

Download the MNNIST dataset on the login node:

```
$ module load anaconda3/2023.9
$ conda activate /home/jdh4/.conda/envs/torch-env
$ python download_mnist.py
```

In this example, a pre-installed Conda environment is being.

Submit the job to the Slurm scheduler:

```
$ sbatch --reservation=pytorch job.slurm
```

Note: After the workshop remove `--reservation=pytorch` since it no longer applies.

After the job finishes, you can inspect the output:

```
$ cat slurm-*.out
```