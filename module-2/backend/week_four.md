## Week Four Recap

### Instructions
Fork this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

* What is a cookie?
-- a hash of data stored on the clients machine that carrys with it user identification tags and corresponding data.
* What’s the difference between a session and a cookie?
-- a session is a hash that persists from page to page and stores user information data.
* What’s a flash and when do you want to use flashes?
-- A message to display a notice (usually either success or failure of a function).
* Why do people say “HTTP is stateless”?
-- An Http request doesn't carry data from previous requests with it, i.e. each request is as if it was the very first request.
* What’s authentication? Explain.
-- Authentication is using user-provided information to determine that someone is who they say they are.
* What’s the difference between authentication and authorization?
-- Authorization is used to control what content users have access to after they have authenticated their identity.
* What’s a before filter?
-- It's a method of running certain functions prior to any other function.
* How do we keep track of a user once they’ve logged in?
-- We store their user data in the "session" hash.  This hash persists until it is manually cleared (logging out).
* When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
-- Namespacing is most commonly used to give administrators access to web pages and CRUD functions that are restricted to regular users.  Nesting a resource is useful when you have data that is referenced by other data. An example of nesting something appropriately would be accessing a page for a book that was branched from a page about the author.  The book is nested in the author (authors/##/books/##).
* At a high level, what tools can you use to implement authorization? How would you use them?
-- Storing a username and password that the user creates, and when the credentials are reentered into a "log in" form, that users data is retreived and stored in the session hash. 
* What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
-- Using an enum is helpful when you are declaring certain privelages to some users and not others.  By adding a "role" to the data types, you can differentiate administrators and regular users.
* What are some strategies you can use to keep your views DRY?
-- Using a shortcut like a "partial" can cut down on repatitive forms in your views. You create the form once, and store it in its own file in the same directory and call it later.
