This dataset was downloaded from Kaggle, has a high rating and looks like a fun learning experience.

After downloading and exploring the dataset, I noticed a few oddities. The first was having 4 Star columns (Star1-Star4). I presume the goal is to allow up to our Actors to be credited. It's also not entirely clear if Star1 is the top billed actor, followed by Star2, etc. It does make it tricky to search with more granularity, and my quick solution was to combine all the columns into one column called 'Cast'.

Of the 1000 movies listed, 171 films were missing the gross amount earned. Most were older films or foreign made films where gross earnings were not available.

Data Columns:
Poster_Link - Link of the poster that imdb using - Not used
Series_Title - Name of the movie
Released_Year - Year at which that movie released
Certificate - Certificate earned by that movie - missing 103 entries
Runtime - Total runtime of the movie
Genre - Genre of the movie
IMDB_Rating - Rating of the movie at IMDB site
Overview - mini story/ summary
Meta_score - Score earned by the movie - 159 entries missing
Director - Name of the Director
Star1,Star2,Star3,Star4 - Name of the Stars
No_of_votes - Total number of votes
Gross - Money earned by that movie - 171 entries missing
Confirmed all cells populated, documented missing cells above


Data Cleaning Steps
Collapsed unused columns (Poster Link, Movie Overview)
Merged Star1-Star4 into Cast
Removed ‘min’ from runtime, confirmed numerical
Streamlined column title names
Checked movie rating system, changed A (Adult) to R (Restricted) since they’re essentially the same.
