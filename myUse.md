## 我的使用

```
# 创建激活环境
conda create -n UNetEG python=3.5
conda activate UNetEG

conda remove -n UNetEG --all
conda clean -y -all
conda info --e

# 修改conda源，修改pip源，升级pip
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
conda config --set show_channel_urls yes

python -m pip install --upgrade pip
pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple


# 安装pytorch
# cuda80最多只能使用1.0.0 conda install pytorch==1.0.0 torchvision==0.2.1 cuda80 -c pytorch
conda install pytorch torchvision cpuonly -c pytorch # cpuonly：只有cpu
conda install pytorch cuda80 torchvision -c pytorch # 无法安装正确版本

# jupyter notebook 安装
conda install jupyter
conda install jupyterlab
pip3 install -r requirements.txt

# No module named 'win32api'
pip install pypiwin32
```

- dataset

https://drive.google.com/open?id=1RzPB1_bqzQhlWvU-YGvZzhx2omcDh38C

- visdom

[模块visdom安装与使用](https://blog.csdn.net/tanmx219/article/details/87800752)