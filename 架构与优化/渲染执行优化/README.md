# 渲染与执行优化

自Chrome 60以来，V8中的原始JavaScript解析速度提高了2倍。与此同时，原始解析（和编译）成本变得不那么明显/重要，因为Chrome中的其他优化工作将其并行化。

 V8通过对工作人员进行解析和编译，将主线程上的解析和编译工作量平均减少了40％（例如Facebook上为46％，Pinterest为62％），最高改进率为81％（YouTube） 线。 这是现有的离线主流线程解析/编译的补充。