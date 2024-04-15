### Revised App Design Project - README Template by Freddy

#### Meal Recipe App

An application designed to simplify recipe discovery and cooking processes, focusing on ingredients, quantities, and servings. Utilizes the [MealDB API](https://www.themealdb.com/api.php) for comprehensive recipe integration.

## Table of Contents

1. [Overview](#overview)
2. [Product Spec](#product-spec)
3. [Wireframes](#wireframes)
4. [Schema](#schema)

## Overview

### Description

The Meal Recipe app offers users a convenient platform to explore and save diverse recipes for their culinary endeavors. Integrated with the MealDB API, users can access a vast collection of recipes, enhancing their cooking experiences.

### App Evaluation

- **Category:** Food & Drink
- **Mobile:** Yes, it's a mobile application.
- **Story:** The app aims to streamline recipe discovery and cooking processes for users by providing a comprehensive database of recipes.
- **Market:** Targeted towards individuals interested in cooking, from beginners to experienced chefs.
- **Habit:** It can be a daily companion for individuals seeking cooking inspiration or occasional users looking for specific recipes.
- **Scope:** The app offers a broad range of features related to recipe search, saving, and cooking instructions.

## Product Spec

### 1. User Stories (Required and Optional)

**Required Must-have Stories**

* User can search for recipes based on food names
* User can view detailed recipe instructions, including ingredients and cooking steps.
* User can save favorite recipes for future reference.

**Optional Nice-to-have Stories**

* User can create a shopping list based on selected recipes.
* User can share recipes with friends or family via social media platforms.
* User can contribute their own recipes to the app's database.

### 2. Screen Archetypes

- [ ] **Recipe Search Screen**
  * User can search for recipes based on various criteria.
- [ ] **Recipe Detail Screen**
  * User can view detailed instructions for a selected recipe.
- [ ] **Saved Recipes Screen**
  * User can access a list of saved favorite recipes.
- [ ] **Shopping List Screen**(Optional)
  * User can view and manage ingredients for selected recipes.

### 3. Navigation

**Tab Navigation** (Tab to Screen)

- [ ] Home
- [ ] Favorites
- [ ] Shopping List

**Flow Navigation** (Screen to Screen)

- [ ] Category Cell 
  * Leads to Meal Category Screen
- [ ] Meal Cell 
  * Leads to Meal Detail Screen

## Wireframes

![wireframes](https://github.com/fcamas/Group-Milestones/assets/76220782/cf93a7e9-18d9-49b7-9670-0b3f929e6b91)


### [BONUS] Digital Wireframes & Mockups

### [BONUS] Interactive Prototype

## Schema 

### Models

**Category**

| Property            | Type    | Description                               |
|---------------------|---------|-------------------------------------------|
| categoryId          | String  | unique id for the category                |
| categoryName        | String  | name of the category                      |
| categoryImageURL    | String  | URL of the category image                 |
| categoryDescription | String  | description of the category

**Recipe**
| Property   | Type   | Description                           |
|------------|--------|---------------------------------------|
| recipeId   | String | unique id for the recipe              |
| name      | String | title of the recipe                    |
| imageURL   | String | URL of the recipe image               |

**Detail**
| Property    | Type       | Description                              |
|-------------|------------|------------------------------------------|
| id          | String     | unique identifier for the detail         |
| instructions| String     | cooking instructions for the recipe      |
| ingredients | [String]?  | list of ingredients for the recipe       |
| measures    | [String]?  | corresponding measures for the ingredients |



### Networking

- **Recipe Search Screen**
  - (GET) Fetch list of recipes based on user search criteria
- **Recipe Detail Screen**
  - (GET) Retrieve detailed information for a selected recipe
- **Saved Recipes Screen**
  - (GET) Fetch list of user's saved favorite recipes
- **Shopping List Screen** (Optional)
  - (POST) Add ingredients from selected recipes to the user's shopping list
