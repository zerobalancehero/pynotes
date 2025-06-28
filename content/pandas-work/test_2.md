---
title: Test 2
date: 2025-06-28
author: Your Name
cell_count: 4
score: 0
---

```python
pip install pandas
```

    Collecting pandas
      Downloading pandas-2.3.0-cp312-cp312-win_amd64.whl.metadata (19 kB)
    Requirement already satisfied: numpy>=1.26.0 in c:\users\sanjay\miniconda3\envs\py312\lib\site-packages (from pandas) (2.3.1)
    Requirement already satisfied: python-dateutil>=2.8.2 in c:\users\sanjay\miniconda3\envs\py312\lib\site-packages (from pandas) (2.9.0.post0)
    Requirement already satisfied: pytz>=2020.1 in c:\users\sanjay\miniconda3\envs\py312\lib\site-packages (from pandas) (2025.2)
    Requirement already satisfied: tzdata>=2022.7 in c:\users\sanjay\miniconda3\envs\py312\lib\site-packages (from pandas) (2025.2)
    Requirement already satisfied: six>=1.5 in c:\users\sanjay\miniconda3\envs\py312\lib\site-packages (from python-dateutil>=2.8.2->pandas) (1.17.0)
    Downloading pandas-2.3.0-cp312-cp312-win_amd64.whl (11.0 MB)
       ---------------------------------------- 0.0/11.0 MB ? eta -:--:--
       ------ --------------------------------- 1.8/11.0 MB 12.6 MB/s eta 0:00:01
       ---------------- ----------------------- 4.5/11.0 MB 11.2 MB/s eta 0:00:01
       ------------------------ --------------- 6.8/11.0 MB 11.3 MB/s eta 0:00:01
       --------------------------------- ------ 9.2/11.0 MB 11.4 MB/s eta 0:00:01
       ---------------------------------------- 11.0/11.0 MB 11.2 MB/s eta 0:00:00
    Installing collected packages: pandas
    Successfully installed pandas-2.3.0
    Note: you may need to restart the kernel to use updated packages.
    


```python
print("testing pynotes 2")
```

    testing pynotes 2
    


```python
import pandas as pd
data={
    'Name':['sanjay','asha','ravi'],
    'score':[85,90,78]
}
df=pd.DataFrame(data)
print(df)
df_csv=pd.read_csv("students.csv")
print(df_csv)
print()
print(df_csv.head())
print()
print(df_csv.tail())
print()
print(df_csv["Score"])
print()
print(df_csv[["Name","Score"]] )
print()
print(df_csv[df_csv["Score"]>85])
print()
print(df_csv)
print()
df_csv["Passed"]=df_csv["Score"]>=80
print(df_csv)
print()
print(df_csv.groupby("Subject")["Score"].mean())

```

         Name  score
    0  sanjay     85
    1    asha     90
    2    ravi     78
         Name  Age  Subject  Score
    0  Sanjay   18     Math     85
    1    Asha   17  Science     90
    2    Ravi   18  English     78
    3   Meena   17     Math     92
    4   Kiran   19  Science     88
    
         Name  Age  Subject  Score
    0  Sanjay   18     Math     85
    1    Asha   17  Science     90
    2    Ravi   18  English     78
    3   Meena   17     Math     92
    4   Kiran   19  Science     88
    
         Name  Age  Subject  Score
    0  Sanjay   18     Math     85
    1    Asha   17  Science     90
    2    Ravi   18  English     78
    3   Meena   17     Math     92
    4   Kiran   19  Science     88
    
    0    85
    1    90
    2    78
    3    92
    4    88
    Name: Score, dtype: int64
    
         Name  Score
    0  Sanjay     85
    1    Asha     90
    2    Ravi     78
    3   Meena     92
    4   Kiran     88
    
        Name  Age  Subject  Score
    1   Asha   17  Science     90
    3  Meena   17     Math     92
    4  Kiran   19  Science     88
    
         Name  Age  Subject  Score
    0  Sanjay   18     Math     85
    1    Asha   17  Science     90
    2    Ravi   18  English     78
    3   Meena   17     Math     92
    4   Kiran   19  Science     88
    
         Name  Age  Subject  Score  Passed
    0  Sanjay   18     Math     85    True
    1    Asha   17  Science     90    True
    2    Ravi   18  English     78   False
    3   Meena   17     Math     92    True
    4   Kiran   19  Science     88    True
    
    Subject
    English    78.0
    Math       88.5
    Science    89.0
    Name: Score, dtype: float64
    


```python

```


---
**Score: 0**