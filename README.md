# use-of-HITRAN
图文简单介绍HITRAN数据库的使用
## HITRAN简介
[HITRAN](https://www.hitran.org/)（High-Resolution Transmission Molecular Absorption）数据库是一个广泛使用的光谱数据库，用于研究大气和大气边界层中分子吸收的光谱特性。该数据库包含了大量关于分子能级、谱线参数和吸收谱线的实验和理论数据。

HITRAN数据库的主要目的是提供研究人员用于模拟和解释大气和大气边界层中分子吸收的光谱数据。它包含了多种分子，如水蒸气、二氧化碳、一氧化碳、甲烷等在大气中的吸收光谱信息。这些数据对于气候变化、大气遥感、大气光学以及行星科学等领域的研究非常重要。

HITRAN数据库提供了各种各样的分子参数，包括能级能量、弛豫参数、电偶极跃迁矩阵元、线宽和吸收强度等。这些数据可用于模拟和预测分子在不同波长和温度条件下的吸收光谱。

HITRAN数据库的最新版本由美国国家标准与技术研究所（NIST）维护，并提供了用于访问和查询数据的软件工具和接口。研究人员可以使用这些工具来获取他们感兴趣的分子的光谱数据，并将其应用于自己的研究工作中。

总而言之，HITRAN数据库是一个集成了大气和大气边界层中分子吸收光谱数据的资源，为研究人员提供了重要的数据支持，特别是在与大气和光学相关的科学研究领域。
## 注册账号
在主界面点击Register按钮，填写必要信息即可，这里不再赘述。

## 谱线数据查询（以CO为例）
按照下面步骤操作，先点Data Access->Line-by-line菜单

![image](https://github.com/WendellD0514/use-of-HITRAN/assets/91401712/a08c275e-9a11-4cb8-ae49-69cd6020388e)

然后进来可以看到很多分子的数据，这里勾选我们想要的

![image](https://github.com/WendellD0514/use-of-HITRAN/assets/91401712/c3ccc4a5-3a86-4f4b-8ebe-440f8c72c779)

进入同位素选择后，正常来说我们只关注最大Abundance（丰度：在自然界中的比例）分子，可以将其他的勾选取消

![image](https://github.com/WendellD0514/use-of-HITRAN/assets/91401712/7be7e69c-6406-4203-9e31-ccfd0ae2e1cc)

进入到波数选择后，根据文献，选择了4300.7$cm^{-1}$附近的一条独立谱线，于是把$\nu_{min},\nu_{max}$分别设置为4295$cm^{-1}$和4305$cm^{-1}$。
这里简单介绍下波数就是波长的倒数，具体如何换算只要关注下波长和波数的单位即可，在波长单位是$nm$，波数单位是$cm^{-1}$时，他们数值的乘积是$10^7$。

![image](https://github.com/WendellD0514/use-of-HITRAN/assets/91401712/84f3ac39-8b14-4722-abc0-e5c119db774f)

进入output options后，可以看到如下界面

![image](https://github.com/WendellD0514/use-of-HITRAN/assets/91401712/a61df100-9cb3-4538-8f73-22316529cebd)

我们这里最好弄一个自己的输出格式，进入输出格式设置界面后，这里是我自己常用的配置

![image](https://github.com/WendellD0514/use-of-HITRAN/assets/91401712/508895a2-6ab3-4649-9ed4-adc6916b7cae)

设置好格式后，进入下一步就行

![image](https://github.com/WendellD0514/use-of-HITRAN/assets/91401712/cc940fa6-48eb-4ccf-93ad-5a26ba6c0aee)

可以看到下图就是我们的搜索结果，可以看到这里第二个小圆点就是我们想找的谱线

![image](https://github.com/WendellD0514/use-of-HITRAN/assets/91401712/1df9bc1e-afc3-4e30-98b0-e1fee1bffd7f)

这里有一个.out的文件，这就是我们要的数据，但是里面的数据可能不太清楚都是些什么，这里需要下载最后一个readme文件，里面有.out文件里每一列对应数据的含义

这是.out文件

![image](https://github.com/WendellD0514/use-of-HITRAN/assets/91401712/4e97c897-e36a-4d80-b0df-9ea51382f6cf)

这是readme文件

![image](https://github.com/WendellD0514/use-of-HITRAN/assets/91401712/3f828b03-0316-4ace-8833-80e4777fa6b6)

之后有了.out文件后就能够进行后续的相关计算或编程了


















