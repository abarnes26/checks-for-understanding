## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

1. List the five common HTTP verbs and what the purpose is of each verb.
>> Get - Reads data
   Put - Updates/ replaces
   Post - Creates data
   Delete - Deletes data
   Patch - Updates/ modifies
   
2. What is Sinatra?
>> A ruby based web application framework.

4. What is MVC?
>> Three basic parts of a web application(Models, Views, and Controllers).

5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
>> For readability and uniformity across the web, in adherance to the RESTful method.

6. What types of variables are accessible in our view templates without explicitly passing them?
>> Instance variables

7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?
  
  ```ruby
  get '/horses' do
    @count = 1
    erb :index :locals => {:name => 'Mr. Ed'}
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
9. What's the purpose of ERB?
>> It allows access to ruby methods side by side in a file with html.

10. Why do I need a development AND test database?
>> 

11. What is CRUD and why is it important?
>> Create/ Read/ Update/ Delete - It's the foundation of how we interact with databases.

12. What does HTTP stand for? 
>> Hyper Text Markup Language

13. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
>> One is to embed your ruby between "<%= %>".  This will print the output of the selected ruby on the page, where as "<% %>"
   will execute the code, but won't print anything.
   
14. What's an ORM?
>> Object Relational Mapping, it is how we link classes of data together and access them in a database.

15. What's the most commonly used ORM in ruby (Sinatra & Rails)?
>> ActiveRecord

16. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
>>  GET  "/restaurants" - View an index of all restaurants.
    POST "/restaurants" - Submit data to create a new instance of a restaurant.
    GET  "restaurants/:id" -  View a page for one individual restaraunt.
    GET  "/restaurants/new" - View form to submit a new instance of restaurant.
    GET  "/restaurants/:id/edit" - View form to submit changres to an existing restaurant.
    PUT  "/restaurants/:id" - Submit changes to an existing restaurant
    DELETE "/restaurants/:id" - Remove a restaurant from the database.

17. What's a migration? 
>> The act of creating the database's schema.

18. When you create a migration, does it automatically modify your database?
>> No, it sets up the blueprint (schema) for how your database will be managed and organized

19. How does a model relate to a database?
>> A model will contain the behaviors associated with your classes and any relationships therein.

20. What is the difference between `#new` and `#create`?
>> "New" will create a new instance of a specific class, but will not be permantently saved to your database.  You can accomplish this by following that instance with the command "save."  "create" will accomplish both of these tasks with the same action.

Review Questions:  
21. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?  
>> loaded_file = CSV.open 'file/path', headers:true, header_converters: :symbol
   loaded_file.each do |row|
      Class.create!(id: row[:id], title: row[:title], description: row[:description]
   end

22. Given the following hash:
```
activities = {
  hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
  karaoke: {cost: $10, supplies: ['courage', 'microphone'],
  brunch: {cost: $35, supplies: ['mimosa flutes'],
  antiquing: {cost: $200, supplies: ['list of antique stores'] 
}
```
How would I add 'granola bar' to things you should have when hiking?
>> hiking:[:supplies] = 'granola bar'

23. What are the 4 Principles of OOP? Give a one sentence explanation of each.
>> Abstraction - Expressing complex ideas in simpler means
   Inheritance - The idea that children (classes) should inherit behaviors from their parent (classes).
   Encapsulation - Only revealing as much data as is necessary to peform the required functions, and keeping everything else                      private.
   Polymorphism - The ability for one function to serve many purposes and not be restricted to one avenue of functionality.
