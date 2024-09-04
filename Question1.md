```python
import numpy as np
import cProfile

A = np.array([[3.7827, 3.3454, 3.2341], [2.2122, 3.5678, 3.9087], [1.1234, 2.8934, 5.9087]])
B = np.array([[3.1234, 3.0987, 3.1234], [2.1111, 3.2222, 3.3333], [1.0987, 1.3456, 5.1234]])
C = np.array([[3.1243, 3.0989, 3.1256], [2.6721, 3.6785, 3.9017], [1.1254, 2.8956, 5.9187]])

def matrix_operations():
    result_add = A + B
    print("Matrix A + Matrix B:")
    print(result_add)

    result_sub = A - B
    print("\nMatrix A - Matrix B:")
    print(result_sub)

cProfile.run('matrix_operations()')
```

    Matrix A + Matrix B:
    [[ 6.9061  6.4441  6.3575]
     [ 4.3233  6.79    7.242 ]
     [ 2.2221  4.239  11.0321]]
    
    Matrix A - Matrix B:
    [[0.6593 0.2467 0.1107]
     [0.1011 0.3456 0.5754]
     [0.0247 1.5478 0.7853]]
             678 function calls (653 primitive calls) in 0.001 seconds
    
       Ordered by: standard name
    
       ncalls  tottime  percall  cumtime  percall filename:lineno(function)
            1    0.000    0.000    0.001    0.001 2703322430.py:10(matrix_operations)
            1    0.000    0.000    0.001    0.001 <string>:1(<module>)
            4    0.000    0.000    0.000    0.000 _ufunc_config.py:132(geterr)
            4    0.000    0.000    0.000    0.000 _ufunc_config.py:33(seterr)
            2    0.000    0.000    0.000    0.000 _ufunc_config.py:426(__init__)
            2    0.000    0.000    0.000    0.000 _ufunc_config.py:430(__enter__)
            2    0.000    0.000    0.000    0.000 _ufunc_config.py:435(__exit__)
           18    0.000    0.000    0.000    0.000 arrayprint.py:1018(__call__)
            2    0.000    0.000    0.001    0.000 arrayprint.py:1595(_array_str_implementation)
            2    0.000    0.000    0.000    0.000 arrayprint.py:403(_get_formatdict)
            2    0.000    0.000    0.000    0.000 arrayprint.py:411(<lambda>)
            2    0.000    0.000    0.000    0.000 arrayprint.py:452(_get_format_function)
            2    0.000    0.000    0.001    0.000 arrayprint.py:506(wrapper)
            2    0.000    0.000    0.001    0.000 arrayprint.py:523(_array2string)
            2    0.000    0.000    0.001    0.000 arrayprint.py:561(array2string)
            2    0.000    0.000    0.000    0.000 arrayprint.py:64(_make_options_dict)
           18    0.000    0.000    0.000    0.000 arrayprint.py:739(_extendLine)
           18    0.000    0.000    0.000    0.000 arrayprint.py:753(_extendLine_pretty)
            2    0.000    0.000    0.000    0.000 arrayprint.py:780(_formatArray)
         26/2    0.000    0.000    0.000    0.000 arrayprint.py:789(recurser)
            2    0.000    0.000    0.000    0.000 arrayprint.py:898(_none_or_positive_arg)
            2    0.000    0.000    0.000    0.000 arrayprint.py:907(__init__)
            2    0.000    0.000    0.000    0.000 arrayprint.py:934(fillFormat)
           20    0.000    0.000    0.000    0.000 arrayprint.py:984(<genexpr>)
           20    0.000    0.000    0.000    0.000 arrayprint.py:989(<genexpr>)
           20    0.000    0.000    0.000    0.000 arrayprint.py:993(<genexpr>)
           20    0.000    0.000    0.000    0.000 arrayprint.py:994(<genexpr>)
            5    0.000    0.000    0.000    0.000 enum.py:1129(__new__)
           15    0.000    0.000    0.000    0.000 enum.py:1544(_get_value)
            5    0.000    0.000    0.000    0.000 enum.py:1551(__or__)
            5    0.000    0.000    0.000    0.000 enum.py:726(__call__)
            2    0.000    0.000    0.000    0.000 fromnumeric.py:2687(_max_dispatcher)
            2    0.000    0.000    0.000    0.000 fromnumeric.py:2692(max)
            2    0.000    0.000    0.000    0.000 fromnumeric.py:2831(_min_dispatcher)
            2    0.000    0.000    0.000    0.000 fromnumeric.py:2836(min)
            4    0.000    0.000    0.000    0.000 fromnumeric.py:71(_wrapreduction)
            1    0.000    0.000    0.000    0.000 iostream.py:137(_event_pipe)
            1    0.000    0.000    0.000    0.000 iostream.py:258(schedule)
            8    0.000    0.000    0.000    0.000 iostream.py:519(_is_master_process)
            8    0.000    0.000    0.000    0.000 iostream.py:546(_schedule_flush)
            8    0.000    0.000    0.000    0.000 iostream.py:624(write)
            7    0.000    0.000    0.000    0.000 socket.py:621(send)
            1    0.000    0.000    0.000    0.000 threading.py:1153(_wait_for_tstate_lock)
            1    0.000    0.000    0.000    0.000 threading.py:1220(is_alive)
            1    0.000    0.000    0.000    0.000 threading.py:601(is_set)
            2    0.000    0.000    0.000    0.000 {built-in method _thread.get_ident}
          2/1    0.000    0.000    0.001    0.001 {built-in method builtins.exec}
            2    0.000    0.000    0.000    0.000 {built-in method builtins.id}
           35    0.000    0.000    0.000    0.000 {built-in method builtins.isinstance}
            8    0.000    0.000    0.000    0.000 {built-in method builtins.issubclass}
          196    0.000    0.000    0.000    0.000 {built-in method builtins.len}
            2    0.000    0.000    0.000    0.000 {built-in method builtins.locals}
           10    0.000    0.000    0.000    0.000 {built-in method builtins.max}
            4    0.000    0.000    0.001    0.000 {built-in method builtins.print}
            8    0.000    0.000    0.000    0.000 {built-in method nt.getpid}
            2    0.000    0.000    0.000    0.000 {built-in method numpy.asarray}
           36    0.000    0.000    0.000    0.000 {built-in method numpy.core._multiarray_umath.dragon4_positional}
            8    0.000    0.000    0.000    0.000 {built-in method numpy.geterrobj}
            4    0.000    0.000    0.000    0.000 {built-in method numpy.seterrobj}
            8    0.000    0.000    0.000    0.000 {method '__exit__' of '_thread.RLock' objects}
            1    0.000    0.000    0.000    0.000 {method 'acquire' of '_thread.lock' objects}
            2    0.000    0.000    0.000    0.000 {method 'add' of 'set' objects}
            1    0.000    0.000    0.000    0.000 {method 'append' of 'collections.deque' objects}
            2    0.000    0.000    0.000    0.000 {method 'copy' of 'dict' objects}
            1    0.000    0.000    0.000    0.000 {method 'disable' of '_lsprof.Profiler' objects}
            2    0.000    0.000    0.000    0.000 {method 'discard' of 'set' objects}
            6    0.000    0.000    0.000    0.000 {method 'items' of 'dict' objects}
            4    0.000    0.000    0.000    0.000 {method 'reduce' of 'numpy.ufunc' objects}
            8    0.000    0.000    0.000    0.000 {method 'rstrip' of 'str' objects}
           18    0.000    0.000    0.000    0.000 {method 'split' of 'str' objects}
           18    0.000    0.000    0.000    0.000 {method 'splitlines' of 'str' objects}
            2    0.000    0.000    0.000    0.000 {method 'update' of 'dict' objects}
            8    0.000    0.000    0.000    0.000 {method 'write' of '_io.StringIO' objects}
    
    
    
