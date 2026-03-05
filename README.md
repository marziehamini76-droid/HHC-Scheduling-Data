# HHC-Scheduling-Data
This document describes the data instances used in the computational experiments of the paper:
“A column generation-based heuristic algorithm for home healthcare scheduling and routing with synchronization and workload balance.”

Instance Overview
The data follow a daily planning framework and are categorized into three instance sizes:

•	Small instances

o	18 patients (20 visits)

o	5 samples

•	Medium instances

o	45 patients (50 visits)

o	3 samples

•	Large instances

o	72 patients (80 visits)

o	2 samples

Each sample includes five time-window scenarios (TW1–TW5), representing increasing temporal flexibility.

Parameter Generation Scheme
The parameters of the instances were generated as follows:

•	Patients requiring two caregivers

o	10% of the total number of visits

•	Caregiver skills

o	Randomly generated

o	Binary compatibility matrix (caregiver × patient)

•	Patients with high fatigue

o	Randomly selected subset of patients

•	Continuity of care scores

o	Generated from a discrete uniform integer distribution∼ Uniform{1,2,3}

•	Gender preference

o	Generated from a binary uniform distribution∼ Uniform{0,1}

All randomly generated parameters are explicitly included in the data files.

File Format Description

Each instance is provided as a plain text file containing:

•	General parameters (number of nodes, caregivers, normal weights (W))

•	Five time-window scenarios (TW1–TW5)

•	Service times and priority levels

•	Caregiver skill matrix

•	Gender preference matrix

•	Continuity of care score matrix
•	Travel time matrix
•	Synchronization requirements
Rows correspond to caregivers, and columns correspond to nodes whenever matrices are used.

Origin of the Base Data
The base structure of the instances (travel times, time windows, service times, and working time limits) is adapted from:
Bredström, D., & Rönnqvist, M. (2008). Combined vehicle routing and scheduling with temporal precedence and synchronization constraints. European Journal of Operational Research, 191 (1), 19–31. 

