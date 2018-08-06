# 重温Java8新特性之文件操作和watchservie
## 文件操作
今天重温了一些文件操作：
- `Files.list()` 遍历文件和目录
- `Files.newDirectoryStream()` 遍历文件和目录
- `Files::isReularFile` 找出目录中的文件
- `file->file.isHidden()` 找出隐藏文件
- `Files.newBufferedWriter` 款速创建一个BufferedWriter，可以使编码语法更简洁
- `Files.write()` 使用简介的语法写入内容到文件
>**Tips：**
对于大目录,使用`DirectoryStream` 会性能更好

## WatchService
利用`WatchService` 对文件目录进行监视，可以对目录中增删改查这些动作进行监控