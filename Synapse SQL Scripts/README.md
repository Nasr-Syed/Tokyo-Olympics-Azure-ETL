## Azure Synapse SQL Scripts:

Following Azure Synapse SQL commands were run on the transformed data ingested onto Azure Data Lake, and resultant .csv files display results from queries.

~~~~sql
-- Retrieving results from transformed dataframe in Databricks.
SELECT * FROM 
sport_popularity

-- Retrieving results from transformed dataframe in Databricks.
SELECT rank,TeamCountry,Total,percentage_medals_won 
FROM medal_percentage

-- Calculate Total Medals from each Country
SELECT country, COUNT(*) AS Total_Athletes FROM athletes
GROUP BY Country
ORDER BY Total_Athletes DESC

--Calculating Total Medals Won by each Country
SELECT TeamCountry,
    SUM(Gold) AS Total_Gold,
    SUM(Silver) AS Total_Silver,
    SUM(Bronze) AS Total_Bronze
FROM Medals
GROUP BY TeamCountry
ORDER BY Total_Gold DESC

~~~~