# MovieLense Film Recommendation system
by Chris Adu

# Background
I built a recommender system to help select movies to watch based on item similarities. 
I am using the Movie Lense Dataset which has over one hundred thousand entries of film ratings between 0 - 5. My focus was on the two films star wars(1977 original) and Liar Liar and I wanted to see if the recommender model will be able to provide me good recommendations based on selected film of choice. 

# Exploratory Data Analysis
I initially analysed the database to understand two key things:
- 1. What films had the highest ratings
 <img width="839" alt="Screenshot 2023-12-28 at 11 03 34" src="https://github.com/ceebeeaka89/Recommender_System_FilmsProject/assets/54710939/7a335d4b-2dc7-4980-beba-57892c5df491">

     
- 2. What films had the most ratings
<img width="830" alt="Screenshot 2023-12-28 at 11 04 29" src="https://github.com/ceebeeaka89/Recommender_System_FilmsProject/assets/54710939/4169b694-9abd-4534-afec-480cfe3f2df4">


**Distribution of Number of Ratings**

<img width="472" alt="Screenshot 2023-12-28 at 11 10 41" src="https://github.com/ceebeeaka89/Recommender_System_FilmsProject/assets/54710939/fb5c11a9-7956-4cd3-8aa9-12087db985c7">

- This demonstrates that there are only a smaller number of films with over 200 ratings. 
- Most movies have between 0 and 1 ratings, this seem plausible because the most popular blockbuster films will have the most ratings and they are the minority of films therefore less successful film which will be the majority will be watched by fewer people hence less ratings.

**Distribution of Ratings**
  
<img width="464" alt="Screenshot 2023-12-28 at 11 17 16" src="https://github.com/ceebeeaka89/Recommender_System_FilmsProject/assets/54710939/01a1db5f-99fa-4d60-8071-bc9cf6173d98">

- This distribution of the ratings themselves has peaks at the whole numbers(1,2,3,4,5), this possibly because only a few people watched those movies and gave it whole number rating.
- Most are distributed normally between 3 and 4.
- There are a few outliner ratings at 1 and 5 ; these movies most likely had a few people watching it and gave it very bad or very good rating. However could also be the very popular blockbuster movies that the majority of people really liked or disliked.


**JointPlot of average rating vs number of rating**

- we see a positive correlation between higher ratings and number of ratings.
- there are a few outliners again in at 1 and 5.
<img width="341" alt="Screenshot 2023-12-28 at 12 01 50" src="https://github.com/ceebeeaka89/Recommender_System_FilmsProject/assets/54710939/8fb9ef3a-52b9-4718-bd43-706d7e30bbbf">


# Summary of Model

Using correlation based on results ratings of movies and focusing on films that had more than over 100 ratings( to get rid of potential outliners) I was able to find results that proved convincing in similarity.

Below is the results for correlation with Star wars:
  
<img width="837" alt="Screenshot 2023-12-28 at 12 06 22" src="https://github.com/ceebeeaka89/Recommender_System_FilmsProject/assets/54710939/2dc07725-6c16-4cba-9a43-171201502ac2">


- We can see that movies Empire Strikes Back , Return of the Jedi are the highest correlated with 0.749 & 0.673 respectively. This is followed by Raders of the Lost Ark which is a similar style movie. There is drop off in the model when it comes to Austin Powers with a correlation of 0.377 this could be due to the movie being a comedy and not a sci-fi like star wars, however the reason it made the recommendations is potentially due to popularity of the film. 

Below is the results for correlation with Liar Liar:
  
<img width="841" alt="Screenshot 2023-12-28 at 12 06 47" src="https://github.com/ceebeeaka89/Recommender_System_FilmsProject/assets/54710939/6333117e-91c9-4faa-8d2f-10c3d0e30d9b">


- The model doesn't show as strong a correlation when it comes to the movie 'Liar Liar', with the highest correlations being 0.517.
- This possibly due the movies highest recommendations being from a variety of genres, however the same lead actor(Jim Carrey) in  all the top three movies is the same.
- There could be a link that a popular actor in a blockbuster film could be key to other blockbuster popular films with the same actor getting a similar rating.

  # Tools Used
  - Seaborn
  - Matplotlib
  - Correlations
  - Movie Lense Dataset
    

