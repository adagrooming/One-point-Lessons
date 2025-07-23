# **One-point-Lessons**

Within SNH, P&G, or outside.

Any topic that could help personally or work wise.

Proposed next owners - flexible if you have something to share, swap/advance

- ✅  28. Dominika,

- ✅  29. Jarek,

-  ☐ 30. Malgorzata,

-  ☐ 31. Matheus,

-  ☐ 32. Zarina,

-  ☐ 33. Zhozef

  

# Spis treści
- [Resolving Data Issues in Power BI with DROP TABLE](#resolving-data-issues-in-power-bi-with-drop-table)
- [Understanding the README and Adding Content to Our GitHub Repository](#understanding-the-readme-and-adding-content-to-our-github-repository)



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

## **Understanding the README and Adding Content to Our GitHub Repository**

### *What is a README File?*
   
The README file is the first thing users see in a GitHub repository.

It provides essential information about the project:
- Project Title: Name of the project.
- Description: Brief overview.
- Installation Instructions: Guide for setup.
- Usage: How to use the project.
- Contributing: Guidelines for contributions.
- License: Licensing information.
  
### *Viewing and Editing the README*

1. View: Go to the repository; the README displays on the main page.
2. Edit:
  - Click the README file, then the pencil icon (✏️).
  - Make your changes and scroll to "Commit changes."
  - Write a brief description and commit.

### *Adding Files to the Repository*

1. Navigate: Go to the repository’s main page.
2. Add File:
  - Click "Add file" and choose "Upload files" or "Create new file."
  - For uploads, drag files or select from your computer.
  - For new files, enter the file name and content.
3. Commit: Write a description and commit your changes.

### *Markdown Basics*

- Headings: Use # for titles, ## for subtitles.
- Bold: **text** or __text__
- Italic: *text* or _text_
- Lists:
  - Unordered: - Item or * Item
  - Ordered: 1. Item
- Links: [Link text](URL)
- Images: ![Alt text](image URL)

---------------------------------------------------------------------------------------------------------------------
