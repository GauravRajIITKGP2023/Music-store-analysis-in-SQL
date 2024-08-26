# SQL Database Analysis for Music Store

## Project Overview
This project focuses on analyzing a music store database to gain actionable insights on customer behavior, sales patterns, and artist performance. By utilizing SQL queries, the project addresses various business questions ranging from identifying top customers and genres to analyzing invoice data across different countries. The analysis was conducted using a relational database that includes tables for customers, invoices, tracks, albums, artists, genres, and employees.

## Tools & Technologies
- **SQL**: The primary tool used for data retrieval and analysis.
- **PostgreSQL**: The database management system used to store and query the data.
- **Data Modeling**: Utilized a relational schema, linking various entities such as Customer, Invoice, Track, Artist, and more to derive meaningful insights.

## Questions Asked

### Easy Level:
1. **Who is the senior-most employee based on job title?**
2. **Which countries have the most invoices?**
3. **What are the top 3 values of total invoices?**
4. **Which city has the best customers?** We would like to throw a promotional Music Festival in the city where we made the most money. Write a query that returns the city with the highest sum of invoice totals. Return both the city name & sum of all invoice totals.
5. **Who is the best customer?** The customer who has spent the most money will be declared the best customer. Write a query that returns the person who has spent the most money.

### Moderate Level:
1. **Write a query to return the email, first name, last name, & Genre of all Rock Music listeners.** Return your list ordered alphabetically by email starting with A.
2. **Let's invite the artists who have written the most rock music in our dataset.** Write a query that returns the Artist name and total track count of the top 10 rock bands.
3. **Return all the track names that have a song length longer than the average song length.** Return the Name and Milliseconds for each track. Order by the song length with the longest songs listed first.

### Advanced Level:
1. **Find how much amount was spent by each customer on artists?** Write a query to return customer name, artist name, and total spent.
2. **We want to find out the most popular music genre for each country.** We determine the most popular genre as the genre with the highest amount of purchases. Write a query that returns each country along with the top genre. For countries where the maximum number of purchases is shared, return all genres.
3. **Write a query that determines the customer that has spent the most on music for each country.** Write a query that returns the country along with the top customer and how much they spent. For countries where the top amount spent is shared, provide all customers who spent this amount.

## Insights from the Schema

### Employee and Customer Relations:
- The **Employee** table is linked to the **Customer** table through the `SupportRepId`, indicating that employees serve as support representatives for customers. This relationship could be analyzed to determine which employees manage the most customers or have the highest customer satisfaction ratings.

### Sales and Invoicing:
- The **Invoice** table, linked to both the **Customer** and **InvoiceLine** tables, is central to the sales process. The **Invoice** table records the total sales, while **InvoiceLine** details each item purchased, including the unit price and quantity. Analyzing these tables could reveal trends in sales, high-performing products, and the total revenue generated per customer or product.

### Music and Media:
- The **Track**, **Album**, **Artist**, **Genre**, and **MediaType** tables collectively form the music catalog. The **Track** table is the most detailed, linking to **Album**, **Genre**, and **MediaType**. This structure supports detailed analysis of track performance, genre popularity, and artist contributions, which could be used to identify top-selling genres or artists and the preferred media types.

### Playlists and User Preferences:
- The **Playlist** and **PlaylistTrack** tables track user-generated playlists, offering insights into user preferences and popular tracks. This data could be used to personalize recommendations or identify trends in user behavior.

### Productivity Insights:
- With the linkage between **Employee**, **Invoice**, and **Customer**, productivity metrics such as revenue per employee or customer satisfaction per support rep can be analyzed. Additionally, employee hierarchy and reporting lines can be observed from the `ReportsTo` column in the **Employee** table, which might be useful for organizational structure analysis.

## Key Insights

1. **Employee Hierarchy**: Identified the top-level employee in the organizational hierarchy, useful for understanding reporting structures and decision-making authority.
2. **Top Countries by Invoice Count**: Revealed the countries with the highest number of invoices, indicating regions with the most customer activity, guiding marketing and promotional efforts.
3. **Top Invoices**: Identified the highest invoice totals to understand significant transactions and explore what led to these high-value sales.
4. **Best City for a Promotional Event**: Identified the city with the highest sum of invoice totals, suggesting the most profitable location for hosting a promotional music festival.
5. **Best Customer**: Declared the customer who spent the most money as the best customer. This insight is useful for customer loyalty programs or personalized marketing.
6. **Rock Music Listeners**: Identified customers who are rock music listeners, providing a list ordered by email, useful for targeting specific customer segments.
7. **Top Rock Bands**: Identified the top 10 rock bands based on the number of tracks in the dataset, informing artist partnerships or promotions.
8. **Songs Longer Than Average**: Identified tracks longer than the average song length, useful for specialized playlists or exploring listener preferences.
9. **Customer Spending on Artists**: Conducted detailed analysis to determine how much each customer spent on specific artists, helping understand customer loyalty to certain artists.
10. **Popular Music Genres by Country**: Determined the most popular music genre for each country, guiding localized marketing strategies and inventory management.
11. **Top Customer by Country**: Identified the top-spending customer in each country, useful for targeted marketing campaigns and understanding high-value customers.

## Summary
The project effectively utilized SQL to explore and answer complex business questions, providing deep insights into customer behavior, sales performance, and artist popularity. By analyzing the data through a relational schema, the project uncovered valuable information that can inform strategic decisions in marketing, promotions, and customer engagement. Key findings include identifying the best customers, the most profitable locations, top-performing artists, and the most popular music genres across different countries.

## Conclusion
- **Optimized customer segmentation** by identifying the top-spending customers across countries, aiding in targeted marketing strategies.
- **Analyzed customer purchase data** to pinpoint the most popular music genres per country, essential for localizing promotional efforts.
- **Enhanced revenue generation** by discovering the top 10 rock bands with the most tracks, allowing for focused artist partnerships.
- **Determined the best city** for hosting a promotional event by analyzing city-level revenue data, driving a data-driven event strategy.
- **Uncovered key insights** into track length preferences, facilitating better playlist curation and user engagement.

