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
    


    ---------------------------------------------------------------------------

    FileNotFoundError                         Traceback (most recent call last)

    Cell In[3], line 8
          6 df=pd.DataFrame(data)
          7 print(df)
    ----> 8 df_csv=pd.read_csv("students.csv")
          9 print(df_csv)
         10 print()
    

    File ~\miniconda3\envs\py312\Lib\site-packages\pandas\io\parsers\readers.py:1026, in read_csv(filepath_or_buffer, sep, delimiter, header, names, index_col, usecols, dtype, engine, converters, true_values, false_values, skipinitialspace, skiprows, skipfooter, nrows, na_values, keep_default_na, na_filter, verbose, skip_blank_lines, parse_dates, infer_datetime_format, keep_date_col, date_parser, date_format, dayfirst, cache_dates, iterator, chunksize, compression, thousands, decimal, lineterminator, quotechar, quoting, doublequote, escapechar, comment, encoding, encoding_errors, dialect, on_bad_lines, delim_whitespace, low_memory, memory_map, float_precision, storage_options, dtype_backend)
       1013 kwds_defaults = _refine_defaults_read(
       1014     dialect,
       1015     delimiter,
       (...)   1022     dtype_backend=dtype_backend,
       1023 )
       1024 kwds.update(kwds_defaults)
    -> 1026 return _read(filepath_or_buffer, kwds)
    

    File ~\miniconda3\envs\py312\Lib\site-packages\pandas\io\parsers\readers.py:620, in _read(filepath_or_buffer, kwds)
        617 _validate_names(kwds.get("names", None))
        619 # Create the parser.
    --> 620 parser = TextFileReader(filepath_or_buffer, **kwds)
        622 if chunksize or iterator:
        623     return parser
    

    File ~\miniconda3\envs\py312\Lib\site-packages\pandas\io\parsers\readers.py:1620, in TextFileReader.__init__(self, f, engine, **kwds)
       1617     self.options["has_index_names"] = kwds["has_index_names"]
       1619 self.handles: IOHandles | None = None
    -> 1620 self._engine = self._make_engine(f, self.engine)
    

    File ~\miniconda3\envs\py312\Lib\site-packages\pandas\io\parsers\readers.py:1880, in TextFileReader._make_engine(self, f, engine)
       1878     if "b" not in mode:
       1879         mode += "b"
    -> 1880 self.handles = get_handle(
       1881     f,
       1882     mode,
       1883     encoding=self.options.get("encoding", None),
       1884     compression=self.options.get("compression", None),
       1885     memory_map=self.options.get("memory_map", False),
       1886     is_text=is_text,
       1887     errors=self.options.get("encoding_errors", "strict"),
       1888     storage_options=self.options.get("storage_options", None),
       1889 )
       1890 assert self.handles is not None
       1891 f = self.handles.handle
    

    File ~\miniconda3\envs\py312\Lib\site-packages\pandas\io\common.py:873, in get_handle(path_or_buf, mode, encoding, compression, memory_map, is_text, errors, storage_options)
        868 elif isinstance(handle, str):
        869     # Check whether the filename is to be opened in binary mode.
        870     # Binary mode does not support 'encoding' and 'newline'.
        871     if ioargs.encoding and "b" not in ioargs.mode:
        872         # Encoding
    --> 873         handle = open(
        874             handle,
        875             ioargs.mode,
        876             encoding=ioargs.encoding,
        877             errors=errors,
        878             newline="",
        879         )
        880     else:
        881         # Binary mode
        882         handle = open(handle, ioargs.mode)
    

    FileNotFoundError: [Errno 2] No such file or directory: 'students.csv'



```python

```


---
**Score: 0**