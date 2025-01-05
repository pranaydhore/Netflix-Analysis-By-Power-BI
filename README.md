<body>
  <h1>Netflix Analysis Using Power BI</h1>

  <h2>1. Introduction</h2>
  <p>This project involves analyzing Netflix data using Power BI and DAX to gain insights into content distribution, genre trends, release patterns, and regional performance. The dataset includes movie and TV show details, such as titles, genres, release years, and countries of origin.</p>

  <h2>2. Dataset Overview</h2>
  <p>The dataset, <code>netflix.csv</code>, contains the following key columns:</p>
  <ul>
    <li><strong>Title:</strong> Name of the movie or TV show.</li>
    <li><strong>Type:</strong> Movie or TV show classification.</li>
    <li><strong>Genre:</strong> Genre or category of the content.</li>
    <li><strong>Release Year:</strong> Year when the content was released.</li>
    <li><strong>Country:</strong> Country where the content was produced.</li>
    <li><strong>Rating:</strong> Audience rating (e.g., PG, R, TV-MA).</li>
    <li><strong>Duration:</strong> Length of movies (in minutes) or number of seasons for TV shows.</li>
  </ul>

  <h2>3. Data Cleaning and Transformation</h2>
  <p>Power BI was used to clean and transform the data:</p>
  <ul>
    <li>Missing values were handled by replacing nulls with 'Unknown' or appropriate placeholders.</li>
    <li>Data types were standardized for consistency.</li>
    <li>New calculated columns were created using DAX for deeper insights (e.g., Year Buckets, Content Age).</li>
  </ul>

  <h2>4. Key Visualizations and Insights</h2>

  <h3>4.1 Content Distribution by Type</h3>
  <p>A bar chart revealed that Netflix has more movies than TV shows. This suggests a focus on shorter, standalone content rather than series.</p>

  <h3>4.2 Genre Analysis</h3>
  <p>A treemap displayed genre popularity, highlighting Drama and Comedy as the most dominant genres.</p>

  <h3>4.3 Release Trends Over Time</h3>
  <p>A line chart tracked content releases by year, showing rapid growth in recent years, indicating Netflix's expansion strategy.</p>

  <h3>4.4 Country-wise Distribution</h3>
  <p>A world map visualization depicted content origin, with the USA and India leading production.</p>

  <h3>4.5 Ratings Breakdown</h3>
  <p>A pie chart illustrated rating distribution, showing a family-friendly focus with TV-MA and PG-13 dominating.</p>

  <h2>5. Key DAX Measures Used</h2>
  <pre><code>
    Total Movies = COUNTROWS(FILTER('Netflix', 'Netflix'[Type] = "Movie"))
    Total TV Shows = COUNTROWS(FILTER('Netflix', 'Netflix'[Type] = "TV Show"))
    Movies Percentage = DIVIDE([Total Movies], COUNTROWS('Netflix'))
    TV Shows Percentage = DIVIDE([Total TV Shows], COUNTROWS('Netflix'))
    Avg Duration = AVERAGE('Netflix'[Duration])
  </code></pre>

  <h2>6. Conclusion</h2>
  <p>This analysis provides a comprehensive view of Netflix's content strategy and trends. Key findings include:</p>
  <ul>
    <li>Movies dominate Netflix's library, suggesting a preference for standalone content.</li>
    <li>Drama and Comedy are the most popular genres, aligning with global audience preferences.</li>
    <li>Content production has surged in recent years, reflecting Netflix's investment in growth.</li>
    <li>The USA and India are key production hubs, emphasizing their role in Netflix's global strategy.</li>
  </ul>
  <p>These insights can help stakeholders make data-driven decisions to optimize content strategy and audience engagement.</p>

  <h2>7. Repository Details</h2>
  <p>This project, including the Power BI file and dataset, is available on GitHub. Clone the repository and explore the report further:</p>
  <pre><code>
    git clone https://github.com/username/netflix-analysis-powerbi.git
  </code></pre>

  <h2>8. Future Work</h2>
  <p>Future enhancements may include:</p>
  <ul>
    <li>Sentiment analysis of titles and descriptions.</li>
    <li>Integration of audience reviews for deeper analysis.</li>
    <li>Comparative analysis with competitors like Amazon Prime and Disney+.</li>
  </ul>

  <h2>9. Acknowledgments</h2>
  <p>Thanks to Netflix for providing the dataset and to Power BI for making visualization and insights easier.</p>

</body>
