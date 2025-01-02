- [ ] #task Find some papers on DAG level scheduling/metrics 
- [ ] #task Perform literature search on common scheduling metrics

# Fair Share Scheduling

# Links

SchedMD docs:
  - SLUG presentation: [Slurm Priority, Fairshare and Fair Tree](https://slurm.schedmd.com/SLUG19/Priority_and_Fair_Trees.pdf)  
  - [https://slurm.schedmd.com/classic_fair_share.html](https://slurm.schedmd.com/classic_fair_share.html)
  - [https://slurm.schedmd.com/fair_tree.html](https://slurm.schedmd.com/fair_tree.html)
## What is Fair Share?

- One configurable priority factor amongst many:
```
Job_priority = (PriorityWeightAge) * (age_factor) + (PriorityWeightFairshare) * (fair-share_factor) + (PriorityWeightJobSize) * (job_size_factor) + (PriorityWeightPartition) * (partition_factor) + (PriorityWeightQOS) * (QOS_factor) + SUM(TRES_weight_cpu * TRES_factor_cpu, TRES_weight_ * TRES_factor_, ...)
```
- General idea of fair share: create an account hierarchy and assign a fractional share of the system to each account in the hierarchy.  If an account has used more than its “fair share” of the system in the recent past, then it gets a priority penalty going forward (and vice-versa).
- Usage is calculated based on a customizable cost function (cost associated with CPU, Mem, Disk, GPU).
- As a random example, maybe we charge 1 unit for each core and 0.25 units for each GB of memory:
```
         CPUs      Mem GB
Job1: (1 *1.0) + (60*0.25) = 16
Job2: (16*1.0) + (1 *0.25) = 16.25
Job3: (16*1.0) + (60*0.25) = 31**
```
- There is a “decay factor” to usage, so that usage gradually fades away as time goes on.
- Alternative is no decay but usage is periodically reset entirely (e.g., monthly, quarterly)