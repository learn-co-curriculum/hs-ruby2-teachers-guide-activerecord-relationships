###SWABTS
  Build out a database in a Sinatra project with multiple tables that each connect to a different model.
  + MVC - Build model, view and controller for an additional model (Users)
  + DATABASES/ACTIVE RECORD -  Set up has_many/belongs_to relationships
  + ACTIVE RECORD - Understand how has_many/belongs_to works via a `user_id` column (or similar equivalent for other models)
  + ACTIVE RECORD - Build up and down migrations to both create and modify tables
  + FORMS - Build a sign up form for new users
  + MVC - Create a sign up POST controller that works with the sign up form to create new users
  + FORMS - Build forms for something like tweets that connect a tweet object to the user it belongs to
  + MVC - Create a `layout.erb` template and understand how the Ruby keyword `yield` is used within `layout.erb` to render partials
  + Advanced Students - start thinking about how to create another model to track user's followers or start using ActiveRecord validations?

### Motivation / Why Should You Care?
Last week we did a ton of work with ActiveRecord to get our databases hooked up to our apps. Our twitter database is pretty simple though - we just have one tweets table with users and their statuses. But what if we were keeping track of tweets and followers and trending hashtags and direct messages? We would need a much more complex database with separate tables and models for tweets, users, hashtags and direct messages. Getting all of these tables hooked up to each other and making all of these models play nice is super important and that is where we see the magic of ActiveRecord.

### Lesson Plan
***Code snippets can be found [here]()

+ Why separate tables and models: (tweet model, user model, hashtag model)
  * that breaking up the functionality of an app into smaller pieces makes it easier to scale up and debug applications.
  * Easier to have multiple developers working on different features at the same time
  * Removes the duplication of data - Your user is defined once and then referenced in every tweet that they write.

+ Tweet and User Model - making new user model
  * Create a new table. In terminal enter: `rake db:create_migration NAME="create_users"`. Will create new migration
    * In migration (in db directory) create `up` and `down` methods.
    * see code snippet 1
    *In terminal: `rake db:migrate` to create the table
  * Create Users model that maps to that table
    * Create `user.rb` file in `app/models`
    * In that file, create a User class that inherits from ActiveRecord::Base


### Conclusion / So What?


### Hints and Hurdles