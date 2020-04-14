# 中文金融情感词典

本 GitHub 仓库上传了一款`中文金融情感词典`，该词典来自`姜富伟、孟令超、唐国豪，2020，经济学（季刊），媒体文本情绪与股票回报预测`。读者可免费使用该词典，但请引用下列文献：
-  [Fuwei Jiang, Joshua Lee, Xiumin Martin, and Guofu Zhou.“Manager Sentiment and Stock Returns” Journal of Financial Economics 132(1), 2019,126-149]:https://www.sciencedirect.com/science/article/abs/pii/S0304405X18302770
- 姜富伟，孟令超，唐国豪.媒体文本情绪与股票回报预测.经济学(季刊),2020.

## 词典构建方法

构建中文金融情感词典的两大素材是英文金融词典（LM词典）以及现有的中文通用情感词典，我们将把英文LM金融词典转化为对应的中文版本（`洋为中用`），并从中文通用情感词典中筛选出在金融语境下仍然适用的情感词汇（`古为今用`），这两部分词语是中文金融情感词典的重要组成部分。为了避免金融情感词语的遗漏，我们利用`word2vec算法`（一种深度学习算法）从语料中找到与前两部分词语高度相关并且具有合适情感倾向的词语，从而实现扩充词典的目的。最后，将上述三种方法得到的词语合并去除，得到最终的中文金融情感词典。在古为今用部分，为了避免不同通用情感词典之间特征差异的影响，同时也为了保证词语的完备性，我们将三个应用程度较为广泛的词典（知网HowNet情感词典、清华大军李军词典以及台湾大学NTUSD词典） 合并去重，以此作为所使用的通用情感词典。

![中文金融情感词典构建方法](images/method.png)



## 词典信息

完整词典共9228个词语，其中消极词语共5890词，积极词语共3338词。


<table class="tg">
  <tr>
    <th class="tg-c3ow" colspan="3">消极词语部分 （5890）</th>
  </tr>
  <tr>
    <td class="tg-0pky">来源</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">词语数量</td>
  </tr>
  <tr>
    <td class="tg-0pky">LM词典中文翻译</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">1562</td>
  </tr>
  <tr>
    <td class="tg-0pky" rowspan="3">通用词典筛选</td>
    <td class="tg-0pky">Tsinghua词典</td>
    <td class="tg-0pky">1945</td>
  </tr>
  <tr>
    <td class="tg-0pky">知网词典</td>
    <td class="tg-0pky">534</td>
  </tr>
  <tr>
    <td class="tg-0pky">NTUSD词典</td>
    <td class="tg-0pky">1243</td>
  </tr>
  <tr>
    <td class="tg-0pky">Word2vec词典扩充</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">606</td>
  </tr>
  <tr>
    <th class="tg-c3ow" colspan="3">积极词语部分 （3338）</th>
  </tr>
  <tr>
    <td class="tg-0pky">来源</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">词语数量</td>
  </tr>
  <tr>
    <td class="tg-0pky">LM词典中文翻译</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">458</td>
  </tr>
  <tr>
    <td class="tg-0pky" rowspan="3">通用词典筛选</td>
    <td class="tg-0pky">Tsinghua词典</td>
    <td class="tg-0pky">1928</td>
  </tr>
  <tr>
    <td class="tg-0pky">知网词典</td>
    <td class="tg-0pky">304</td>
  </tr>
  <tr>
    <td class="tg-0pky">NTUSD词典</td>
    <td class="tg-0pky">255</td>
  </tr>
  <tr>
    <td class="tg-0pky">Word2vec词典扩充</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">393</td>
  </tr>
</table>





---------
更多细节请参见论文：`姜富伟、孟令超、唐国豪，2020，经济学（季刊），媒体文本情绪与股票回报预测`.读者可免费使用该词典，但请引用下列文献：
-  Fuwei Jiang, Joshua Lee, Xiumin Martin, and Guofu Zhou.“Manager Sentiment and Stock Returns” Journal of Financial Economics 132(1), 2019,126-149
- 姜富伟，孟令超，唐国豪.媒体文本情绪与股票回报预测.经济学(季刊),2020.

