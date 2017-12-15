## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

1. What is the entry at the command line to create a new rails app?

#### "rails new (project name) -d="postgresql"(to change from sqlite to psql) + any other modifications you'd like to make. 

2. What do Models generally inherit from in rails?

#### "Application Record"

3. What do Controllers generally inherit from in a rails project?

#### "Application Controller"

4. How would I create a route if I wanted to see a specific horse in my routes fitle assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?

#### resources :horse, only: [:show]

5. What rake task is useful when looking at routes, and what information does it give you?

#### "rails routes" - all designated routes in your application

6. What is an example of a route helper? When would you use them?

#### "new_class_subclass(class)" these are useful when making a "link_to."

7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?

#### "_path" is useful for rendering views. _url is useful for redirects.

8. What are strong params and why are the necessary?

#### Strong params are methods meant to control and limit which params get passed from the url to other methods.

9. What role does `form_for` play in helping us create our forms?

#### form_for does all the work of the action/method form line (standard html).  They work intuitively based on the current path.

10. How does `form_for` know where to submit the user's input?

#### It's based on the current view/ path.

11. Create a form using a `form_for` helper to create a new `Horse`. 

#### <%= form_for @horse do |f| %>
#### <%= f.label :name %>
#### <%= f.text_field :name %>

#### <%= f.label :breed %>
#### <%= f.text_field :breed %>

#### <%= f.submit %>

#### <%end%>

12. Why do we want to validate our models?

#### To ensure that all necessary information has been passed through to create the the object.
