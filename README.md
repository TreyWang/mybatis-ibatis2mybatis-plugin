ibatis2mybatis
==============
### 基于https://github.com/mybatis/ibatis2mybatis  做部分修改

1.做生成规则修改，生成xml更完善；

2.针对mybatis使用selectKey做主键如果没有order属性默认会在insert语句执行完之后运行，引起报错，在ibatis xml中如果没有type属性时，默认添加order=“BEFORE”

3.ibatis中有部分jdbcType在mybatis中不存在，修改DATETIME转换之后为TIMESTAMP,修改LONGTEXT转换之后不增加jdbcType（可转换为LONGVARCHAR,请自行修改）;

主要修改文件：build.xml, migrate.xslt

### 运行

1.下载并安装ant；

2.将需要转换的ibatis xml文件放入source文件夹中；

3.命令行运行ant命令，转换的mybatis xml文件放在destination文件夹中

