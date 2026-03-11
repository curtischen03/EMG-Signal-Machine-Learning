# EMG Signal Machine Learning
This is built upon the emg2qwerty work from Meta. The first section of this README provides some guidance for working with the repo and contains a running list of FAQs. **Note that the rest of the README is from the original repo and we encourage you to take a look at their work.**

# emg2qwerty
[ [`Paper`](https://arxiv.org/abs/2410.20081) ] [ [`Dataset`](https://fb-ctrl-oss.s3.amazonaws.com/emg2qwerty/emg2qwerty-data-2021-08.tar.gz) ] [ [`Blog`](https://ai.meta.com/blog/open-sourcing-surface-electromyography-datasets-neurips-2024/) ] [ [`BibTeX`](#citing-emg2qwerty) ]

A dataset of surface electromyography (sEMG) recordings while touch typing on a QWERTY keyboard with ground-truth, benchmarks and baselines.

<p align="center">
  <img src="https://github.com/user-attachments/assets/71a9f361-7685-4188-83c3-099a009b6b81" height="80%" width="80%" alt="alt="sEMG recording" >
</p>

## Setup

```shell
# Install [git-lfs](https://git-lfs.github.com/) (for pretrained checkpoints)
git lfs install

# Clone the repo, setup environment, and install local package
git clone git@github.com:joe-lin-tech/emg2qwerty.git ~/emg2qwerty 
cd ~/emg2qwerty
conda env create -f environment.yml
conda activate emg2qwerty
pip install -e .

# Download the dataset, extract, and symlink to ~/emg2qwerty/data
cd ~ && wget https://fb-ctrl-oss.s3.amazonaws.com/emg2qwerty/emg2qwerty-data-2021-08.tar.gz
tar -xvzf emg2qwerty-data-2021-08.tar.gz
ln -s ~/emg2qwerty-data-2021-08 ~/emg2qwerty/data
```

## Checkpoints Used In Project
Our progress and experimentation can be seen in the branches. Here is a link to the checkpoints used in the final result: https://drive.google.com/drive/folders/1MbhLU7Q1fT8wlk4Nxhs6tKNNkqIOQ--l
