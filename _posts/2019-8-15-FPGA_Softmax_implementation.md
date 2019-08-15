---
layout:     post
title:      FPGA Softmax 
subtitle:   FPGA Softmax inplementation
date:       2019-08-15
author:     BY ckmufeng
header-img: img/post-bg-2015.jpg
catalog: true
tags:
    - FPGA
---

> FPGA Softmax Implementation

# FPGA Softmax Implementation

## 方案1-分段线性

首先使用 pwlf (https://github.com/cjekel/piecewise_linear_fit_py)包找到最优化的分段函数。



几个可以优化的思考点：

1、sub-max

2、定点化，结合浮点数fp32只有25bit有效精度一起考虑。

3、取对数法，可以不用考虑除法的实现，但需要设计FPGA实现ln。减小latency；

4、非分段的方法，如泰勒展开。

