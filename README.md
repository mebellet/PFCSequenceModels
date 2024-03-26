# PFCSequenceModels
Code used in [Bellet et al. 2024](https://www.cell.com/cell-reports/fulltext/S2211-1247%2824%2900280-8)

There is one jupyter notebook per main figure.

Supplementary analyses are contained in the supplementary notebooks.

Download the data on figshare (see the manuscript for the DOI) and edit the file path in the scripts accordingly.

First run the code in preprocessing.ipynb and then the figure scripts one after the other. Scripts in later notebooks are based on the output of previous notebooks.

### Explanation of variables in the pandas dataframes:

Each row in the dataframe corresponds to the presentation of one stimulus (not an entire sequence).

- PFC_MU: Prefrontal multi-unit activity. List of 96 recording channels. Spike times in sec. relative to stimulus onset.

- PPC_MU: Parietal muti-unit activity.

- PFC_SU: Prefrontal single-unit activity. List of N isolated neurons.

- PPC_SU: Parietal single-unit activity.

- TrialID: Number of trial of the stimulus.

- ItemID: Position of the stimulus in the sequence, [0,1,2,3] 

- StimID: Stimulus A [0] or B [1]

- StimName: Name of the stimulus (string)

- StimOn: Onset time of the stimulus (sec. from start)

- blockID: Number of the block in a session, [0,1,2,3] Note: 4 is exceptional and can be discarded.

- blockType: xx [0] or xY [1] block

- date: date of recording yyyymmdd 

- StimDur: Duration of stimulus presentation (msec)

- ISIDur: Duration of inter-stimulus interval (msec)

- RewardOn: Reward onset time relative to start (sec). NaN for ItemID = [0,1,2]
