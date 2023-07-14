## 环境配置

### 安装miniconda

<u>安装前，请先将本地已有的python卸载。</u>

客户端安装一路进行下去即可。

### conda配置

- 在开始菜单打开Anaconda Prompt（miniconda）

- 配置源

  ```shell
  conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
  ```

- 创建虚拟环境（下载依赖，需要等待较长时间）

  ```shell
  conda env create -n python_3.10 -f environment.yml
  ```

- 进入虚拟环境

  ```shell
  conda activate python_3.10
  ```
​		

## 运行脚本

- <u>将csv格式的文件放置于与脚本同级目录。</u>

- 进入特定目录

- 输入命令，执行脚本

  ```shell
  python rcd.py
  ```

## 附：命令说明

### 源配置

```
#添加清华的源
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
#查看是否添加成功
conda config --show-sources
#移除源
conda config --remove channels
```

### 虚拟环境配置

```
#查看所有虚拟环境
conda info --envs
#创建虚拟环境
conda create -n <环境名> python=3.10
conda env create -n <环境名> -f <配置文件名>
#进入虚拟环境
conda activate <环境名>
#退出虚拟环境
conda deactivate <环境名>
```

