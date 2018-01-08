1. How do we make flash messages display on a page?
- By creating them in the controller method of your choice and calling them in the body of 'application.html'

2. Where is cart information/temporary information usually stored?
- In the sessions hash

3. What might be some reasons not to store cart in our database? Are there any reasons why we would want to persist that information?
- We would not want to store cart information in the database as it's not always associated with a user (usually a session). We want to persist that information because we want their potential purchases to be avilable after they log in and when they leave and return to the website. Otherwise it causes extra work for the user and decreases the chance of a purchase.

4. What is the purpose of the asset pipeline?
- To import necessary data for displaying your webpage and to decrease the number of unnecessary trips to the server by storing some information on the client's computer (cache).

5. Why do we precompile our assets?
- to cut down on the size of the files that travel between the server and client.

6. What do each of the following tags do?

```ruby 
<%= stylesheet_link_tag "application" %> - a shortcut to link a stylesheet

<%= javascript_include_tag "application" %> - links a javascript file

<%= image_tag "rails.png" %> - a shortcut for displaying an image file
- 
```

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?

- A good readme has a "What," "why," "where," and "how."  It should also include screenshots of tests and implementation.

8. What are the top four accessibility issues that we as developers should be aware of?
- Those that cannot use a mouse, the blind, the deaf, and reading disorders.

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?
A Callback, we would find it at the top of our controller file.

10. Given the following object, how would we create a scope for all users who are active?

```ruby 
User.create(name: "Happy", active: true)
```

11. What is the difference between a scope and a class method?
