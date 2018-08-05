# 重温Java8的Stream操作

## 1.Java8中Stream的特性
- Not a data structure 非数据结构
- Designed for lambdas 为Lambdas表达式设计
- Do not support indexed access 不支持索引访问
- Can easily be outputted as arrays or lists 可以轻易输出数组或者列表
- Lazy access supported 支持延迟访问
- Parallelizable 并行处理

# 2.Stream的创建方式
- Using Stream.of(val1, val2, val3….)
- Using Stream.of(arrayOfElements)
- Using someList.stream()
- Using Stream.generate() or Stream.iterate() functions
- Using String chars or String tokens

# 3.转换流到集合的两种方式
- Convert Stream to List using stream.collect(Collectors.toList())
- Convert Stream to array using stream.toArray(EntryType[]::new)

# 4.核心流操作
## 4.1中间态操作
以下几种操作返回值依然是Stream对象，可以继续进行流式操作
- filter()
- map()
- sorted()

## 4.2终结态操作
以下几种操作返回值是该方法确定的返回类型，不会再返回Stream对象
- forEach()
- collect()
- match()
- count()
- reduce()

## 4.3短路操作
以下几种操作，只要满足predicate判断条件就会立即返回，不会继续往下执行
- anyMatch()
- findFirst()

# 5并行处理
如```list.parallelStream(); ```可以获取并行流对象，可以对集合里面的任务进行并行处理

# 6应用场景
- 对带有重复数据的集合去重
- 对日期、字符、数值等查找最大最小值