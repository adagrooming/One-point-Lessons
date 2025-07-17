# **One-point-Lessons**

Within SNH, P&G, or outside.

Any topic that could help personally or work wise.

Proposed next owners - flexible if you have something to share, swap/advance

# Spis treści
- [Resolving Data Issues in Power BI with DROP TABLE] (#Resolving Data Issues in Power BI with DROP TABLE)



- ✅  28. Dominika,

- ✅  29. Jarek,

-  ☐ 30. Malgorzata,

-  ☐ 31. Matheus,

-  ☐ 32. Zarina,

-  ☐ 33. Zhozef

---------------------------------------------------------------------------------------
## *Resolving Data Issues in Power BI with DROP TABLE*
 

Key Takeaways:

When discrepancies arise between Databricks and Power BI, particularly with unexpected empty values in columns, consider the following:

1. Data Type Mismatches:

o Ensure that data types in Databricks align with those in Power BI to avoid incorrect data interpretations (e.g., strings interpreted as numbers).

2. Data Loading and Transformation Issues:

o Be aware that filters and aggregations in Power BI may inadvertently remove or hide data.

o Perform a full refresh to clear Power BI’s cache and ensure it reflects the most current data.

3. Indexing and Performance Considerations:

o Overwriting a table (e.g., using CREATE OR REPLACE) may not fully update all data, especially in large datasets.

o Using DROP TABLE clears all associated metadata and indices, providing a clean state for data loading.

4. Limitations of CREATE OR REPLACE:

o If there are active connections, CREATE OR REPLACE may not fully replace the table. DROP TABLE guarantees complete removal.

Why DROP TABLE is Effective:

· Complete Removal:

o DROP TABLE deletes the entire table, including all metadata and indices, allowing for fresh data loading without legacy issues.

· Elimination of Caching Problems:

o This method ensures that Power BI loads the most up-to-date data, free from any old cached entries.

Example Case:

1. Scenario:

o A table named Sales_Data in Databricks has all columns populated, yet the Total_Sales column shows empty values in Power BI.

2. Initial Attempt:

o Using CREATE OR REPLACE TABLE Sales_Data AS ... does not resolve the issue.

3. Solution:

o Execute DROP TABLE IF EXISTS Sales_Data; followed by recreating the table. This action clears previous metadata and cached data, resolving the issue.

*Conclusion:*

In cases of data integrity issues in Power BI—despite correct data in Databricks—utilizing DROP TABLE followed by the table's recreation is an effective strategy to eliminate problems related to metadata, data types, and caching.

--------------------------------------------------------------------------------------
