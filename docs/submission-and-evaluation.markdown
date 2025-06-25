---
layout: page
title: Submission and Evaluation
permalink: /submission-and-evaluation/
weight: 3
---

## Submission
### **Model Submission Requirements**:
Please provide your solution to [TBD](). Each team can submit multiple times and we will only use the latest version you submit. Your models and scripts should be accessible and runnable. 

Please submit the following three items:
1. **Neural Network Components**: Include your model definition, training script, inference script, and any trained weights or checkpoints.
2. **Code Packaging**: Provide all source files, a `requirements.txt` listing dependencies, and a brief `README.md` with setup and run instructions.
3. **Result files**: Your output should be saved in a txt file inside the `rlsolver/result` folder. Take a data file `rlsolver/data/syn_BA/BA_100_ID0.txt` as an example, the output result file is `rlsolver/result/syn_BA/BA_100_ID0.txt`. Each line represents the assignment of a node to one of two sets (for MaxCut):

```
   1 2
   2 1
   3 2
   4 1
   5 2
```
- The first number is the node ID (starting from 1)  
- The second number is the assigned set (1 or 2)  

This format directly follows the example in the README. Make sure to include all nodes and follow the naming exactly.

### **Paper Submission Requirements**:
Each team should submit short papers with 3 complimentary pages and up to 2 extra pages, including all figures, tables, and references. The paper submission is through [the special track](https://www.cloud-conf.net/cscloud/2025/cscloud/cfp_files/RLSolver_CFP.pdf) and should follow its instructions. Please include “RLSolver Contest Task 1/2” in your abstract.

## Evaluation

#### **Ranking rules**

Each team will be evaluated separately on each of the datasets according the task's metric, i.e., objective value. This metric will be averaged across all instances in the test dataset, resulting in an individual ranking for each dataset. 

For example, for the task I, team A might obtain ranks 3, 8, 1 respectively in 3 datasets, while team B obtains ranks 2, 2, 15. Then, for each team those three ranks will be multiplied together to obtain the overall score of the team. For example, team A will obtain a score of 3x8x1=24 while team B obtains 2x2x15=60. 

The team with the lowest overall score wins. The objective value is the most important metric. If several teams have the same score of objective value, we will compare the inference time. 

Submissions are assessed in two categories:
#### 1. Distribution-wise Reinforcement Learning Methods
- **Training Time**: total time spent training across instances  
- **Inference Time**: average time to produce a solution for a single test graph  
- **Objective Value**: primary score (e.g. MaxCut value, tour length, etc.)

#### 2. Conventional Methods
- **Running Time**: time to solve each test instance (no training phase)  
- **Objective Value**: final score achieved on the problem

| Method Type               | Time Metric              | Optimization Metric |
|---------------------------|--------------------------|---------------------|
| Distribution-wise RL      | Training + Inference     | Objective Value     |
| Conventional (non-RL)     | Running Time only        | Objective Value     |


**Notes:**  
- **Objective Value** is defined by the problem (higher is better unless stated otherwise).  
- **Inference Time** is measured on GPU (when applicable) and averaged over all test cases.  
- All methods run on the same standardized server under fixed resource limits.  
- Final rankings may combine time and objective metrics with track-specific weights.  


### **Paper Assessment**:
The assessment of the paper will be conducted by invited experts and professionals. The judges will independently rate the data and model analysis, robustness and generalizability, innovation and creativity, organization and readability, each accounting for 20% of the qualitative assessment. 

Note that since the paper submission will follow the timeline on the [Special Track: Reinforcement Learning for Combinatorial Optimizations](https://www.cloud-conf.net/cscloud/2025/cscloud/cfp_files/RLSolver_CFP.pdf) and the models can be submitted later than the paper, the discussion of results and performance will not be counted in the paper assessment. 
