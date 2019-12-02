# Helpful Python Snippets

The purpose of this document is to provide a place for me to document any helpful snippets of Python i've found. This will primarily be singular lines or small chunks of code. Larger items will have their own documents.

## Index

1. [Pandas - convert column with type string to datetime](#sec_1)

## Snippets

#### 1. Pandas - convert column with type string to datetime <a name="sec_1"></a>

Converts the column `Date_str` in the string format to `Date_dt` in the datetime format
```python
df['Date_dt'] = pd.to_datetime(df['Date_str'])
```
