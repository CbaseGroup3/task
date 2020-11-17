# task1
使用列表模拟表的列存储模型，示例数据为part.tbl，每一列存储为一个列表；模拟基于列存储模型的基本记录操作，统计 `P_SIZE<15` 并且`P_CONTAINER='WRAP BOX'`的P_RETAILPRICE累加和。 

**Tips**：使用一个bitmap列记录每行记录在第一个谓词操作`P_SIZE<15`上的结果，1为满足条件，0为不满足条件，然后按位图值访问下一个列，执行第二个谓词条件`P_CONTAINER='WRAP BOX'`的结果，最后按位图中1的位置访问P_RETAILPRICE列并求累加和。
