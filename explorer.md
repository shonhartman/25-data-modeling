# Instructions

In each section below, you'll have some data described to you. List the models you would create, the fields those models would have, the data type for each field and a description of what the field is for. For example, if I said I wanted to model a todo, I might write something like:

## Todo Model
1. item - string - the actual description of what they want to do
2. completed - boolean - the status of whether it's completed or not
3. user_id - integer - the id for the user who owns this todo
4. created_at - datetime - when the todo was created

NOTE! For all of these, assume you have a User model that represents the person logged into the website.



# Quest 1 - Medium Clone

Let's start with an easy one. I've provided you with the minimum number of models, you just need to provide the field information. If you can think of additional normalized data that needs another model, don't feel restricted by what's here.

You're creating a simple Medium clone where people can write blog posts and comment on other people's blog posts. You want to have enough information to show the latest blog posts, blog posts for specific authors, and blog posts for specific categories. Categories and Authors need to match exactly for us to do this, so we'll make them their own models.

## Blog Post Model
1. title - string - the title of the post
2. content - string - the body of the post
3. tags - string, array - tags to classify the post
4. created_at - datetime - when the post was created
5. image_url - string - image associated with the post
6. read_speed - integer - average read time

## Comment Model
1. responses - string, array - user information for response author and response strings
2. likes - boolean, integer - total likes and personal preference

## Author Model
1. username - string - the user's unique name for Medium
2. name - string - the user's actual name
3. url - string - the url to the user's profile on Medium
4. image_url - string - the url to the user's avatar
5. publications - strings - ids, titles, descriptions, and urls for all publications
6. author_description - string - description of the author

## Category Model
1. title - string - the title of each post
2. image_urls - string - the url for each post
3. following - boolean - whether or not I follow this Category
4. image_url - string - the url to each image associated with each post
5. likes - boolean, integer - total likes and personal preference for each post





# Quest 2 - Twitter Clone

You're creating a Twitter clone. People can create tweets, follow other people and have followers. Keep in mind, unlike the blog post example where a comment is a separate entity, tweets responding to other tweets are still just tweets. Also, think about how Twitter turns a tweet into useful information. Do you think they scan tweets for @mentions and hashtags, or are they storing that kind of thing as additional fields? What models do we need to recreate Twitter?

1. card - array - collection of objects attributed to each tweet
2. description - string - description of user
3. site_url - string - @username card attributed to each tweet
4. image_url - strings - avatar and uploaded images
5. data - string - data encompassed in user tweets
6. categories - string, array - hashtags categories




# Quest 3 - Car Makes and Models

You're building a site that associates data with specific variations of specific cars. You need to break the data down from the manufacturer to the specific model. In other words, you need to model in such detail that the system knows that a 2007 Mustang and a 2013 Mustang are the _same_ thing (from the 5th Generation, 2005-2014), but that a 2015 Mustang is different from both of those. The car models should also know general information about the cars.

1. make - string - the make of the vehicle
2. model - string - model attributed to each vehicle
3. style - string, number - the style of the vehicle for instance Nissan Rogue 'SV'
4. year - number - the year the vehicle was manufactured
5. engine - string, number - the engine specifications
6. transmission - string - standard or automatic
7. image_url - string - the images associated with each vehicle
8. miles per gallon - number - estimated miles per gallon of each vehicle
9. exterior color - string - the vehicles exterior color
10. interior color - string - the vehicles interior color
11. VIN - string, number - the unique identifier for each vehicle




# Quest 4 - DC Comics

You've used the Marvel API quite a bit. Let's model a comic site of our own for DC. You'll need to think about the fact that there are characters (the superheroes), comics (the actual issues), series (the collections of issues), events (which consist of many issues), artists, writers, et cetera. This is an incredibly deep rabbit hole. Create at least 5 models that would be able to provide enough information for someone to build all of our Marvel apps, but in the DC universe.

1. characters - string - each character in the DC universe
2. description - string - a description for each character
3. image_url - string - images associated with each characters
4. comics - string, array - a list of all DC comics
5. creators - string, array - authors associated with their comic works
6. events - string, array - events associated with each character and each author involved
7. writers - string, array - writers and their associated works
8. artists - string, array - artists and their associated works

//
