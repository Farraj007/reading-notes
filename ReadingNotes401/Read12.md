[Main Page](../README.md)

# Reading Notes 12

## Articles  

[Link to article](https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html)

## Pandas

- pandas is a Python package that provides fast, flexible, and expressive data structures designed to make working with "relational" or "labeled" data both easy and intuitive. It aims to be the fundamental high-level building block for doing practical, real world data analysis in Python. Additionally, it has the broader goal of becoming the most powerful and flexible open source data analysis / manipulation tool available in any language.

## Object creation

- Creating a Series by passing a list of values, letting pandas create a default integer index:

  `s = pd.Series([1, 3, 5, np.nan, 6, 8])`

  output :

  > 0 1.0
  > 1 3.0
  > 2 5.0
  > 3 NaN
  > 4 6.0
  > 5 8.0
  > dtype: float64

- Creating a DataFrame by passing a NumPy array, with a datetime index and labeled columns:

  `dates = pd.date_range('20130101', periods=6)`

  output:

  > DatetimeIndex(['2013-01-01', '2013-01-02', '2013-01-03', '2013-01-04',
  >
  > > '2013-01-05', '2013-01-06'],
  > > dtype='datetime64[ns]', freq='D')

- Creating a DataFrame by passing a dict of objects that can be converted to series-like.

  > df2 = pd.DataFrame({'A': 1.,
  > 'B': pd.Timestamp('20130102'),
  > 'C': pd.Series(1, index=list(range(4)), dtype='float32'),
  > 'D': np.array([3] \* 4, dtype='int32'),
  > 'E': pd.Categorical(["test", "train", "test", "train"]),
  > 'F': 'foo'})

- Viewing data

  > df.head()
  > A B C D
  > 2013-01-01 0.469112 -0.282863 -1.509059 -1.135632
  > 2013-01-02 1.212112 -0.173215 0.119209 -1.044236
  > 2013-01-03 -0.861849 -2.104569 -0.494929 1.071804
  > 2013-01-04 0.721555 -0.706771 -1.039575 0.271860
  > 2013-01-05 -0.424972 0.567020 0.276232 -1.087401

- To drop any rows that have missing data.

  `df1.dropna(how='any')`

- Filling missing data.

  `df1.fillna(value=5)`

## Operations and Stats

- Operations in general exclude missing data.

- Operating with objects that have different dimensionality and need alignment. In addition, pandas automatically broadcasts along the specified dimension.

  > s = pd.Series([1, 3, 5, np.nan, 6, 8], index=dates).shift(2)
  >
  > 2013-01-01 NaN
  > 2013-01-02 NaN
  > 2013-01-03 1.0
  > 2013-01-04 3.0
  > 2013-01-05 5.0
  > 2013-01-06 NaN
  > Freq: D, dtype: float6

- Apply
  Applying functions to the data:

- df.apply(np.cumsum)

  >            A         B        C      D  F
  >
  > 2013-01-01 0.000000 0.000000 -1.509059 5 NaN
  > 2013-01-02 1.212112 -0.173215 -1.389850 10 1.0
  > 2013-01-03 0.350263 -2.277784 -1.884779 15 3.0
  > 2013-01-04 1.071818 -2.984555 -2.924354 20 6.0
  > 2013-01-05 0.646846 -2.417535 -2.648122 25 10.0
  > 2013-01-06 -0.026844 -2.303886 -4.126549 30 15.0

## Grouping

- By “group by” we are referring to a process involving one or more of the following steps:

  - Splitting the data into groups based on some criteria
  - Applying a function to each group independently
  - Combining the results into a data structure
  - Grouping and then applying the sum() function to the resulting groups.

    > df.groupby('A').sum()
    >
    >            C         D
    >
    > A
    > bar 1.732707 1.073134
    > foo 2.824590 -0.574779

### Reshaping and Stack

- The stack() method “compresses” a level in the DataFrame’s columns.

  > stacked = df2.stack()
  >
  > stacked
  >
  > first second
  > bar one A -0.727965
  > B -0.589346
  > two A 0.339969
  > B -0.693205
  > baz one A -0.339355
  > B 0.593616
  > two A 0.884345
  > B 1.591431
  > dtype: float64

- With a “stacked” DataFrame or Series (having a MultiIndex as the index), the inverse operation of stack() is unstack(), which by default unstacks the last level:
  > stacked.unstack()
  > A B
  > first second
  > bar one -0.727965 -0.589346
  > two 0.339969 -0.693205
  > baz one -0.339355 0.593616
  > two 0.884345 1.591431

### Plotting

- We use the standard convention for referencing the matplotlib API

  > import matplotlib.pyplot as plt
  > plt.close('all')
  > ts = pd.Series(np.random.randn(1000),
  > index=pd.date_range('1/1/2000', periods=1000))

### HDF5

- Writing to a HDF5 Store.

`df.to_hdf('foo.h5', 'df')`

- Reading from a HDF5 Store.

  > pd.read_hdf('foo.h5', 'df')
  > A B C D
  >
  > 2000-01-01 0.350262 0.843315 1.798556 0.782234
  > 2000-01-02 -0.586873 0.034907 1.923792 -0.562651
  > 2000-01-03 -1.245477 -0.963406 2.269575 -1.612566
  > 2000-01-04 -0.252830 -0.498066 3.176886 -1.275581
  > 2000-01-05 -1.044057 0.118042 2.768571 0.386039
  > ... ... ... ... ...
  > 2002-09-22 -48.017654 31.474551 69.146374 -47.541670
  > 2002-09-23 -47.207912 32.627390 68.505254 -48.828331
  > 2002-09-24 -48.907133 31.990402 67.310924 -49.391051
  > 2002-09-25 -50.146062 33.716770 67.717434 -49.037577
  > 2002-09-26 -49.724318 33.479952 68.108014 -48.822030
  > [1000 rows x 4 columns]