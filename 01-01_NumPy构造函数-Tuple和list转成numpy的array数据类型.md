# 1 NumPy构造函数

## 1.1 Tuple和list转成numpy的array数据类型

Numpy的官方网站：  
www.numpy.org

示例：

	import numpy as np
	
	# 查看numpy版本
	print(np.__version__)
	# 1.15.0
	
	# list转化为numpy的array
	my_list = [12, 23.24, -19]
	my_np_array = np.array(my_list)
	print(my_np_array)
	# [ 12.    23.24 -19.  ]
	
	# 转换为numpy的array以后，后期运算会非常高效
	print(my_np_array * 100)
	# [ 1200.  2324. -1900.]
	
	# tumple转化为numpy的array
	my_tuple = (11, 2, 3, 6, 7)
	my_np_array = np.array(my_tuple)
	print(my_np_array)
	# [11  2  3  6  7]
	
	# tuple和numpy的array的不同
	print(my_tuple * 3)
	# (11, 2, 3, 6, 7, 11, 2, 3, 6, 7, 11, 2, 3, 6, 7)
	print(my_np_array * 3)
	# [33  6  9 18 21]


