# helloworld
my first github project

## first link
[baidu](http://www.baidu.com)

## second link
[mail](http://mail.163.com)

## 质量方程：

$\frac{\partial}{\partial t}(\alpha_g \rho_g) + \frac{1}{A} \frac{ \partial}{\partial t}(\alpha_g \rho_g v_g A) = \Gamma_g$

$\frac{\partial}{\partial t}(\alpha_f \rho_f) + \frac{1}{A} \frac{ \partial}{\partial t}(\alpha_f \rho_f v_f A) = \Gamma_f$

一般而言，流体中没有source或者sink，所以总体的连续性假设可得出液体产生的速率等于负的气体产生的速率，即

$\Gamma_f = -\Gamma_g$

界面质量输运模型假定总的质量输运可以分为主流流体中气液界面中的质量输运（$\Gamma_{ig}$）和壁面附近边界层内气液界面中的质量输运（$\Gamma_{w}$），即

$\Gamma_{g} = \Gamma_{ig} + \Gamma_{w}$

## 动量方程：

## 能量方程：
$\frac{\partial}{\partial t}(\alpha_g \rho_g U_g) + \frac{1}{A} \frac{ \partial}{\partial t}(\alpha_{g} \rho_g U_g v_g A) = -P\frac{\partial \alpha_g}{\partial t}-\frac{P}{A}\frac{\partial}{\partial x}(\alpha_g v_g A)+Q_{wg}+Q_{ig}+\Gamma_{ig}h_g^*+\Gamma_{w} h_g^{'}+DISS_g$

$\frac{\partial}{\partial t}(\alpha_{f} \rho_f U_f) + \frac{1}{A} \frac{ \partial}{\partial t}(\alpha_f \rho_f U_f v_f A) = -P\frac{\partial \alpha_f}{\partial t}-\frac{P}{A}\frac{\partial}{\partial x}(\alpha_f v_f A)+Q_{wf}+Q_{if}-\Gamma_{ig}h_f^*-\Gamma_{w} h_f^{'}+DISS_f$

在能量方程中，$Q_{wg}$和$Q_{wf}$是单位体积内的壁面传热速率，满足下式：

$Q=Q_{wg}+Q_{wf}$

其中$Q$是单位体积内壁面到流体的总传热速率。
与主流流体界面质量输运相关的相焓(phasic enthalpies, $h_g^*$, $h_f^*$)被定义为气液界面处的界面能跃迁条件。特别的，对于蒸发情况$h_g^*$和$h_f^*$分别为$h_g^s$和$h_f$，对于冷凝情况$h_g^*$和$h_f^*$分别为$h_g$和$h_f^s$。对于与壁面(热边界层)界面质量输运相关的相焓（phasic enthalpies, $h_g^{'}$, $h_f^{'}$）是类似的。这种选择的逻辑将会在质量输运（蒸汽产生，vapor generation）模型中进一步解释。

### 蒸汽产生
蒸汽产生（或冷凝）由两部分组成，即能量交换（$\Gamma_{ig}$）和壁面传热效应（$\Gamma_{w}$）。每一种蒸汽产生（或冷凝）过程都与界面质量输运效应有关。能量方程中的界面传热项（$Q_{ig}$和$Q_{if}$）包括了主流中和壁面附近热边界层处的界面能量交换导致的流体状态到界面状态的热交换。蒸汽产生（或冷凝）速率通过界面处能量平衡假设构建。
能量方程的和导出混合能量方程，界面能量输运的总和需为零，即

$Q_{ig}+Q_{if}+\Gamma_{ig}(h_g^*-h_f^*)+\Gamma_{w}(h_g^{'}-h_f^{'})=0$
