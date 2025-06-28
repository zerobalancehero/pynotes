---
title: Test 1
date: 2025-06-28
author: Your Name
cell_count: 4
score: 0
---

```python
pip install matplotlib
```

    Requirement already satisfied: matplotlib in c:\users\sanjay\miniconda3\envs\py312\lib\site-packages (3.10.3)
    Requirement already satisfied: contourpy>=1.0.1 in c:\users\sanjay\miniconda3\envs\py312\lib\site-packages (from matplotlib) (1.3.2)
    Requirement already satisfied: cycler>=0.10 in c:\users\sanjay\miniconda3\envs\py312\lib\site-packages (from matplotlib) (0.12.1)
    Requirement already satisfied: fonttools>=4.22.0 in c:\users\sanjay\miniconda3\envs\py312\lib\site-packages (from matplotlib) (4.58.4)
    Requirement already satisfied: kiwisolver>=1.3.1 in c:\users\sanjay\miniconda3\envs\py312\lib\site-packages (from matplotlib) (1.4.8)
    Requirement already satisfied: numpy>=1.23 in c:\users\sanjay\miniconda3\envs\py312\lib\site-packages (from matplotlib) (2.3.1)
    Requirement already satisfied: packaging>=20.0 in c:\users\sanjay\miniconda3\envs\py312\lib\site-packages (from matplotlib) (25.0)
    Requirement already satisfied: pillow>=8 in c:\users\sanjay\miniconda3\envs\py312\lib\site-packages (from matplotlib) (11.2.1)
    Requirement already satisfied: pyparsing>=2.3.1 in c:\users\sanjay\miniconda3\envs\py312\lib\site-packages (from matplotlib) (3.2.3)
    Requirement already satisfied: python-dateutil>=2.7 in c:\users\sanjay\miniconda3\envs\py312\lib\site-packages (from matplotlib) (2.9.0.post0)
    Requirement already satisfied: six>=1.5 in c:\users\sanjay\miniconda3\envs\py312\lib\site-packages (from python-dateutil>=2.7->matplotlib) (1.17.0)
    Note: you may need to restart the kernel to use updated packages.
    


```python
print("hello for testing")
```

    hello for testing
    


```python
import matplotlib.pyplot as plt
def arr():
    n= list(x for x in map(int,input("enter the numbers seperated byt space: ").strip().split())if x>=0)
    if not n:
        print ("no input given")
    else:
        plt.plot(n,marker='o')
        plt.title("example table")
        plt.xlabel('x-axis')
        plt.ylabel('y-axis')
        plt.grid()
        plt.show()


arr()
```

    enter the numbers seperated byt space:  1 2 3 -6 -3 6 0
    


    
![png](/pynotes/images/test_1_2_1.png)
    



```python

```


---
**Score: 0**