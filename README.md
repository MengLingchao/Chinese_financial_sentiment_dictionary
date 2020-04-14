# 中文金融情感词典

本 GitHub 仓库上传了一款中文金融情感词典，该词典来自姜富伟、孟令超、唐国豪（2020）：媒体文本情绪与股票回报预测

## 词典构建方法

构建中文金融情感词典的两大素材是英文金融词典（LM词典）以及现有的中文通用情感词典，我们将把英文LM金融词典转化为对应的中文版本（洋为中用），并从中文通用情感词典中筛选出在金融语境下仍然适用的情感词汇（古为今用），这两部分词语是中文金融情感词典的重要组成部分。为了避免金融情感词语的遗漏，我们利用word2vec算法（一种深度学习算法）从语料中找到与前两部分词语高度相关并且具有合适情感倾向的词语，从而实现扩充词典的目的。最后，将上述三种方法得到的词语合并去除，得到最终的中文金融情感词典。在古为今用部分，为了避免不同通用情感词典之间特征差异的影响，同时也为了保证词语的完备性，我们将三个应用程度较为广泛的词典（知网HowNet情感词典、清华大军李军词典以及台湾大学NTUSD词典） 合并去重，以此作为所使用的通用情感词典。

