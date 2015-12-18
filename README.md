# Practice Rails MVC and Nested Routing

Create a Rails application that allows users to view books. The application must satisfy the below criteria:  

## To get started
Take a look around the app and see what you have to start. The following gems have been installed in the test and development group:

  ```
  gem 'pry-rails'
  gem 'rspec-rails'
  gem 'capybara'
  gem 'factory_girl'
  gem 'launchy'
  ```
- Create your databases `rake db:create`
- Write your tests and let them guide your development of the below requirements

## App Requirements
- A book has to have a title, author, and isbn code. It can optionally have a description and a genre.
- Visiting the /books path should contain a list of books.
- Visiting the /books/new path should display a form for adding a new book.
- If a book is saved I'm redirected to to `/books` and should new the book name I've added, if it is not I'm left on the `/books/new` page and displayed an error.
- Visiting the /books/5 path should show the book details for a book with ID = 5.
- Visiting the root path should display a list of all books.

Once these criteria have been met, add the ability for users to review books. For this challenge assume all books and reviews are added anonymously. The application must satisfy the following criteria:

- A book can have many reviews. Each review must contain a rating between only 1 and 5, a body, and a timestamp for when it was created.
- If a review is saved, I'm redirected to the `books/5` path, if it is not saved, I should be left on the new review form page and render errors associated with the review.  
- Visiting the /books/5/reviews/new should display a form for creating a new review for a book with ID = 5.
- Visiting the /books/5 path should also include all reviews for a book with ID = 5.

For additional practice create some acceptance tests that allow the user to complete the following stories.(Hint these should be passing according the above criteria):
- Viewing a list of books
- Adding a new book through a form
- Viewing the details of a specific book
- Adding a review for a specific book only shows on the details page for that book
