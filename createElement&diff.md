# quantumVdom
- 在支持qasm在线语法编辑触发线路图的渲染后，由于复杂的向前对齐逻辑。我采用了暴力的所有内容重新渲染的形式。但是基于此的性能非常之差，且结构不清晰。因而希望以虚拟树的形式进行渲染
##
- 参考内容snabbdom
  - 实现h
  - 实现createElement
  - 实现patch
  - 实现diff
## 线路图的ast diff实现
- 原本snabbdom中的实现diff主要依靠tag和key
- 比较不在同一层级。往往需要用前后一层去和新插入的对比。
