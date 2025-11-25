
<!-- omit in toc -->
## Overview
- [Corruption Types](#corruption-types)
- [Benchmark Results](#benchmark-results)
- [Metrics](#metrics)
- [Dataset Download](#dataset-download)
- [Dataset Compilation](#dataset-compilation)
- [Dataset Usage](#dataset-usage)
- [TODOs](#todos)
- [Acknowledgments](#acknowledgments)


## Corruption Types

### Missing Camera
| Severity Level 1                                       | Severity Level 2                                       | Severity Level 3                                       |
|--------------------------------------------------------|--------------------------------------------------------|--------------------------------------------------------|
| Multi-View:                                            | Multi-View:                                            | Multi-View:                                            |
| ![Severity 1 Multi-View](assets/missingcamera_1_multi_view_camera_scene-0097_scene_animation.gif) | ![Severity 2 Multi-View](assets/missingcamera_2_multi_view_camera_scene-0097_scene_animation.gif) | ![Severity 3 Multi-View](assets/missingcamera_3_multi_view_camera_scene-0097_scene_animation.gif) |

### Motion Blur
| Severity Level 1 | Severity Level 2 | Severity Level 3 |
|-------------------|-------------------|-------------------|
| BEV:              | BEV:              | BEV:              |
| ![Severity 1 BEV](assets/motionblur_1_bev_scene-0097_scene_animation.gif) | ![Severity 2 BEV](assets/motionblur_2_bev_scene-0097_scene_animation.gif) | ![Severity 3 BEV](assets/motionblur_3_bev_scene-0097_scene_animation.gif) |
| Front:            | Front:            | Front:            |
| ![Severity 1 Front](assets/motionblur_1_front_camera_scene-0097_scene_animation.gif) | ![Severity 2 Front](assets/motionblur_2_front_camera_scene-0097_scene_animation.gif) | ![Severity 3 Front](assets/motionblur_3_front_camera_scene-0097_scene_animation.gif) |

### Points Reducing
| Severity Level 1 | Severity Level 2 | Severity Level 3 |
|-------------------|-------------------|-------------------|
| BEV:              | BEV:              | BEV:              |
| ![Severity 1 BEV](assets/pointsreducing_1_bev_scene-0097_scene_animation.gif) | ![Severity 2 BEV](assets/pointsreducing_2_bev_scene-0097_scene_animation.gif) | ![Severity 3 BEV](assets/pointsreducing_3_bev_scene-0097_scene_animation.gif) |
| Front:            | Front:            | Front:            |
| ![Severity 1 Front](assets/pointsreducing_1_front_camera_scene-0097_scene_animation.gif) | ![Severity 2 Front](assets/pointsreducing_2_front_camera_scene-0097_scene_animation.gif) | ![Severity 3 Front](assets/pointsreducing_3_front_camera_scene-0097_scene_animation.gif) |

### Snow
| Severity Level 1 | Severity Level 2 | Severity Level 3 |
|-------------------|-------------------|-------------------|
| BEV:              | BEV:              | BEV:              |
| ![Severity 1 BEV](assets/snow_1_bev_scene-0097_scene_animation.gif) | ![Severity 2 BEV](assets/snow_2_bev_scene-0097_scene_animation.gif) | ![Severity 3 BEV](assets/snow_3_bev_scene-0097_scene_animation.gif) |
| Front:            | Front:            | Front:            |
| ![Severity 1 Front](assets/snow_1_front_camera_scene-0097_scene_animation.gif) | ![Severity 2 Front](assets/snow_2_front_camera_scene-0097_scene_animation.gif) | ![Severity 3 Front](assets/snow_3_front_camera_scene-0097_scene_animation.gif) |

### Temporal Misalignment
| Severity Level 1 | Severity Level 2 | Severity Level 3 |
|-------------------|-------------------|-------------------|
| BEV:              | BEV:              | BEV:              |
| ![Severity 1 BEV](assets/temporalmisalignment_1_bev_scene-0097_scene_animation.gif) | ![Severity 2 BEV](assets/temporalmisalignment_2_bev_scene-0097_scene_animation.gif) | ![Severity 3 BEV](assets/temporalmisalignment_3_bev_scene-0097_scene_animation.gif) |
| Multi-View:       | Multi-View:       | Multi-View:       |
| ![Severity 1 Multi-View](assets/temporalmisalignment_1_multi_view_camera_scene-0097_scene_animation.gif) | ![Severity 2 Multi-View](assets/temporalmisalignment_2_multi_view_camera_scene-0097_scene_animation.gif) | ![Severity 3 Multi-View](assets/temporalmisalignment_3_multi_view_camera_scene-0097_scene_animation.gif) |

### Spatial Misalignment
| Severity Level 1 | Severity Level 2 | Severity Level 3 |
|-------------------|-------------------|-------------------|
| BEV:              | BEV:              | BEV:              |
| ![Severity 1 BEV](assets/spatialmisalignment_1_bev_scene-0097_scene_animation.gif) | ![Severity 2 BEV](assets/spatialmisalignment_2_bev_scene-0097_scene_animation.gif) | ![Severity 3 BEV](assets/spatialmisalignment_3_bev_scene-0097_scene_animation.gif) |
| Multi-View:       | Multi-View:       | Multi-View:       |
| ![Severity 1 Multi-View](assets/spatialmisalignment_1_multi_view_camera_scene-0097_scene_animation.gif) | ![Severity 2 Multi-View](assets/spatialmisalignment_2_multi_view_camera_scene-0097_scene_animation.gif) | ![Severity 3 Multi-View](assets/spatialmisalignment_3_multi_view_camera_scene-0097_scene_animation.gif) |

### Beams Reducing
| Severity Level 1 | Severity Level 2 | Severity Level 3 |
|-------------------|-------------------|-------------------|
| BEV:              | BEV:              | BEV:              |
| ![Severity 1 BEV](assets/beamsreducing_1_bev_scene-0097_scene_animation.gif) | ![Severity 2 BEV](assets/beamsreducing_2_bev_scene-0097_scene_animation.gif) | ![Severity 3 BEV](assets/beamsreducing_3_bev_scene-0097_scene_animation.gif) |
| Front:            | Front:            | Front:            |
| ![Severity 1 Front](assets/beamsreducing_1_front_camera_scene-0097_scene_animation.gif) | ![Severity 2 Front](assets/beamsreducing_2_front_camera_scene-0097_scene_animation.gif) | ![Severity 3 Front](assets/beamsreducing_3_front_camera_scene-0097_scene_animation.gif) |

### Brightness
| Severity Level 1 | Severity Level 2 | Severity Level 3 |
|-------------------|-------------------|-------------------|
| Multi-View:       | Multi-View:       | Multi-View:       |
| ![Severity 1 Multi-View](assets/brightness_1_multi_view_camera_scene-0097_scene_animation.gif) | ![Severity 2 Multi-View](assets/brightness_2_multi_view_camera_scene-0097_scene_animation.gif) | ![Severity 3 Multi-View](assets/brightness_3_multi_view_camera_scene-0097_scene_animation.gif) |

### Dark
| Severity Level 1 | Severity Level 2 | Severity Level 3 |
|-------------------|-------------------|-------------------|
| Multi-View:       | Multi-View:       | Multi-View:       |
| ![Severity 1 Multi-View](assets/dark_1_multi_view_camera_scene-0097_scene_animation.gif) | ![Severity 2 Multi-View](assets/dark_2_multi_view_camera_scene-0097_scene_animation.gif) | ![Severity 3 Multi-View](assets/dark_3_multi_view_camera_scene-0097_scene_animation.gif) |

### Fog
| Severity Level 1 | Severity Level 2 | Severity Level 3 |
|-------------------|-------------------|-------------------|
| BEV:              | BEV:              | BEV:              |
| ![Severity 1 BEV](assets/fog_1_bev_scene-0097_scene_animation.gif) | ![Severity 2 BEV](assets/fog_2_bev_scene-0097_scene_animation.gif) | ![Severity 3 BEV](assets/fog_3_bev_scene-0097_scene_animation.gif) |
| Multi-View:       | Multi-View:       | Multi-View:       |
| ![Severity 1 Multi-View](assets/fog_1_multi_view_camera_scene-0097_scene_animation.gif) | ![Severity 2 Multi-View](assets/fog_2_multi_view_camera_scene-0097_scene_animation.gif) | ![Severity 3 Multi-View](assets/fog_3_multi_view_camera_scene-0097_scene_animation.gif) |


*Note: Right click and click on `Open Image in new tab` to enlarge an animation*


## Benchmark Results
### 📊 Relative Resistance Ability (RRA) computed with NDS metric and baseline BEVfusion
| Model                                                           | Clean     | ⬆️ mRRA    | Beams Red.   | Brightness   | Darkness   | Fog       | Missing Cam.   | Motion Blur   | Points Red.   | Snow       | Spatial Mis.   | Temporal Mis.   |
|:----------------------------------------------------------------|:----------|:----------|:-------------|:-------------|:-----------|:----------|:---------------|:--------------|:--------------|:-----------|:---------------|:----------------|
| ⭐ [MEFormer](https://github.com/hanchaa/MEFormer)              | **0.739** | **7.391** | 16.759       | 0.878        | 1.556      | 8.586     | -0.168         | -0.307        | **8.865**     | **11.382** | 16.689         | **9.668**       |
| [CMT](https://github.com/junjie18/CMT)                          | 0.729     | 7.161     | **18.642**   | -1.138       | -0.096     | **9.398** | **2.041**      | -0.841        | 8.213         | 9.887      | **17.053**     | 8.448           |
| [MoME](https://github.com/konyul/MoME)                          | 0.735     | 6.837     | 15.061       | 0.400        | 0.694      | 7.891     | 1.634          | -0.685        | 8.421         | 10.852     | 14.975         | 9.128           |
| [MEFormer w/o PME](https://github.com/hanchaa/MEFormer)         | 0.737     | 6.740     | 15.172       | 0.714        | 1.522      | 8.176     | -0.791         | -0.679        | 8.384         | 10.749     | 14.968         | 9.184           |
| [Sparsefusion](https://github.com/yichen928/SparseFusion)       | 0.732     | 3.033     | 4.264        | **3.179**    | **1.821**  | 4.429     | 0.297          | 0.280         | 3.242         | 1.887      | 3.699          | 7.228           |
| [IS-Fusion](https://github.com/yinjunbo/IS-Fusion)              | 0.737     | 2.708     | 3.684        | 2.291        | 1.267      | 3.890     | 0.920          | **3.994**     | 1.691         | -2.351     | 4.513          | 7.177           |
| ⚓ [BEVfusion](https://github.com/mit-han-lab/bevfusion)         | 0.714     | 0.000     | 0.000        | 0.000        | 0.000      | 0.000     | 0.000          | 0.000         | 0.000         | 0.000      | 0.000          | 0.000           |
| [TransFusion](https://github.com/XuyangBai/TransFusion)         | 0.708     | -1.718    | -7.210       | 1.799        | 1.146      | -0.552    | 0.340          | -5.412        | -3.296        | -4.220     | -3.626         | 3.850           |
| [UniBEV_avg](https://github.com/tudelft-iv/UniBEV)              | 0.684     | -2.154    | 7.617        | -3.758       | -4.595     | -1.228    | -5.170         | -11.777       | -0.144        | -6.909     | 2.812          | 1.617           |
| [UniBEV_cat](https://github.com/tudelft-iv/UniBEV)              | 0.678     | -2.653    | 6.534        | -4.303       | -5.279     | -0.199    | -5.438         | -12.505       | -0.979        | -6.596     | 1.436          | 0.799           |
| [UniBEV_cnw](https://github.com/tudelft-iv/UniBEV)              | 0.685     | -2.893    | 5.030        | -3.729       | -4.383     | -1.104    | -5.749         | -13.119       | -0.428        | -8.055     | 1.582          | 1.025           |
| [DeepInteraction](https://github.com/fudan-zvg/DeepInteraction) | 0.691     | -7.221    | -6.361       | -3.150       | -7.215     | -25.037   | -16.386        | -7.077        | -2.188        | -5.149     | 0.212          | 0.145           |

### 📊 Resistance Ability (RA) computed with NDS metric
| Model                                                           | Clean     | ⬆️ mRA     | Beams Red.   | Brightness   | Darkness   | Fog       | Missing Cam.   | Motion Blur   | Points Red.   | Snow      | Spatial Mis.   | Temporal Mis.   |
|:----------------------------------------------------------------|:----------|:----------|:-------------|:-------------|:-----------|:----------|:---------------|:--------------|:--------------|:----------|:---------------|:----------------|
| ⭐ [CMT](https://github.com/junjie18/CMT)                       | 0.729     | **0.865** | **0.786**    | 0.937        | 0.948      | **0.806** | 0.974          | 0.841         | **0.925**     | 0.833     | **0.809**      | **0.788**       |
| [MEFormer](https://github.com/hanchaa/MEFormer)                 | **0.739** | 0.856     | 0.764        | 0.944        | 0.952      | 0.790     | 0.941          | 0.835         | 0.918         | **0.834** | 0.796          | 0.787           |
| [MoME](https://github.com/konyul/MoME)                          | 0.735     | 0.856     | 0.756        | 0.943        | 0.948      | 0.788     | 0.962          | 0.835         | 0.919         | 0.833     | 0.788          | 0.786           |
| [MEFormer w/o PME](https://github.com/hanchaa/MEFormer)         | 0.737     | 0.853     | 0.755        | 0.945        | 0.954      | 0.789     | 0.937          | 0.834         | 0.917         | 0.831     | 0.786          | 0.785           |
| [UniBEV_cat](https://github.com/tudelft-iv/UniBEV)              | 0.678     | 0.847     | 0.759        | 0.975        | 0.967      | 0.791     | 0.970          | 0.798         | 0.910         | 0.761     | 0.753          | 0.788           |
| [UniBEV_avg](https://github.com/tudelft-iv/UniBEV)              | 0.684     | 0.844     | 0.760        | 0.972        | 0.965      | 0.776     | 0.964          | 0.797         | 0.909         | 0.752     | 0.757          | 0.787           |
| [UniBEV_cnw](https://github.com/tudelft-iv/UniBEV)              | 0.685     | 0.837     | 0.740        | 0.971        | 0.966      | 0.775     | 0.957          | 0.784         | 0.905         | 0.742     | 0.747          | 0.781           |
| [Sparsefusion](https://github.com/yichen928/SparseFusion)       | 0.732     | 0.834     | 0.689        | 0.975        | 0.963      | 0.767     | 0.954          | 0.848         | 0.879         | 0.770     | 0.714          | 0.777           |
| [BEVfusion](https://github.com/mit-han-lab/bevfusion)           | 0.714     | 0.830     | 0.676        | 0.967        | 0.969      | 0.752     | 0.974          | 0.866         | 0.872         | 0.774     | 0.705          | 0.742           |
| [IS-Fusion](https://github.com/yinjunbo/IS-Fusion)              | 0.737     | 0.826     | 0.680        | 0.960        | 0.952      | 0.758     | 0.953          | **0.873**     | 0.860         | 0.733     | 0.715          | 0.771           |
| [TransFusion](https://github.com/XuyangBai/TransFusion)         | 0.708     | 0.824     | 0.633        | **0.993**    | **0.988**  | 0.754     | **0.985**      | 0.826         | 0.851         | 0.748     | 0.685          | 0.777           |
| [DeepInteraction](https://github.com/fudan-zvg/DeepInteraction) | 0.691     | 0.795     | 0.655        | 0.969        | 0.929      | 0.583     | 0.842          | 0.832         | 0.882         | 0.759     | 0.731          | 0.768           |

## Metrics
We adhere to the official nuScenes metric definition for computing the NDS and mAP metrics on the MultiCorrupt dataset. To quantitatively compare the performance between the corrupted dataset and the clean nuScenes datasets, we use a metric called the *Resistance Ability* (RA). This metric is calculated across the different severity levels with 

$$RA_{c,s} = \frac{M_{c,s}}{M_{clean}}, RA_c = \frac{1}{3} \sum_{s=1}^{3} RA_{c,s}$$

$$mRA = \frac{1}{N} \sum_{c=1}^{N} RA_c$$

where  $M_{c,s}$  represents metric for the $c$ types of corruption at the $s$-the severity level, $N$ is the total number of corruption types considered in our benchmark, and $M_{clean}$ is performance on the "clean" nuScenes dataset.

*Relative Resistance Ability* ( $RRA_{c}$ ) compares the relative robustness of each model for a specific type of corruption with a baseline model. If the value is greater than zero, it indicates that the model demonstrates superior robustness compared to the baseline model. If the value is less than zero, it suggests that the model is less robust than the baseline. We can summarize the relative resistance by computing *Mean Relative Resistance Ability* (mRRA), which measures the relative robustness of the candidate model compared to a baseline model for all types of corruptions

$$RRA_{c} = \frac{\sum\limits_{i=1}^{3} (M_{c, s})}{\sum\limits_{i=1}^{3} (M_{baseline, c, s})} - 1$$


$$mRRA = \frac{1}{N} \sum_{i=1}^{N} RRA_c$$

where $c$ denotes the type of corruption, $s$ represents the level of severity, and $N$ is the total number of corruption types considered in our benchmark. The term $RRA_{c}$ specifically illustrates the relative robustness of each model under a particular type of corruption $c$. The $mRRA$ reflects the global perspective by showing the average robustness of each model across all considered types of corruption with the baseline model.


## Dataset Download
Follow the Huggingface [Dataset Download](https://huggingface.co/docs/hub/datasets-downloading) instructions and download the dataset from the following link:
[https://huggingface.co/datasets/TillBeemelmanns/MultiCorrupt](https://huggingface.co/datasets/TillBeemelmanns/MultiCorrupt)

For example, you can run the following command to install the huggingface cli
```bash
pip install -U "huggingface_hub[cli]"
```

then download the whole dataset with
```bash
huggingface-cli download TillBeemelmanns/MultiCorrupt --repo-type dataset --local-dir /path/to/dataset
```

Please note the default cache location is `~/.cache/huggingface/datasets/downloads/`. This might cause problems if your local host does not have much free space in the `/home` directory. Change the cache location by setting the shell environment variable `HF_HOME` to another directory:

```bash
$ export HF_HOME="/path/to/another/directory/datasets"
```

Unzip the compressed dataset with the [unzip_compressed_dataset.sh](helper/unzip_compressed_dataset.sh) script.


## Dataset Compilation
You can also manually compile the whole dataset locally using the clean nuScenes dataset.

### Clone this repository:

```bash
git clone https://github.com/jeremynguyenn/FusionCorrupt3D-A-Robustness-Benchmark-for-Multi-Modal-Detection.git
cd multicorrupt
```

### Build the Docker image:

```bash
cd docker
docker build -t multicorrupt_create -f Dockerfile .
```

### Download Snowflakes
We use [LiDAR_snow_sim](https://github.com/SysCV/LiDAR_snow_sim) to simulate snow in LiDAR point clouds. To make the
snow simulation run we need to download the snowflakes:

```bash
cd converter
wget https://www.trace.ethz.ch/publications/2022/lidar_snow_simulation/snowflakes.zip
unzip snowflakes.zip
rm snowflakes.zip
```


## Dataset Usage

### Docker Container Setup
We recommend to use [run.sh](docker/run.sh) to start the
`multicorrupt_create_container` in order to generate MultiCorrupt.
Please modify the following pathes according to your local setup.

```
multicorrupt_data_dir="/work/multicorrupt"
nuscenes_data_dir="/work/nuscenes"
```
Please make sure that you have downloaded [nuScenes](https://www.nuscenes.org/)
 to `nuscenes_data_dir`.

After setting up the container, you could use VS Code to attach to the container 
or directly execute the following scripts.

### Image Corruption Generation

Run the following script to generate a corrupted image data:

```bash
usage: img_converter.py [-h] [-c N_CPUS] [-a {snow,fog,temporalmisalignment,brightness,dark,missingcamera,motionblur}] [-r ROOT_FOLDER]
                        [-d DST_FOLDER] [-f SEVERITY] [--seed SEED]

Generate corrupted nuScenes dataset for image data

options:
  -h, --help            show this help message and exit
  -c N_CPUS, --n_cpus N_CPUS
                        number of CPUs that should be used
  -a {snow,fog,temporalmisalignment,brightness,dark,missingcamera,motionblur}, --corruption {snow,fog,temporalmisalignment,brightness,dark,missingcamera,motionblur}
                        corruption type
  -r ROOT_FOLDER, --root_folder ROOT_FOLDER
                        root folder of dataset
  -d DST_FOLDER, --dst_folder DST_FOLDER
                        savefolder of dataset
  -f SEVERITY, --severity SEVERITY
                        severity level {1,2,3}
  --seed SEED           random seed
```

### Example

```bash
python converter/img_converter.py \
--corruption snow \
--root_folder /workspace/data/nuscenes \
--dst_folder /workspace/multicorrupt/snow/3 \
--severity 3 \
--n_cpus 24
```

### LiDAR Corruption Generation

Run the following script to generate a corrupted LiDAR data:

```bash
usage: lidar_converter.py [-h] [-c N_CPUS] [-a {pointsreducing,beamsreducing,snow,fog,copy,spatialmisalignment,temporalmisalignment,motionblur}] [-s SWEEP] [-r ROOT_FOLDER]
                          [-d DST_FOLDER] [-f SEVERITY] [--seed SEED]

Generate corrupted nuScenes dataset for LiDAR

options:
  -h, --help            show this help message and exit
  -c N_CPUS, --n_cpus N_CPUS
                        number of CPUs that should be used
  -a {pointsreducing,beamsreducing,snow,fog,copy,spatialmisalignment,temporalmisalignment,motionblur}, --corruption {pointsreducing,beamsreducing,snow,fog,copy,spatialmisalignment,temporalmisalignment,motionblur}
                        corruption type
  -s SWEEP, --sweep SWEEP
                        if apply for sweep LiDAR
  -r ROOT_FOLDER, --root_folder ROOT_FOLDER
                        root folder of dataset
  -d DST_FOLDER, --dst_folder DST_FOLDER
                        savefolder of dataset
  -f SEVERITY, --severity SEVERITY
                        severity level {1,2,3}
  --seed SEED           random seed
```

> [!IMPORTANT]
> For all experiments and results in the paper `--sweep` was activated, which means the LiDAR corruptions were applied to all LiDAR sweeps in the  dataset !

> [!WARNING]
> Depending on the number of available CPUs on your system, a lot of time is needed to generate some of the corruptions. Users report [12h of generation time](https://github.com/ika-rwth-aachen/MultiCorrupt/issues/12) for the LiDAR snow corruptions using 32 CPUs. Make sure to use all available CPUs on your compute cluster environment.


### Example

```bash
python3 converter/lidar_converter.py \
--corruption snow \
--root_folder /workspace/data/nuscenes \
--dst_folder /workspace/multicorrupt/snow/3/ \
--severity 3 \
--n_cpus 64 \
--sweep true
```

### MultiCorrupt Folder Structure
We recommend to create the following folder structure for MultiCorrupt using 
`lidar_converter.py` and `img_converter.py`:
```
-- multicorrupt
    |-- beamsreducing
    |   |-- 1
    |   |-- 2
    |   `-- 3
    |-- brightness
    |   |-- 1
    |   |-- 2
    |   `-- 3
    |-- dark
    |   |-- 1
    |   |-- 2
    |   `-- 3
    |-- fog
    |   |-- 1
    |   |-- 2
    |   `-- 3
    |-- missingcamera
    |   |-- 1
    |   |-- 2
    |   `-- 3
    .
    .
    .
```

### MultiCorrupt Evaluation
If you have created MultiCorrupt in the structure above, we recommend you to use
our simple [evaluation script](helper/multicorrupt_evaluation.sh) that iterates over
the whole dataset, executes the evaluation and extracts the NDS and mAP metrics.

In the script you would need to replace the pathes for `multicorrupt_root`,
`nuscenes_data_dir` and `logfile` according to your setup.
```bash
#!/bin/bash

# List of corruptions and severity levels
corruptions=("beamsreducing" "brightness" "dark" "fog" "missingcamera" "motionblur" "pointsreducing" "snow" "spatialmisalignment" "temporalmisalignment")
severity_levels=("1" "2" "3")

# Directory paths
multicorrupt_root="/workspace/multicorrupt/"
nuscenes_data_dir="/workspace/data/nuscenes"
logfile="/workspace/evaluation_log.txt"

.
.
.
```


## TODOs
- [ ] 📝 Add visualization for results

## Acknowledgments
We thank the authors of

- [mmdetection3d](https://github.com/open-mmlab/mmdetection3d)
- [LiDAR_fog_sim](https://github.com/MartinHahner/LiDAR_fog_sim)
- [LiDAR_snow_sim](https://github.com/SysCV/LiDAR_snow_sim)
- [lidar-camera-robust-benchmark](https://github.com/kcyu2014/lidar-camera-robust-benchmark)
- [RoboBEV](https://github.com/Daniel-xsy/RoboBEV)
- [Robo3D](https://github.com/ldkong1205/Robo3D)

for their open source contribution which made this project possible.


Please note that you should cite the original nuScenes dataset once you use MultiCorrupt.
