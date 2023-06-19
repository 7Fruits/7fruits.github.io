---
published: false
---


RANK(), ROW_NUMBER() and DENSE_RANK() are three useful functions in SQL query for ranking purpose.

RANK () returns the rank of each row within the partition of a result set. The rank of a row is one plus the number of ranks that come before the row in question. RANK provides the same numeric value for ties For example: 1,2,2,4, 5. The numbers in ranking are not consecutive, there is gap if there are ties.

ROW_NUMBER and RANK are similar. ROW_NUMBER numbers all rows sequentially (for example 1, 2, 3, 4, 5). 
DENSE_RANK() returns the rank of each row within a result set partition, with no gaps in the ranking values. The rank of a specific row is one plus the number of distinct rank values that come before that specific row.

By running the T-SQL script in SQL server as below, I got the results that 2 and 4 were skipped due to the ties with RANK(); ROW_NUMBER() gave the consecutive numbers for each row within the result set partition. DENSE_RANK() gave out the rank without gap.


    SELECT 
            [Latest Recorded Population]
            ,[City Key]
            ,RANK() OVER( PARTITION BY [Latest Recorded Population] ORDER BY [City Key]) AS rk
            ,ROW_NUMBER() OVER(PARTITION BY [Latest Recorded Population]  ORDER BY [City Key]) AS rowNo
            ,DENSE_RANK() OVER (PARTITION BY [Latest Recorded Population]  ORDER BY [City Key]) AS dRk
    FROM [Kineteco].[dbo].[Cities]

![]({{site.baseurl}}/images/rk_rn_drk.png)