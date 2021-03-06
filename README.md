# NLP-Interview-Notes
专门为自然语言处理(NLP)面试准备的学习笔记与资料

## 一、招职位/投简历
1. 学校BBS

> 力推`北大未名`、`水木社区`,:这里面一般是学长或者学姐发布的内推职位，一般回复较快，但是你面对的竞争也很大（清北的学子们）

2. 招聘网站

> `BOSS直聘`、`实习僧`:有些岗位是重合的，信息较新，BOSS直聘回复较快

3. 互联网公司官网

> 一般春招和秋招的时候可以集中关注下
##  **二、实习篇**
## 蚂蚁金服-NLP内推面试
1. 简单自我介绍
2. 详细讲解下自己做过的一个项目（最熟悉的）
3. 解释下泛化，处理方法
4. bagging和boosting的原理以及区别
> 二者都是集成学习算法，都是将多个弱学习器组合成强学习器的方法。

> Bagging：从原始数据集中每一轮有放回地抽取训练集，训练得到k个弱学习器，将这k个弱学习器以投票的方式得到最终的分类结果。

> Boosting：每一轮根据上一轮的分类结果动态调整每个样本在分类器中的权重，训练得到k个弱分类器，他们都有各自的权重，通过加权组合的方式得到最终的分类结果。

5. 深度学习的过拟合欠拟合和解决方法
6. epoch和batch的原理
7. 调整learning rate的依据
8. xgboost和lightgbm的联系与区别
9. 孪生网络的原理
10. LDA的原理
11. CRF
12. 命名实体识别的原理BILSTM-CRF
13. 结巴词性标注的原理
14. 深度学习流行或者普及的原因
15. 在样本数据很少的情况下（不是样本不均衡），应该怎么做
16. 你有什么想问的？想了解的
17. L1和L2正则化
18. Dropout
> 防止过拟合。每次训练，都对每个神经网络单元，按一定概率临时丢弃。
19. 激活函数的比较
> 从晚7:30-8:30，面试官问了一个小时的问题，自己凭记忆想出上面的，都是一些基础的问题，不是刻意刁难。基础不牢，地动山摇，好好准备吧。

## 微软 DKI小组
> 刚开始一个开放型编程题，二选一；第一题是给定了数据集，然后要求做二分类，评价指标AUC；第二题是自我介绍+前端或者后端二选一，一天内完成，我选择了第一题，auc达到0.8269。

1. xgboost分类节点的依据

>如何计算每次分裂的收益呢？假设当前节点记为C,分裂之后左孩子节点记为L，右孩子节点记为R，则该分裂获得的收益定义为当前节点的目标函数值减去左右两个孩子节点的目标函数值之和：`Gain=ObjC-ObjL-ObjR`，具体地，根据目标函数值公式可得：
![](https://upload-images.jianshu.io/upload_images/1371984-d0a9c89dbbc34f7c.PNG?imageMogr2/auto-orient/strip%7CimageView2/2/w/544/format/webp)

2. 信息增益vs信息增益比
3. HMM原理
4. LDA原理
5. LSTM网络结构图
6. 二叉树层次遍历
7. 青蛙上楼梯
8. 快速排序
9. 项目（中间考虑项目是否存在缺陷，比较细节，这一块很重要）
10. 余弦距离、曼哈顿距离公式
11. SQL取第50条到第100条数据
12. pandas取最后三列的方法
13. TextRank原理

## 微软小冰NLP组面试
1. 反转单词
2. 最长公共子串
3. 二叉树层次遍历变型
4. 手写KNN
5. 列举神经网络以及用处和场景；RNN自动翻译，怎么处理输入与输出长度不同的情况
6. 还有一个矩阵题（太长了，四五行，题意读不懂）
7. AI自动写作系统设计写出思路，没有代码

## 联想面试
1. CNN的3大优点

>CNN的三个优点：sparse interaction(稀疏的交互)，parameter sharing(参数共享)，equivalent respresentation(等价表示)。适合于自动问答系统中的答案选择模型的训练。
2. RNN、LSTM、DNN、CNN比较
3. LR的损失函数
4. 常见激活函数的比较
5. SVM 支持向量到直线的距离公式
6. 常见核函数有哪些
7. 剪枝策略
## 联想研究员自然语言处理实习生
面试小组是做联想智能问答的，然后主要题目如下：
1. 数据预处理方法
2. TensorFlow实现基本运算
3. sgd原理、是否收敛
4. cnn卷积作用、参数共享怎么回事
> 所谓的权值共享就是说，用一个卷积核去卷积一张图，这张图每个位置是被同样数值的卷积核操作的，权重是一样的，也就是参数共享。

5. 池化和池化作用
> 减小图像尺寸即数据降维，缓解过拟合，保持一定程度的旋转和平移不变性。
6. batchsize选择的依据
> 较大Batch Size：1、 提高了内存的利用率，大矩阵乘法的并行化效率提高；2、 运行一次epoch所需要的迭代次数减少，相同数据量的数据处理速度加快；3、 Batch_Size越大下降方向越准，引起的训练震荡越小。但是每次迭代耗时更长。

> 较小Batch Size：Batch_Size不宜选的太小，太小了容易修正方向导致不收敛，或者需要经过很大的epoch才能收敛；
7. attention机制

> 深度学习中的注意力机制从本质上讲和人类的选择性视觉注意力机制类似，核心目标是从大量信息中有选择地筛选出少量重要信息并聚焦到这些重要信息上，忽略大多不重要的信息。目前在神经机器翻译(Neural Machine Translation)、图像理解(Image caption)等场景都有广泛应用。

8. word2vec

9. knn、贝叶斯、svm，kmeans、pca

10. 编程题统计100w词频

11. 1亿个数排序，查找

12. 开放性题目：如何实现问题检索

13. 编辑距离

14. python2.7和python3的区别

15. 梯度爆炸和梯度消失出现的原因以及解决方法

> 针对梯度爆炸问题，解决方案是引入Gradient Clipping(梯度裁剪)。通过Gradient Clipping，将梯度约束在一个范围内，这样不会使得梯度过大。


> 梯度消失：在反向传播算法计算每一层的误差项的时候，需要乘以本层激活函数的导数值，如果导数值接近于0，则多次乘积之后误差项会趋向于0，而参数的梯度值通过误差项计算，这会导致参数的梯度值接近于0，无法用梯度下降法来有效的更新参数的值。改进激活函数，选用更不容易饱和的函数，如ReLU函数。

    
## 百度在线笔试

1. 数字0-9，每个数字的使用次数大于等于0，输入数A的位数，数B的位数，求A和B乘积的最小值
```

# cnts=[1,3,0,0,0,0,0,0,0,1]

# A=2;B=2


# cnts=[2,3,0,0,0,0,0,0,0,1]
cnts=[2,3,0,0,0,0,0,0,0,1]
A=1;B=1
def findMinFac(cnts,A,B):
    nums=[0,1,2,3,4,5,6,7,8,9]
    num_cnt=dict(zip(nums,cnts))
    if A<=B:
        A,B=B,A
    aval=0
    for num in num_cnt:
        while num_cnt[num]>0 and A>0:
            aval=aval+10**(A-1)*num
            num_cnt[num]-=1
            A-=1
            # print("A:",A,"aval",aval)    

    bval=0
    for num in num_cnt:
        while num_cnt[num]>0 and B>0:
            bval=bval+10**(B-1)*num
            num_cnt[num]-=1
            B-=1
            # print("B:",B,"aval",bval)
    return aval*bval
print(findMinFac(cnts,A,B))

```
## 香侬科技 NLP算法实习生
1. 如果模型在训练结果表现很好，在测试集表现很差的原因有哪些
    > 比如在测试集的准确率为90%，在测试集的准确率为10%
2. Dropout(p)的理解，随着p的增加，模型的性能会是怎样的表现
3. 假如随着p的增加，模型的性能一直在下降，还有哪些原因
4. 给定一个实数列表nums和一个数key，寻找在nums离key最近的n个数
5. 动态规划：给定一个词典dictionary，实现分词：
    > 词语长度最大;最少分词次数

## 神州泰岳
- 连续子数组乘积最大
- 连续子数组求和最大
- 连续最长的无重复子串
- Dropout
- Attention，Self Attention
- seq2seq如何解决不等长问题
    >通过一些标志填充
- 未登录如何解决：增量学习，word2vec重新训练
- FastText的sub-word
- CNN
- RNN,LSTM的结构

## 猿辅导
- 简历项目
- 算法题
    > https://leetcode.com/problems/add-two-numbers/

## 阿里巴巴-本地生活
- Doc2Vec与word2vec的区别
- 如何使用别人的pretrained embedding进行fine-tuning
- word2vec的原理 ，如何解决一词多义
- lstm，bilstm,cnn的比较
## 第四范式
- 逻辑回归的手推公式
- 分词实现
- 最长公共前缀
## 阿里巴巴-达摩院
## 中科院计算机研究所
## 字节跳动[他人]
 - 最深叶子节点的最小子树，
 - top K ，
 - 栈中元素的最小值，
 - 最长回文子串。

## 商汤科技
- RNN,LSTM,GRU的区别
- 手写LSTM公式
- 解释Transformer
- 找出给定数组的第k大数
- 水仙花数最短长度

## 创新工场 医疗LAB-自然语言处理实习生
- xgb，gbdt，区别与联系，优缺点
- glove与word2vec的区别，glove的训练样本
- crf与hmm的优化算法和公式
- dropout的原理以及在前向和反向传播的操作，概率的是否为参数还是超参数
- cnn池化层的原理，是否解决过拟合，步数strid怎么设置，反向怎么计算
- 快速排序算法，时间复杂度，以及在数组相对有序的情况下哪个排序最优
- 最长斐波那契数列
- transformer，gpt，bert，elmo，attention家族(血虐)
- lstm与crf结合起来的有点以及单独的缺点
- l1与l2正则化以及求解公式，区别
- 权重初始化的方法有哪些，优缺点
- 超参数优化的方案有哪些

## 360 nlp算法实习生面试
- 问简历，讲下dssm，esim等原理
- 自己作死写了熟悉spark，然后让我手写ip地址统计的map-reduce

## 铁科院电子所-算法实习生
- 聊待遇：很诱惑
- 算法题1：斐波那契数列
- 算法题2：铁路区间空余车票求解
https://exservice.12306.cn/prepub/oj/status?myself=0&page=1


## 腾讯-CSIG算法实习生
- 算法题：六选四+C++手写
- 简历项目

## 深度好奇
- RNN，LSTM对比，LSTM为什么可以解决提取消失
- CNN文本分类
- TensorFlow手写逻辑回归

## 粉笔网-NLP算法实习生
- 介绍CRF的原理，Bilstm最后一层到crf的过程解释
- 介绍CNN，RNN，LSTM，手写LSTM公式
- Word2Vec的原理，层级的Softmax，霍夫曼树原理
- BiLSTM如何实现序列标注
- XGBoost，LigbhtGBM，GBDT区别
- 算法题：字典序排序；无序数组找第大K个数；最长分词实现
    
    说实话这三道题太经典了，在面试过程中出镜率很高


##  **三、秋招篇**
## VIVO 自然语言处理工程师
## 阿里大文娱-UC部门-自然语言处理工程师
- 一面
    > 从简历抽出一个项目介绍，里面的一些细节，是否有不足之处，怎么改善，了解目前业界的解决方案吗；一些NN模型的原理介绍；由于一面答的还可以，面试官没有为难，一道算法题：递归快速排序
- 二面
    > 主要聊简历，和一面差不多，一个小时，算法题找出一个字符串的最长单词，复杂度O(n)，不能使用split或者直接排序，主要考察了边界情况；之后也聊了下工作地点的青睐什么的
- 三面
    > 还是聊简历上的项目，因为这一面是交叉面，所以思考的角度可能不一样，主要侧重为什么这样做
- 四面
    > 本来以为三面面试凉了，但是还是抱着一丝希望：因为三面面完是12点了，所以想着可能还有电话面。该来的还是来了，5天后电话面，这一面还是比较细节的，这个和我春招实习投递的蚂蚁金服一样，问的比较仔细，解释方法加原理。
    深度学习，效果不好时应该怎么做，这个当时主要从欠拟合和过拟合解释的；xgboost与gbdt的区别；bilstm-crf实现序列标注，中间的输入，输出，crf概率怎么转移；针对网易实习项目展开询问，方案是什么，效果怎么样，怎么提升，
    需要注意那里，预测为概率的缺点是什么，怎么生成负样本，是否有更好的方式。
## 陌陌-自然语言处理工程师
一面，问了下滴滴的项目，然后原理，还有搜狐畅游的dssm；问了下attention加上bert，transformer，两道算法题，第一道编辑距离，第二道递归；

二面，问的导师那边的项目，比如ner，cnn文本分类，crf，em算法，维特比算法，bilstm，二面问的比较细，主要考察你是不是对网络结构理解，cnn一维二维的区别，问了两道算法题，第一道相邻单词，第二道最长数字字串

## 拼多多在线笔试
```python
# 1
# import sys
# if __name__ == '__main__':
#
#     # a = [1, 3, 7, 4, 10]
#     # b = [2, 1, 5, 8, 9]
#     line = sys.stdin.readline().strip()
#     # 把每一行的数字分隔后转化成int列表
#     a = list(map(int, line.split()))
#
#     line = sys.stdin.readline().strip()
#     # 把每一行的数字分隔后转化成int列表
#     b = list(map(int, line.split()))
#
#     def find_b(s, e):
#         b.sort(reverse=True)
#         for num in b:
#             if num < e and num > s:
#                 return num
#
#     flag=False
#     for i in range(1, len(a)):
#         if a[i] < a[i - 1]:
#             if find_b(a[i-1],a[i+1]):
#                 a[i]=find_b(a[i-1],a[i+1])
#                 flag=True
#                 break
#     if flag:
#         print(" ".join([str(num) for num in a ]))
#     else:
#         print("NO")

# 2
# import sys
# if __name__ == '__main__':
#
#     line=sys.stdin.readline().strip()
#     # CAT TIGER RPC
#     flag=True
#     new_line=line.replace(' ','')
#     if len(new_line)==len(set(new_line)):
#         flag=False
#     else:
#         words=line.split()
#         if not set.intersection(set(words[0]),set(words[-1])):
#             flag = False
#         else:
#             for i in range(1,len(words)):
#                 if not set.intersection(set(words[i]),set(words[i-1])):
#                     flag = False
#                     break
#     if flag:
#         print("true")
#     else:
#         print("false")


# 4

import sys
if __name__ == '__main__':

    line=sys.stdin.readline().strip()
    N=int(line)

    line = sys.stdin.readline().strip()
    Li= list(map(int, line.split()))

    line = sys.stdin.readline().strip()
    Wi= list(map(int, line.split()))

    lw=dict(zip(Wi,Li))
    Li.sort(reverse=True)
    Wi.sort(key=lambda x:lw[x],reverse=True)
    height=1
    for i,wi in enumerate(Wi):
        print(i)
        cur_sum=0
        cur_height = 0
        for j in Wi[i+1:]:
            if cur_sum<=sum(7*[Wi[i]]):
                cur_sum+=Wi[j]
                cur_height+=1
        height=max(cur_height,height)
    print(height)
```

## 英语流利说在线笔试
- 函数求导
- 贝叶斯条件概率
- 生成式模型，判别式模型
- 堆排序
- 二进制，十六进制转换
- 排序算法稳定性
- SGD算法的缺点，学习率
- 方差和偏差
- 召回率计算
- 算法题：二叉排序树（二叉搜索树）的构建，插入，层次遍历
- 简单题：召回率计算

## 映客直播[他人]
- XGB是如何并行的。如何快速分裂的。
- adma的设计思想是什么。
- 如何加速收敛
- L1正则化和L2正则化的选择
- word2vec窗口大小的选择
- 两个数只出现一次，其他出现两次，找到这两个数

## 其他公司面试
1. 堆排序和快速排序
2. 贝叶斯原理和推理过程
3. 青蛙上楼梯 动态规划
4. 最短路径问题
5. RNN的前向和后向传播
6. 三层全连接网络的模拟过程
7. [基于矩阵分解的推荐算法](https://www.jianshu.com/p/812234c0da87)
8. [最大似然估计与贝叶斯估计的区别](https://www.jianshu.com/p/ead99acd6437)
9. 如何在embedding层之前实现两个句子向量交互


## 算法刷题
1. 《剑指Offer》
2. Leetcode
3. 牛客网

## 面试技巧
1. 掌握一门基础语言（c++或者java），尤其大厂很注重这一点
2. 发散性思维
## 相关资料
- [机器学习算法岗面试与提问总结](https://zhuanlan.zhihu.com/p/58434325?utm_source=wechat_session&utm_medium=social&s_r=0#showWechatShareTip)
- [精选Python面试100题](https://mp.weixin.qq.com/s/uPvzonBTGYLqF7PO3hZ8cg)
- [知识点 | 关于机器学习的超全总结](http://wemedia.ifeng.com/86075044/wemedia.shtml)
- [生成模型学习笔记：从高斯判别分析到朴素贝叶斯](https://www.jiqizhixin.com/articles/2018-12-24-13?from=synced&keyword=%E6%9D%A1%E4%BB%B6%E6%A6%82%E7%8E%87%E5%88%86%E5%B8%83)
- [专栏 | Bi-LSTM+CRF在文本序列标注中的应用](https://mp.weixin.qq.com/s?__biz=MzA3MzI4MjgzMw==&mid=2650735630&idx=4&sn=726c61346d436edb69963dd88cc35a41)
- [机器学习与深度学习常见面试题（上）](https://mp.weixin.qq.com/s/e8rlmjNp9solM3ZJXsioaA)