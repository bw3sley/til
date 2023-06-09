# Convert
The **CONVERT()** function converts a value (of any type) into a specified datatype. It looks like the [CAST()](./cast.md) function.

Eg: 
```sql
    SELECT 
        CONVERT(varchar, Information.Date, 110)

    FROM Information
```

## Convert datetime to character

<center>

| With century | Input/Output | Standard |
| :----------: | :----------: | :------: |
| 100 | mon dd yyyy hh:miAM/PM | Default |
| 101 | mm/dd/yyyy | US |
| 102 | yyyy.mm.dd | ANSI | 
| 105 | dd-mm-yyyy | Italian/Brazilian | 
| 110 | mm-dd-yyyy | USA |

</center>

See more at: [w3schools](https://www.w3schools.com/sql/func_sqlserver_convert.asp).