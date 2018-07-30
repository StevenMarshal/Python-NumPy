## 1.2 NumPy内置函数array

示例：

	import numpy as np
	
	# 创建numpy的array数据类型
	np_array = np.arange(9)
	print(np_array)
	# [0 1 2 3 4 5 6 7 8]
	
	# 半开区间大于等于2和小于9
	np_array = np.arange(2,9)
	print(np_array)
	# [2 3 4 5 6 7 8]
	
	# 进行整体加减乘除运算
	print(np_array - 1)
	# [1 2 3 4 5 6 7]
	print(np_array - 1 + 2)
	# [3 4 5 6 7 8 9]
	
	# 计算numpy的array长度
	np_array_len = len(np.arange(2,9))
	print(np_array_len)
	# 7
	
	# 通过step进行间隔取数
	np_array = np.arange(2, 9, 3)
	print(np_array)
	# [2 5 8]
	np_array = np.arange(0, 9, 3)
	print(np_array)
	# [0 3 6]
	np_array = np.arange(9, step = 3)
	print(np_array)
	# [0 3 6]