# Data-Exploration-using-Tableau
Visualizing Zomato's work in India using Tableau

## Introduction to the dataset
The subject area which is discussed here is Zomato – The online food delivery application. The dataset for the analysis is obtained from Kaggle.
#### About Zomato:
Zomato is one of the well-known food delivery app worldwide. Apart from delivery it gives us more information about a restaurant. In short, the purpose is to give the end users a clear idea about the restaurants in various parts of the country and make their work easier.


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

<img width="666" alt="Image1" src="https://user-images.githubusercontent.com/52580630/86415785-f7c6d580-bcbf-11ea-9294-60c6d53db346.png">

The analysis is carried out for the restaurants in India to gain insights from the dataset. Zomato extends their service in various parts of the country mainly focusing the cities.

<img width="546" alt="Image2" src="https://user-images.githubusercontent.com/52580630/86416532-19c15780-bcc2-11ea-955b-c663fb713850.png">

####                                                         Number of Restaurants in each City

<img width="653" alt="Image3" src="https://user-images.githubusercontent.com/52580630/86416560-2d6cbe00-bcc2-11ea-8cbb-f2567d2e7254.png">

India has nearly 8000 restaurants registered with Zomato in 21 cities. The bar graph shows the number of restaurants in a city with Zomato. New Delhi, the capital of India is having more number of restaurants registered with Zomato.

####                                                                   Ratings

<img width="323" alt="Image4" src="https://user-images.githubusercontent.com/52580630/86416549-2b0a6400-bcc2-11ea-8cc3-a488e2a6b2e8.png">

The restaurants in India are rated based on five different rating categories. All restaurants fall under any of these categories based on the aggregate rating. This bubble chart gives a view on how many restaurants falls under each rating category.


####                                                           Top cuisines in the country

<img width="596" alt="Image5" src="https://user-images.githubusercontent.com/52580630/86416551-2ba2fa80-bcc2-11ea-9ac0-1856edc698b0.png">

India is more famous for its different variety of food. To widely spread cuisines are said to be the more rated ones. Using a tree map, visualization has been done to pick out the top 10 cuisines in the Indian cities.

####                                                               Service Provided

<img width="149" alt="Image6" src="https://user-images.githubusercontent.com/52580630/86416552-2c3b9100-bcc2-11ea-89f4-2a6f62f43c21.png">
<img width="162" alt="Image7" src="https://user-images.githubusercontent.com/52580630/86416554-2c3b9100-bcc2-11ea-8e24-74dd483c868e.png">
<img width="133" alt="Image8" src="https://user-images.githubusercontent.com/52580630/86416555-2cd42780-bcc2-11ea-971a-762eb592795d.png">

Here the analysis is done to check whether the services provided in a restaurant has any effect on the rating. The services are Table booking option, Online delivery and switching to order menu. Bar graphs has been plotted to explore this section.

From the above graphs we can understand that,
1)	Restaurants that provide table booking and online delivery tend to have higher rating.
2)	Since no restaurants provide this service, nothing can be judged with this variable.

####                                                         Maximum and minimum cost in a City

<img width="633" alt="Image9" src="https://user-images.githubusercontent.com/52580630/86416557-2cd42780-bcc2-11ea-9881-89daf0b11f11.png">

A line graph is plotted to show the maximum and minimum cost for two persons in a city. Minimum value is shown in green and maximum in red.

####                                                           Votes Vs Aggregate Rating

![Image10](https://user-images.githubusercontent.com/52580630/86416558-2d6cbe00-bcc2-11ea-8d8e-e22749339f8a.png)

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



