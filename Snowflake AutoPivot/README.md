<h1 style="font-weight:normal">
  Snowflake AutoPivot SQL Script 
</h1>

I created this script to <b>remove the need to write Long PIVOT queries</b> in Snowflake. Using the AutoPivot Stored procedure can save valuable time by dynamiclly generating your pivot query as shown below.<br><br>

<h2>Normal Pivot Query</h2>
SELECT<br>
    *<br>
FROM TABLE<br><br>
PIVOT (SUM("Value") FOR "Sales/Profit" IN ('Profit','Sales'))<br><br>
AS P (Field 1, Field 2, Field 3, Field 4 , Field 5, Field 6, Field 7, Field 8,<b>… Field N</b>);
<br><br>

<h2>AutoPivot Query</h2>
CALL Auto_Pivot('TABLE','Sales/Profit','Value','SUM');<br><br>

Copy and paste the [AutoPivot SQL Script](https://github.com/RobsonEzra/SQL-Scripting/blob/6c1cd398bb67ac8d0d8d32ef76ee2aaed9d8ddd1/Snowflake%20AutoPivot/AutoPivot%20SQL%20Script) into your desired schema to use.
