```python
from pyspark.sql import SparkSession

spark = (
    SparkSession.builder.remote("sc://192.168.0.13:15002")
    .appName("hello_spark")
    .getOrCreate()
)
```


```python
df = spark.read.csv(
    "hdfs://192.168.0.13:9000/employees_hadoop.csv",
    header=True,
    inferSchema=True,
)
```


```python
df.show()
```


```python
from pyspark.sql.functions import max

df.select(max("hire_date")).show()

```


```python
df.filter((df.emp_no < 10020) & (df.gender == "M") & (df.first_name.startswith("G"))).show()
```
