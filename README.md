# readme
<h2> InspirationOnly

<h4> The official code for "InspirationOnly: synthesizing expiratory CT from inspiratory CT to estimate parametric response map"

## Environment

pip install -r requirements.txt

## Usage

Main directories and files are listed below:

```
.
├── checkpoints  # 模型的权重
├── models  # 模型
│   ├── base_model.py
│   ├── cycle_gan_model.py
│   └── networks.py
├── test_data  # 测试数据
│   ├── data # 吸气相数据
│   ├── result # 测试结果
│       ├── lobe # 肺叶分割结果
│       └── airway # 气道分割结果 
├── data  # 数据读取
│   ├── base_dataset.py
│   ├── image_folder.py
│   └── unaligned_dataset.py
├── runs  # Logs and checkpoints save root
├── options  # 参数设置
│   ├── base_options.py
│   └── test_options.py
├── excel.py #根据肺叶计算每个肺叶的PRM（'emphysema','fSAD','None','Normal'）,保存为excle文件
├── infer.py #PRM生成代码
├── nii2dcm.py 
├── PRM.py #计算PRM
└── test.py
```
# Example command to run the script

python infer.py -i 吸气相路径  -o 输出路径 -g 显卡（0，1，2，3...） -a 气道路径 -e 肺叶路径 

#运行后会自动在 -o后的路径下创建两个文件夹 , fake_exp存放合成呼气相nii，PRM存放PRM文件。



