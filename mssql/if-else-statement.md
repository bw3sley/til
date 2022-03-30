# IF - ELSE
The **IF...ELSE** statement is a control-flow statement that allows you to execute or skip a statement block based on a specified condition.

Eg:
```
    IF (@Number > 5)
    BEGIN
        PRINT 'All good!'
    END

    ELSE

    BEGIN
        PRINT 'Awfuck'
    END
```

In this syntax, if the ``Boolean_expression`` evaluates to **TRUE** then the ``statement_block`` in the **BEGIN...END** block is executed. Otherwise, the ``statement_block`` is skipped and the control of the program is passed to the statement after the **END** keyword.