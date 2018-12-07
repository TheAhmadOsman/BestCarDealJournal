# <center>Best Car Deal Journal</center>

### <center>Ahmad Osman</center>

## <center>Analyzing 1,700,000 Cars Listings to Find the Best Deal</center>

### October 25, 1pm

I talked with Austin about teaming up for this project. We discussed the possibilities and he brought up the idea of Craigslist scraping and analyzing data from there, specifically vehicles data. I am actually trying to buy a car myself and this would be very beneficial to me. We agreed to think about it and come back to continue our thoughts later.

I get lost every time I go on Craigslist, and I wish it was simpler or more concrete. I had plans to actually write a script that would be following new listings on Craigslist and to notify me if some relative deal is posted, but I did not know how to write such a formula to know if a car is a good deal or not.

Not only that I did not know what is a good deal, I really do not know what to assess a car based on. I have zero knowledge about cars and in  our quest on such data I would be learning about cars and manufacturers, and with the analysis and visualization, I would be able to find out what to look for in a good car deal for my earlier-thought-about script to notify me about.

### November 1, 11pm

Met with Austin and we decided further pursue our initial idea. I brought up the idea of a script that would notify me about good deals and the idea caught Austin's attention, he asked if we might consider building a Flask App to do this, which would help me not only get notifications, but also lively visualize data. This is a super idea and I am very excited for it.

The Flask app would be designed in such a way that we would allow users to choose between graphs they want to visualize. This would be a platform to allow users to build their own customized graphs by selecting the type of graph to visualize and the kind of data to visualize on said graph. We also have this idea of displaying statistical insights on visualized maps. We also agreed on having customizable heated maps.

Furthermore, we thought it would be awesome if the graphs can allow multiple columns to be visualized simultaneously at the same graph, and that we would allow choosing graphs titles, sizes, colors, etc... We also hope to be able to build graphs specific to a location and a radius, but this is kinda of a stretch.

### November 2, 7pm

I started looking at the data we could parse from Craigslist, we have 700,000 entries, with such amount of data I think we could be answering a couple of good questions such as:

* What is a good car deal?
* Which states should my focus be on when looking for cars being sold?

The data seems to have a mix of categorical and numerical variables, and this is great for different kinds of graphs. I am kinda of disappointed that we only have longitudes and latitudes instead of specific location and addresses. However, I think we would be able to figure this problem out later as we get further into our analysis requirements.

I talked with Austin and we agreed we need to start visualizing simple line graphs of strong variables such as prices and odometer. I started doing some of this visualizations in a Jupyter notebook and it looks like plotting 700,000 entries in a line graph can make Pandas crash (who knew!).

### November 3, 5pm

I thought about sampling the 700,000 entries we have and take like 50,000 of that to visualization, however, I am even more concerned right now that 700,000 won't be good enough to analyze to come up with an answer to a good car deal.

If I am buying a car myself, my search would not be happening over the span of a 24 hours, I believe it would take me at least a month to catch a good deal. For this exact reason, I think we should scrap more data, we should make our data as close to the listings of a month-long as possible.

I tried plotting the data again, and this time it worked and Pandas did not crash. There is a clear, and very expected, fall in price as the odometer increases. I started looking at different manufacturers and we have 53 different manufacturers. I talked with a friend who has gone through the process of buying a car before and I understood that there are American, European, and Japanese cars that people try to choose from. Also, the idea of automatic and manual cars are still confusing to me. I hope I would learn about all of that along the this project.

### November 6, 1pm

I met with Austin and we talked about our findings. We agreed that the data seem to be causing Pandas to crash, but we also agreed on my idea of how long it would take for someone to buy a car, and that we actually might need to add more data. Scrapping will happen two more times within the next two weeks.

For the Flask App, we agreed that until we get it optimized, we will take a sample of the data to make our Flask graphs from. I told Austin that Flask is not exactly the best framework to build such a heavy app on, but this is for later to change or make decisions about.

Austin showed me a heatmap he built using latitudes and longitudes with Folium. Clearly a heatmap is going to be equally heated from a zoomed-out perspective, and only when we zoom into specific counties it start to make more sense.

Our plan is to continue looking at different graphs and variables and see what insights would those graphs give us.

### November 7, 8pm

I started looking at manufacturers and I think in our analysis we should focus on the top 10 manufacturers by the number of listings of each manufacturer. Looking at a pie chart of the top 10 manufacturers I could see that Ford is the most popular top-10 manufacturer, and BMW is the least popular top-10 manufacturer. So, I am assuming that Ford is going to be relatively cheaper due to demand and supply laws.

Right now we are looking at single variables and making assumptions about availability, and I plan to further explore this with multiple variables, which is part of our initial plan anyway. In the end, I want to see a good deal for a used, in a good condition, car from the top-10 manufacturers.

I also look a bar graph for the mean price per top-10 manufacturers, it is an interesting graph, but again, I am worried that any assumption made from this is not counting for the cars condition, the state it is being sold at, the size of the car, etc. I do not want to think about this analysis as a correlation between number of cars offered and price. I will talk to Austin about this tomorrow.

### November 8, 5pm

Austin is working on custom bar graphs and was having some problems with user input, we tried Googling Flask solutions and worked on this for the main part of the class time.

We talked about my findings and agreed that our initial idea of analyzing by multiple variables is very important in this project, and that we cannot make a single-variable model as that won't count for all factors.

The plan for now is to continue working on our analysis and visualizations over the weekend and to update each others later next week. I plan on to start looking at solutions for finding the States given a longitude and a latitude.

### November 10, 9pm

I did not expect this to be so hard and I am so exhausted from just the research. I know our data is so large, so I am avoiding searching for online APIs, let alone that those and I would prefer a module that would be take a longitude and a latitude and give back a State and a County. Nothing came out of my research.

I want a local database, and maybe somebody has a way of connecting longitudes and latitudes to a DB of states and counties? I am not an expert of longitudes and latitudes, and I am not familiar with states and counties, so implementing an algorithm on that would take some tremendous amount of time, unless explicitly stated algorithm is found.

I will continue working on this tomorrow. States are essential to our analysis, I want to know if maybe visiting another State to buy a car from would be a good idea. Maybe I can plan a break trip to another state to buy a car - of course this means I need to find a good listing before, but still, it is worth a shot.

### November 11, 6pm

I could find multiple databases that had states information besides longitudes and latitudes, but I could not really figure out how to implement an algorithm to find the States and Counties given longitudes and latitudes to the DB.

My last resort is to look at online APIs for this, but still, we initially have 700,000 entries with more to have within a week from now. I am assuming we will be up to 2,000,000 entries, and to make 2,000,000 entries, I can only assume that this is gonna be impossible because we will be blocked from making requests, and to even do that with a CSV is quite hard to imagine being any fast.

I am going to discuss our options with Austin next class. For now, I will stop thinking about this until class time - maybe a different eye on the matter can give any solution. We will see.

### November 13, 1pm

Austin explained to me what he has been working on - the Flask App seems like a strong candidate for visualizing our data now. I like that both of us are actually passionate about this data set. I cannot wait to demo it, and it has a huge potential too!

I explained to Austin what I have been doing, and how finding the States is a hard task. We decided to focus on merging the newly scraped data and then to figure out if there is an API, even if it would cost something like 20 Dollars, to find the States and Counties we need.

We also had a conversation with Dr. Lee about our progress, and I asked him for his feedback on the question we are coming to formulate and to try to answer. I told Dr. Lee that I essentially wanted to buy a car, and he pointed out that I should look for the insurance of the car and to see if the car was flooded or not on that insurance. 

I now think that we will also need to figure out the weather information about each listing within the month of that listing.

### November 14, 6pm

I researched for websites that would allow us to see forecast data about listings, given a longitude and a latitude. But as a famous philosopher once said, you cannot always get what you want. The closest to that was OpenWeatherMap API, and it is not doing exactly what we wanted. And it is so EXPENSIVE for the amount of entries that we will be doing the requests on.

I think this is something that I should not focus on for now. It is a great hypothesis to try to see a correlation between floods and cars conditions/prices, and would be a great indicator, but we have a lot on our plates for this project right now.

I think what I will do is to find the historical average weather data of all states for October and November, and to use that as a preliminary analysis, it is a long shot but initial to what might come later if we decide to expand on this. I will look for the website over Thanksgiving break, even if I end up getting the data manually won't be a problem.

### November 15, 1pm

I talked with Austin about my findings about the weather and we agreed on my conclusion. He told me that we have about 1,100,000 entries, scraped over the last two weeks, divided on two CSV files, that we need to merge.

I have some concerns about duplicates, because for sure some listings would overlap over the three different scraped files we have now. I decided that the URL is unique, and that while looping through the data, if the same url exists, we will just drop the entry.

My plan for now is to merge the data and to decide afterwards how will we get the State date - it has to be done because it is essential to our analysis. This is challenging. Challenges are good.

### November 17, 10am

I decided to work with the data in SQL format. It is easier and will allow me to make the URL a primary key. By doing that, I will have 3 different DB files. I will use sqlite because it is simple, and I will simply open one DB in Python, and go over another DB, and update the first with the entries from the second one given that no primary key can be a duplicate. Then I did the same exact thing with the third DB file.

We ended up combining 1,700,000 entries in one DB file. It is easy to export a DB file into a CSV so our progress should still be valid on our newly combined data. I know for sure that our visualizations will be slower, but I am sure it is worth it. Having the URL as a primary key helped us merge the data we scrapped in October and November without any duplicates.

At this point, we believe that finding a good car for any individual can take a tremendous amount of research, and that it usually can take a span of a month to two, and that was one of the reasons we wanted to do our analysis on the total amount of cars being sold on Craigslist over a month. Our hypothesis right now is that 1.7 million cars would be what individuals looking to choose from in any given month.

### November 18, 2pm

My focus now is on finding the needed geographical data for our analysis. I was so lucky to come across the Federal Communications Commission Area API. It literally asks you to enter longitude and latitude and gives back a lot of info, in JSON format, including State and County.

I am still worried about sending 1.7 million requests to this website, and how long would it take, and if we would raise any flags and get banned. I read their policy, carefully, because I am a little extra worried being that I am an international student, although I should not be scared; still I am.

I decided to write a simple script and see if this would work, and it does! I added five new fields to our sqlite database, which are:

* county_name
* county_fips
* state_code
* state_name
* state_fips

Then I implemented an algorithm that goes through the all entries that have a null value in state_name, get long/lat of that entry and extract the above variables and update this very specific entry, using its URL primary key, with the new geographical values.

It is slow, very slow, like it take a minute to update 120 entries. I am not okay with this but I will work on it more tomorrow.

### November 19, 2pm

I think I will try to have a multi-threaded program to do this. But first, there are multiple problems that we need to deal with, first, we need to divide the database into batches because it will be faster that way, second, the data we receive from our requests for the geographical data sometimes return errors and I do not know why.

I was able to figure out how to loop through batches of our database, which solves the first problem.

After some debugging, apparently our data include Canadian entries, which we will need to filter out. I decided to give a value of "FAILED" to any long/lat that does not return the expected information.

I got a multi-threaded program written, but it is not working, and after a lot of research, apparently sqlite does not allow concurrent writing to its database. I need to convert the database to PostgreSQL.

### November 19, 11pm

I wish my day was 72 hours. Installing PostgreSQL is alone a lot of work, and to get it to run is quite hectic. There are multiple tools out there to convert from Sqlite to PostgreSQL, however, all of them raise errors when I try to convert my data. Looking at the logs it became clear to me that the problem is the different types' syntax between the two databases.

After a lot of research, I tried to try a simple solution, convert the Sqlite DB to CSV, and import the CSV into PostgreSQl, and alas! It worked. Indeed one does learn by trial and error.

For now, I will call it a night, and I will get back to the original plan of writing a multi-threaded program to grab the data we need.

### November 20, 8pm

Success. I was able to grab the states adn the counties for all entries. The program had more than a couple of errors, and I had to initiate a new connection and cursor to the database in each new thread, and it worked smoothly thanks to PostgreSQL.

I pushed the limits of numbers of threads per minute, and my machine was heating up so badly, however, I was successfully able to grab the geographical information for all 1,700,000 entries. 15,000 requests per minute, it was a stretch, and under two hours, I was able to have all the data I wanted. I was worried that I might get banned, but the FCC people are good people :D

Now, we have our states and counties, and ready to do our analysis and visualizations on those two variables. I sent the data to Austin and he was glad it worked out, we want to do a quite high number of visualizations with this geographical data, and now we can!

Long story short, we implemented a multi-threaded program that made about 15,000 requests per minute. We also had to migrate from Sqlite to PostgreSQL, since the former did not have any multi-threading support.

### November 21, 4pm

I did some visualizations with the States, and California comes at the first place with just below 160,000 cars being listed. I looked at the average price per state, and District of Colombia is the winner for that. I also noticed that there was about 70,000 entries from Canada, which we dropped from our data.

Now, we still need to the weather data. It might have an influence on the data. I was able to find a governmental website to help collecting weather data. I found the US Climate Data website, which had historical weather data for each State. I ended up taking the average historical temperature for October and November for each state and incorporated that in our database under the weather column.

I looked at weather and condition graph and there was no correlation, it was expected and I knew it was a long shot but still, as a preliminary step, it is not so bad. I sent the data to Austin and we will see what to do after the break.

### November 27, 1pm

Today we met with Simon and walked him through our work and the processes we went through to acquire the data and what does the data represent and what questions we hope to answer.

He saw the Flask App and we walked him through the idea of the Flask App and what we are trying to achieve with it. 

He also got to know what kind of visualizations we are trying to do to answer our questions and serve the purpose of answering our question.

I asked Simon to start his own exploration of the data, and to see if he can come up with some visualizations that can help us answer our questions.

### November 27, 11pm

Today we looked at a heated map based on the number of cars sold per county in the United States and also a map of the average price per county. The date seemed very interesting and I was really glad that our pursue of including geographical data.

We are not exactly sure how will we include that in our Flask App. I am more interested right now in getting our analysis in a notebook and I asked Austin to start combining a his most interesting graphs in one place so that we can build our presentation website from that.

I plan to start a Sphinx website soon, but I don't want to work on it in restructured text, and I plan to find a way to make Sphinx work with markdown.

### November 29, 1pm

Today Simon started showing us some of his basic explorations, I like that he is starting in a similar way to how we started when we first looked at the data. He is interested in the data and showing that he wants to work with us on this project.

We agreed that our final question is "What is the best car deal?" - we discussed that "best" is not exactly what we will end up with, but we decided to use that word because it is as "best" as we can get it to be.

We decided to start looking at percentiles of price, condition, and and odometer. We think this is essential for answering our question. We also started exploring different violin graphs to show correlations between condition and price, the result was not surprising at all.


### December 1, 10pm

I started working on the website. I have Sphinx configured, got a good theme, and started to plan out the structure of the sections of the website. I wrote our motivation, explained our data gathering process, and explained our incentives to answer the questions.

I started receiving notebooks from Austin and Simon with some graphs and some explanations, and I plan to combine them within my own notebook. This will help me structure the website later and prepare our presentation.

### December 3, 4pm

Austin, Simon, and I met to discuss our presentation. We layed out our plan and we decided our website should have the same structure as our presentation. I asked Austin and Simon to finalize their notebooks with descriptive comments to show our work on the website. I asked them to send me what they have as soon as they can and I would work on combining all our notebooks and then we choose the best graphs that would help showing our progress in exploring our data.

Austin showed us his progress with the quantile tables. I was surprised of the insights these tables have. Simply we can see the best deal of any condition, of a specified car manufacture, in a specific State, with a specified odometer, and dive in even further, by specifying more factors, and we would still be able to see the prices of the best deals.

I cannot help but imagine our Flask App being able to point out to those specific deals, I would be able to find a good car in no time based on this. This have to happen beyond the scope of this project right now, but I will work on it for sure.

### December 4, 9pm

Worked on including heatmaps in our website, and writing good descriptions for them. I wanted to include interactive versions of these heatmaps and we added links to those in our website.

We had to decide which quantile tables to choose for our website and how to show the potential of this, I really hope to make people in the class interested in our project.

I finished combining our notebooks and chose the best visualizations to have in our website. The plan is to get with Austin tomorrow to work finalizing the website and practicing the presentation.

### December 5, 7pm

We just finished building our website. We changed the theme and did some edits on the config file to suite our visual needs. 

We revised our layout of the website and how our narrative would work. We wanted to start with the motivation, followed by data gathering and secondary data gathering, and then jumping into basic explorations followed by more advanced exploration. We wanted our narrative to show how we steadily progressed with our analysis in complexity and how we were able to answer our question.

Wrote the final analysis of the chosen graphs, updated our motivation, saved images of the important graphs and took screenshots of the important maps plus linking to their interactive versions.

### December 6, 10:30am

We met at 9am today to go over the website and the presentation plan one more time. We had some last minute changes to add to the website and we added more description to one graph.

We assigned roles and decided on talking points. We also took some videos of the Flask App in case demoing it live in class failed.

I really hope we rock this presentation!

### December 6, 10pm

WOW. We did it! I wish we had the time to demo our Flask app, but since we did not, we added the video to our website so Dr. Lee can see them.

There is nothing I would do different if time goes back. I had a good group and worked with people who were interested in getting results.

I plan to revisit this project, but I would start by the way craigslist gets scraped and see if I can make it more efficient. Then I would get the data feed to Flask efficiently, probably via PostgreSQL, and get the best deals populated on a Google Maps based on percentiles using multiple variables. This would help me find a car, and has the potential to be a real platform that people use to find the best deals.

Overall 10/10 would do again!
