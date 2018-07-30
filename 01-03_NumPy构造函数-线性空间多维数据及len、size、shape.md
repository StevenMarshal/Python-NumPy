## 1.3 线性空间多维数据及len、size、shape

示例：

	import numpy as np
	
	# linspace
	
	my_linspace = np.linspace(5, 15, 8)
	print(my_linspace)
	# [ 5.          6.42857143  7.85714286  9.28571429 10.71428571 12.14285714  13.57142857 15.        ]
	my_linspace = np.linspace(5, 15, 9)
	print(my_linspace)
	# [ 5.    6.25  7.5   8.75 10.   11.25 12.5  13.75 15.  ]
	my_arange = np.arange(5, 15)
	print(my_arange)
	# [ 5  6  7  8  9 10 11 12 13 14]
	
	# 返回间隔值
	my_linspace = np.linspace(5, 15, 9, retstep=True)
	print(my_linspace)
	# (array([ 5.  ,  6.25,  7.5 ,  8.75, 10.  , 11.25, 12.5 , 13.75, 15.  ]), 1.25)
	
	my_linspace = np.linspace(5, 15, 8, retstep=True)
	print(my_linspace)
	# (array([ 5.        ,  6.42857143,  7.85714286,  9.28571429, 10.71428571,  12.14285714, 13.57142857, 15.        ]), 1.4285714285714286)
	print(my_linspace[0])
	# [ 5.          6.42857143  7.85714286  9.28571429 10.71428571 12.14285714  13.57142857 15.        ]
	print(my_linspace[1])
	# 1.4285714285714286
	
	# zeros()
	
	my_zeros = np.zeros(6)
	print(my_zeros)
	# [0. 0. 0. 0. 0. 0.]
	
	my_zeros = np.zeros((2, 3))
	print(my_zeros)
	# [[0. 0. 0.]
	#  [0. 0. 0.]]
	
	my_zeros = np.zeros((2, 3, 4))
	print(my_zeros)
	# [[[0. 0. 0. 0.]
	#   [0. 0. 0. 0.]
	#   [0. 0. 0. 0.]]
	#
	#  [[0. 0. 0. 0.]
	#   [0. 0. 0. 0.]
	#   [0. 0. 0. 0.]]]
	
	# ones()
	my_ones = np.ones(5)
	print(my_ones)
	# [1. 1. 1. 1. 1.]
	
	my_ones = np.ones((5, 3))
	print(my_ones)
	# [[1. 1. 1.]
	#  [1. 1. 1.]
	#  [1. 1. 1.]
	#  [1. 1. 1.]
	#  [1. 1. 1.]]
	
	# Numpy data types
	
	my_ones = np.ones(5, dtype='int32')
	print(my_ones)
	# [1 1 1 1 1]
	
	my_zeros = np.zeros(5, dtype='int32')
	print(my_zeros)
	# [0 0 0 0 0]
	
	my_ones = np.ones((5, 3), dtype='int64')
	print(my_ones)
	# [[1 1 1]
	#  [1 1 1]
	#  [1 1 1]
	#  [1 1 1]
	#  [1 1 1]]
	
	my_ones = np.ones((5, 3), dtype='int64')
	print(len(my_ones))
	# 5
	print(my_ones.size)
	# 15
	print(my_ones.shape)
	# (5, 3)

