# readme
<h2> InspirationOnly

<h4> The official code for "InspirationOnly: synthesizing expiratory CT from inspiratory CT to estimate parametric response map"

## Environment

pip install -r requirements.txt

## Usage

Main directories and files are listed below:

```
.
├── INR.pth # 模型的权重
├── INR.py  # 模型
├── testA   # 测试数据
├── testB   # 呼气相生成保存路径
│ 
├── data  # 数据读取
│   ├── aligned_dataset.py
│   ├── ...
│   └── base_dataset.py
├── options  # 参数设置
│   ├── base_options.py
│   ├── train_options.py
│   └── test_options.py
├── excel.py # 根据肺叶计算每个肺叶的PRM（'emphysema','fSAD','None','Normal'）,保存为excle文件
└── test.py  # 呼气相生成代码
```
# Example command to run the script

直接使用test即可预测。
如果新数据输入的时候，请将肺区提取出来并将肺区之外的CT值置为-1024。



