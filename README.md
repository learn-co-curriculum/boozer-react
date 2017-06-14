# Boozer React Mini-Project

Today, we're going to be building a React project from scratch! We'll be using an awesome tool from facebook to bootstrap our app called `create-react-app`. To use it, first, install the package globally (for CLI tools, we usually install npm packages in a global location)

```bash
npm install -g create-react-app
```

Next, we'll create our application.

```bash
create-react-app boozer-react
```

This will create a new app in the directory where you run the command. Simple!

### Instructions

0. Using `create-react-app`, create a new project called `boozer`.
1. We've provided you with an API. Fork and clone the api, then run `rake db:migrate` and `rake db:seed`. We have two endpoints right now: `/api/v1/cocktails` renders out a list of cocktails and their proportions. Our domain model is that  cocktail has many proportions and has many ingredients through those proportions.
2. Create a component called `CocktailsContainer`. This component should fetch a list of cocktails from the API and render our the cocktail names.
3. Next, each cocktail name should be a clickable link. Clicking on this link should render out a detail view of the cocktail including the name, description, instructions, and proportions. **HINT** - use react-router-dom to update the URL as you click on each particular cocktail. Our goal is to have a "Master-Detail" layout - our list should be ever-present on the left side and our detail view should take up two thirds of the screen.

### Part Two

Once you finish the above features, start implementing the below user stories. **NOTE** You will have to add endpoints to the API to make these work properly.

0. As a user, I should be able to create a new cocktail. This means we will need a form where I can enter a cocktail name, description, instructions, and multiple proportions. The form should be dynamic - I should be able to choose how many different proportions I want to add.

**NOTE** - there is a lot of functionality tied up in this one user story. You probably need to break this one up into multiple stories. Focus on small pieces of work at a time. First, maybe you want to make a form that just has a user enter in a cocktail name? Then let the user submit that form? Then add a hard-coded number of proportions? Build in small chunks and don't worry about edge cases to start. Pretend that the user will do everything perfectly.

1. As a user, I can filter the list of cocktails by name. This means I need a search input to enter in a name. Our list should then only show cocktails whose name matches.
