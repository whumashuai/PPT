# PPT
Generative Adversarial Network (GAN)
2gan基本框架
https://mp.weixin.qq.com/s__biz=MzU2NDQ3MTQ0MA==&mid=2247483814&idx=2&sn=ff24b1460aa168ba6c2e14473e419faa&chksm=fc4b3259cb3cbb4f
3goodfellow论文实验结果图
https://papers.nips.cc/paper/5423-generative-adversarial-nets.pdf
4公式
https://papers.nips.cc/paper/5423-generative-adversarial-nets.pdf
??_?? (z): a prior on input noise variables
G(z; θg): represent a mapping to data space,parameters θg. 
D(x): represents the probability that x came from the data rather than pg. We train D to maximize the probability of assigning the correct label to both training examples and samples from G. We simultaneously train G to minimize log(1 ? D(G(z))).
5-8 训练过程
https://blog.csdn.net/weixin_38145317/article/details/793/77017947

https://blog.csdn.net/GAN_player/article/details/77017947

https://zhuanlan.zhihu.com/p/39398823
设z为随机噪声，x为真实数据，生成式网络和判别式网络可以分别用G和D表示，其中D可以看作一个二分类器，那么采用交叉熵表示，可以写作:


其中第一项的logD(x)表示判别器对真实数据的判断，第二项log(1 ? D(G(z)))表示则对数据的合成与判断。通过这样一个极大极小(Max-min)博弈，循环交替地分别优化G和D来训练所需要的生成式网络与判别式网络，直到到达Nash均衡点。
