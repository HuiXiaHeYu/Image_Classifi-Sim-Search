### 功能： 图像分类、以图搜图

**优点**：支持CPU和GPU两种训练方式，自定义cuda0/1

以图搜图原理：特征向量相似度计算

特征度量：
1. 余弦相似度损失训练
   1. faiss度量【余弦相似度检索、大规模数据集】
2. KDTree度量（metric使用cosine度量不准确）【欧氏距离做检索】

部署相关：
1. 设置端口和防火墙
2. 因为python是以文件夹的形式作为模块的，所以创建python环境变量(可以将src下文件夹作为模块导入)
   - `export PYTHONPATH=/home/xxx/image_classifi/src`
3. 创建`main.py` -> `nohup python main.py > log.log 2>&1 &`
   - 查看日志：`cat log.log`

可改进方面：
 - 样本数、类别数过少
 - 页面美化
