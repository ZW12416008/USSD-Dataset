USSD Dataset (Urban Salient Sound Dataset)
This repository provides the Urban Salient Sound Dataset (USSD), a crowdsourced dataset of salient sound events collected in public spaces of Dalian, China. The dataset is designed for sound event detection and urban acoustic environment analysis.

Dataset Overview
The dataset was constructed to capture salient sound events (SSEs) in diverse urban environments. Salient sounds are those that stand out perceptually in an acoustic scene (e.g., traffic horns, human voices, bird calls, mechanical noise, or quiet states).
Total samples: 3094 audio clips
Clip length: 10 seconds (wav format, 16-bit, 48 kHz, mono)
Categories: 22 fine-grained sound event classes, grouped into 5 main categories:
Natural sounds
Human sounds
Traffic sounds
Mechanical sounds
Silence/Quiet
Each clip is labeled with one or multiple salient sound events. Both single-source and mixed-source recordings are included.

Data Collection
Study area: 15 representative public spaces in Dalian, located near:
Transportation facilities (high sound pressure levels, dynamic changes)
Commercial centers (high density, periodic patterns)
Residential areas (dominated by resident activities)
Mixed-use public facilities (diverse sound types)
Recording equipment:
Device: Luyin sound recorders LY-M-01 (software v1.7.2)
Format: WAV, mono, 16-bit, 48 kHz
Recording campaign:
Period: October 2024
Weather: sunny, avg. temp. 18.5°C
Duration: ≥1 week continuous recording per site
Total audio collected: over 3000 hours
From each site’s recordings, samples were extracted at regular intervals to ensure spatial and temporal balance.

<img width="817" height="488" alt="image" src="https://github.com/user-attachments/assets/6b888fa6-9d3e-4bb5-a419-d9e60b5e52f9" />

<img width="826" height="183" alt="image" src="https://github.com/user-attachments/assets/a711a5b3-0c4e-4ed9-9763-bcf551d4c78a" />

Annotation Process
The dataset was labeled through a crowdsourcing mechanism with multiple steps:
1. Pre-annotation training:
5 trained annotators standardized the labeling scheme.
Classification scheme refined from ISO standards and prior datasets (e.g., UrbanSound8K, ESC-50).
Added Silence as a new category.
2. Crowdsourcing:
80 recruited volunteers participated after a short training.
Online loudness calibration ensured consistent listening conditions (~65 ± 10 dB).
3. Quality control:
Annotators’ classification accuracy (SCA) and consistency (Cohen’s Kappa, CK) were evaluated.
Only high-performing annotators (n=60) continued with full annotation.
Each clip labeled by ≥5 annotators; majority vote used as final label.
Samples with low agreement (<60% consensus) were discarded.

<img width="622" height="373" alt="image" src="https://github.com/user-attachments/assets/ec4c1105-d9f5-44f8-9045-ed0004de588b" />

Dataset Composition
3094 labeled audio clips
1749 single-event clips
1345 mixed-event clips
Category distribution (examples):
Traffic: 1076 samples
Human: 1083 samples
Natural: 547 samples
Mechanical: 276 samples
Quiet: remainder

<img width="865" height="487" alt="image" src="https://github.com/user-attachments/assets/a7a670b7-7248-4a3c-afd3-a32e44f66174" />

Model Benchmark
We trained an ECAPA-TDNN model on USSD:
Average accuracy (22 subcategories): 91.3%
Average accuracy (5 main categories): 93.9%
Best-performing class: Mechanical sounds (99.1%)
Most common errors: Confusions within the same top-level category
This demonstrates that the dataset is suitable for deep learning-based sound event detection in complex urban environments.

<img width="709" height="499" alt="image" src="https://github.com/user-attachments/assets/892b6486-5b27-4906-8ebc-1ad932ed40d1" />

<img width="410" height="331" alt="image" src="https://github.com/user-attachments/assets/29ae5648-9d36-4acf-934e-3b430cebe2b6" />

In addition, we assessed the model’s ability to fit human perception of salience:
A comparison was conducted between human annotations in the Pre-SSD dataset and the model’s predictions.
The overall agreement (ACC) reached 83.33%.
This result demonstrates that the model successfully captures the regularities of human perception of salient sound events.
Visualization:
Each grid represents a 10-second sound sample.
✅ Green dots indicate agreement between human judgments and model predictions.
❌ Red areas indicate disagreement.
This confirms that the USSD dataset reflects representative and valid human perceptual judgments of salient sound events.

<img width="449" height="228" alt="image" src="https://github.com/user-attachments/assets/63f9cbc0-74bb-4f4a-9352-e5c103fbb057" />


Access
The dataset is shared via Baidu Cloud:
This dataset contains annotations of salient sound events in urban environments.
通过网盘分享的文件：USSD Dataset 链接: https://pan.baidu.com/s/1lD4la3nsK2-y2rnkr5BBxg 
“Shared via Baidu Cloud: USSD Dataset
Link: https://pan.baidu.com/s/1lD4la3nsK2-y2rnkr5BBxg
⚠ The extraction code is not public.
To obtain access, please contact the dataset authors at zw12416008@mail.dlut.edu.cn, providing:
Your name
Your institution/organization
Intended research purpose
Access will be granted for research and educational purposes only.


Citation
If you use this dataset, please cite our related work:
https://github.com/ZW12416008/USSD-Dataset

License
This dataset is released for research and educational purposes only. Redistribution for commercial use is not allowed without permission.
