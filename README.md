# data_analysis

Some data analysis code about Pixiv.net daily ranking data.

Just so you know.

### 2018-9-12

#### Add two data files (csv -> 7z)

尝试从原json文件中加载数据发现，消耗内存过多，无法实现。

后尝试分批从json文件中将有用信息取出，按年份保存为csv文件。

最后将所有保存好的csv文件读入，pd.concat成一整个DataFrame，然后使用to_csv方法，保存为一整个csv文件。

至此，读入写出均不会占用过大内存，个人认为之前在解析json文件时，占用了太多内存，导入读入失败。（待验证）