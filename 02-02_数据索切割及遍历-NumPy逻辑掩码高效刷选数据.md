## 2.2 NumPy逻辑掩码高效刷选数据

示例：

	import numpy as np
	
	# Boolean mask arrays
	my_vector = np.array([-12, -23, 0, 3, 4, 7, 100])
	print(my_vector)
	# [-12 -23   0   3   4   7 100]
	
	# 取得能够被3整除的
	zero_mod_3_mask = 0==(my_vector%3)
	print(zero_mod_3_mask)
	# [ True False  True  True False False False]
	
	print(my_vector[zero_mod_3_mask])
	# [-12   0   3]
	
	# 取得大于0的（这是Python的一种方式）
	print(my_vector[my_vector > 0])
	# [  3   4   7 100]
	
	# 大于0而且被3整除
	print(my_vector[(my_vector > 0) & zero_mod_3_mask])
	# [3]
	
	postive_test = my_vector > 0
	print(postive_test)
	print(zero_mod_3_mask)
	# [False False False  True  True  True  True]
	# [ True False  True  True False False False]
	
	combined_mask = np.logical_and(zero_mod_3_mask, postive_test)
	print(combined_mask)
	# [False False False  True False False False]
	
	print(my_vector[combined_mask])
	# [3]
	
	my_vector = np.arange(-4, 8)
	print(my_vector)
	# [-4 -3 -2 -1  0  1  2  3  4  5  6  7]
	
	print(my_vector.size)
	# 12
	
	my_vector.shape = (3, 4)
	print(my_vector)
	# [[-4 -3 -2 -1]
	#  [ 0  1  2  3]
	#  [ 4  5  6  7]]
	
	print(my_vector[(my_vector > 0) & (my_vector % 2 == 0)])
	# [2 4 6]
