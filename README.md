# Data-Exploration-using-Tableau
Visualizing Zomato's work in India using Tableau

### Analysis Questions
The analysis is carried out on different restaurants in a city that are registered with Zomato based on the provisions.
The questions to be analysed are
1)	What are the top cuisines in the country?
2)	Does the service provided in the restaurant have any effects on the rating?
3)	What are the minimum and maximum cost for two in a city?

### Visualization Tools 
The tools used are,    
1)	Tableau
2)	R

### Tableau Workbook
A workbook is published in tableau public the contains all visual analysis done with the data set. A dashboard is created to analyse some major sections of the dataset. By clicking on each country, the specific data can be visualized accordingly. The workbook can be accessed using public.tableau/shristeca/zomato

### Exploration of the dataset
Zomato is scattered all over the world providing services to the customers in various parts of the country. They have a strong base in India, United States and Australia. A world map visualisation is provided with the cities of the countries plotted where the service of Zomato is present.

The analysis is carried out for the restaurants in India to gain insights from the dataset. Zomato extends their service in various parts of the country mainly focusing the cities.

India has nearly 8000 restaurants registered with Zomato in 21 cities. The bar graph shows the number of restaurants in a city with Zomato. New Delhi, the capital of India is having more number of restaurants registered with Zomato.

The restaurants in India are rated based on five different rating categories. All restaurants fall under any of these categories based on the aggregate rating. This bubble chart gives a view on how many restaurants falls under each rating category.

India is more famous for its different variety of food. To widely spread cuisines are said to be the more rated ones. Using a tree map, visualization has been done to pick out the top 10 cuisines in the Indian cities.

#### Service Provided
Here the analysis is done to check whether the services provided in a restaurant has any effect on the rating. The services are Table booking option, Online delivery and switching to order menu. Bar graphs has been plotted to explore this section.

From the above graphs we can understand that,
1)	Restaurants that provide table booking and online delivery tend to have higher rating.
2)	Since no restaurants provide this service, nothing can be judged with this variable.

A line graph is plotted to show the maximum and minimum cost for two persons in a city. Minimum value is shown in green and maximum in red.

A line graph is drawn for the number of votes got and the average rating. This graph is achieved by R using ggplot2 library. The restaurants with lesser votes also have average rating equivalent to 5. So, the rating does not increase with the number of votes.

##### Code
```
data <- read.csv(file.choose(), header = TRUE, sep = ",")
install.packages("dplyr")
india<-data %>% filter(Country.Code == 1)
install.packages("ggplot2")
ggplot(data=india, aes(x=Aggregate.rating, y=Votes, group=1)) + geom_line()+geom_point()
```

### Final Insights
With the above visualizations we can conclude that,
1)	India is the country with more number of restaurants registered with Zomato.
2)	More number of restaurants in India are rated to be Average.
3)	The North Indian cuisine tends to be on top of all other cuisines.
4)	Service provided by the restaurants can be considered as one factor that affect the ratings.
5)	Delhi and Noida are having the minimum average cost for two people in a restaurant (Rs 50, not taking the cities with zero as minimum value).
6)	Delhi has the maximum average cost for two persons in a restaurant (Rs 8000).
7)	The rating got by a restaurant fairly depends on the number of votes. 



