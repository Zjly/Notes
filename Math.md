### 假设检验

#### 错误

##### 第一类错误

$P\{拒绝H_0|H_0为真\}=\alpha$

##### 第二类错误

$P\{接受H_0|H_0为假\}=\alpha$

#### 单个正态总体

##### ${\sigma^2}$已知，$\mu$的假设检验

$H_0:\mu=\mu_0;H_1:\mu\neq\mu_0$

$U=\frac{\overline{X}-\mu_0}{\sigma/\sqrt{n}} \sim N(0,1)$

##### ${\sigma^2}$未知，$\mu$的假设检验

$H_0:\mu=\mu_0;H_1:\mu\neq\mu_0$

$T=\frac{\overline{X}-\mu_0}{S/\sqrt{n}} \sim t(n-1)$

##### $\mu$未知，${\sigma^2}$的假设检验

$H_0:{\sigma^2}={\sigma_0}^2;H_1:{\sigma^2}\neq{\sigma_0}^2$

$\chi^2=\frac{(n-1)S^2}{{\sigma_0}^2} \sim \chi^2(n-1)$

##### $\mu$已知，${\sigma^2}$的假设检验

$H_0:{\sigma^2}={\sigma_0}^2;H_1:{\sigma^2}\neq{\sigma_0}^2$

$\chi^2=\frac {\sum\limits_{i=1}^{n}(X_i-\mu)^2} {{\sigma_0}^2} \sim \chi^2(n)$

#### 两个正态总体

##### ${\sigma_1},{\sigma_2}$已知，$\mu_1=\mu_2$的假设检验

$H_0:\mu_1=\mu_2;H_1:\mu_1\neq\mu_2$

$U=\frac {\overline{X}-\overline{Y}} {\sqrt{\frac{{\sigma_1}^2}{n_1}+\frac{{\sigma_2}^2}{n_2}}} \sim N(0,1)$

##### ${\sigma_1},{\sigma_2}$未知但相等，$\mu_1=\mu_2$的假设检验

$H_0:\mu_1=\mu_2;H_1:\mu_1\neq\mu_2$

$T=\frac{\overline{X}-\overline{Y}}{\sqrt{\frac{1}{n_1}+\frac{1}{n_2}}S_w}\sim t(n_1+n_2-2)$

${S_w}^2=\frac{(n_1-1){S_1}^2 + (n_2-1){S_2}^2}{n_1+n_2-2}$是$\sigma^2$的无偏估计

##### $\mu_1,\mu_2$未知，${\sigma_1}^2={\sigma_2}^2$的假设检验

$H_0:{\sigma_1}^2={\sigma_2}^2;H_1:{\sigma_1}^2\neq{\sigma_2}^2$

$F=\frac {{S_1}^2} {{S_2}^2} \sim F(n_1-1,n_2-1)$

##### $\mu_1,\mu_2$已知，${\sigma_1}^2={\sigma_2}^2$的假设检验

$H_0:{\sigma_1}^2={\sigma_2}^2;H_1:{\sigma_1}^2\neq{\sigma_2}^2$

$F=\frac {\sum\limits_{i=1}^{n_1}(X_i-\mu_1)^2/n_1} {{\sum\limits_{i=1}^{n_2}(Y_i-\mu_2)^2/n_2}^2} \sim F(n_1,n_2)$

#### 大样本非正态总体

##### 0-1分布

$H_0:p=p_0;H_1:p\neq p_0$

$U=\frac {\overline{X}-p_0} {\sqrt{p_0(1-p_0)/n}} \sim N(0,1)$

##### 总体均值

$H_0:\mu=\mu_0;H_1:\mu\neq\mu_0$

$T=\frac{\overline{X}-\mu_0}{S/\sqrt{n}} \sim N(0,1)$

##### 两个总体均值

$H_0:\mu_1-\mu_2=\delta;H_1:\mu_1-\mu2\neq\delta$

$U=\frac {\overline{X}-\overline{Y}-\delta} {\sqrt{\frac{{s_1}^2}{n_1}+\frac{{s_2}^2}{n_2}}} \sim N(0,1)$

#### 非参数假设检验

##### 不含未知参数

$\chi^2=\sum\limits_{i=1}^k\frac{(f_i-np_i)^2}{np_i}\sim\chi^2(k-1)$

##### 含有未知参数

$\chi^2=\sum\limits_{i=1}^k\frac{(f_i-n\hat p_i)^2}{n\hat p_i}\sim\chi^2(k-r-1)$

$r$为未知参数的个数
