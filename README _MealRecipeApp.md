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
- [ ] **Shopping List Screen**
  * User can view and manage ingredients for selected recipes.

### 3. Navigation

**Tab Navigation** (Tab to Screen)

- [ ] Home
- [ ] Recipes
- [ ] Favorites
- [ ] Shopping List

**Flow Navigation** (Screen to Screen)

- [ ] Recipe Search Screen
  * Leads to Recipe Detail Screen
- [ ] Recipe Detail Screen
  * Allows navigation to Shopping List Screen
- [ ] Saved Recipes Screen
  * Leads to Recipe Detail Screen
- [ ] Shopping List Screen
  * Allows navigation to Recipe Detail Screen

## Wireframes

Super rough, so feel free to change it if anyone dislikes it
![Rough Image](https://i.imgur.com/Nq20KrN.jpeg)

### [BONUS] Digital Wireframes & Mockups

### [BONUS] Interactive Prototype

## Schema 

### Models

**User**
| Property | Type   | Description                                  |
|----------|--------|----------------------------------------------|
| userId   | String | unique id for the user                       |
| username | String | user's display name                          |
| email    | String | user's email address                         |
| password | String | user's password for login authentication     |

**Recipe**
| Property   | Type   | Description                           |
|------------|--------|---------------------------------------|
| recipeId   | String | unique id for the recipe              |
| title      | String | title of the recipe                   |
| ingredients| String | list of ingredients needed for the recipe |
| instructions| String | step-by-step cooking instructions     |
| imageURL   | String | URL of the recipe image               |
| category   | String | category or cuisine type of the recipe |

**DetailLocalData**
| Property    | Type       | Description                              |
|-------------|------------|------------------------------------------|
| id          | String     | unique identifier for the detail         |
| instructions| String     | cooking instructions for the recipe      |
| ingredients | [String]?  | list of ingredients for the recipe       |
| measures    | [String]?  | corresponding measures for the ingredients |

**DessertDetail**
| Property | Type       | Description                          |
|----------|------------|--------------------------------------|
| meals    | [Detail]   | list of dessert details              |

**Detail**
| Property           | Type    | Description                           |
|--------------------|---------|---------------------------------------|
| id                 | String  | unique identifier for the dessert     |
| strMeal            | String  | name of the dessert                   |
| strDrinkAlternate | String? | alternative drink option              |
| strCategory        | String  | category of the dessert               |
| strArea            | String  | area or region of the dessert         |
| strInstructions    | String  | cooking instructions for the dessert  |
| strMealThumb       | String  | URL of the dessert image              |
| ingredients        | [String]? | list of ingredients for the dessert  |
| measures           | [String]? | corresponding measures for the ingredients |

### Networking

- **Recipe Search Screen**
  - (GET) Fetch list of recipes based on user search criteria
- **Recipe Detail Screen**
  - (GET) Retrieve detailed information for a selected recipe
- **Saved Recipes Screen**
  - (GET) Fetch list of user's saved favorite recipes
- **Shopping List Screen**
  - (POST) Add ingredients from selected recipes to the user's shopping list
