# Meal-Planner

A simple Python command-line tool to help you figure out how many meals you can make from your available ingredients and calculate the cost per meal.

---

## Table of Contents

* [Overview](#overview)
* [Features](#features)
* [File Formats](#file-formats)
    * [Recipes File (recipes.csv)](#recipes-file-recipescsv)
    * [Inventory File (inventory.csv)](#inventory-file-inventorycsv)
* [Installation](#installation)
* [Usage](#usage)
* [Future Enhancements](#future-enhancements)
* [Contributing](#contributing)
* [Licence](#licence)
* [Contact](#contact)

---

## Overview

This tool helps you manage your kitchen inventory and meal planning. By providing a list of recipes and your current ingredient stock, it can tell you:
* How many servings of a specific meal you can prepare.
* The estimated ingredient cost for one serving of that meal.

## Features

* Reads recipe data from a CSV file.
* Reads ingredient inventory and costs from a separate CSV file.
* Calculates the maximum number of servings for a given recipe based on available ingredients.
* Calculates the ingredient cost per serving for any recipe.
* Command-line interface for easy interaction.

## File Formats

It's crucial that your input CSV files follow these exact formats for the tool to work correctly.

### Recipes File (recipes.csv)

This file defines your recipes, with each line representing one ingredient required for a single serving of a recipe.

**Format:** `RecipeName,IngredientName,Quantity,Unit`

* `RecipeName`: The name of the meal (e.g., "Pasta Carbonara").
* `IngredientName`: The specific ingredient required (e.g., "Spaghetti", "Eggs").
* `Quantity`: The numerical amount needed for *one serving*.
* `Unit`: The unit of measurement (e.g., "g", "ml", "unit", "cup", "tbsp"). **Units must exactly match those in the `inventory.csv` for the same ingredient.**

**Example `recipes.csv`:**
```csv
Pasta Carbonara,Spaghetti,200,g
Pasta Carbonara,Eggs,2,unit
Pasta Carbonara,Pancetta,50,g
Pasta Carbonara,Parmesan,30,g
Chicken Curry,Chicken Breast,300,g
Chicken Curry,Curry Paste,50,g
Chicken Curry,Coconut Milk,200,ml
Simple Salad,Lettuce,100,g
Simple Salad,Tomato,1,unit
Simple Salad,Cucumber,0.5,unit
```

### Inventory File (inventory.csv)

This file lists the ingredients you currently have on hand and their cost.

**Format:** `IngredientName,QuantityAvailable,Unit,CostPerUnit`

`IngredientName`: The name of the ingredient (must match IngredientName in recipes.csv exactly!).
`QuantityAvailable`: The total numerical amount you have.
`Unit`: The unit of measurement for your available quantity. Must match the unit used in recipes.csv for the same ingredient.
`CostPerUnit`: The cost of one unit of that ingredient (e.g., cost per gram, per ml, per single egg).


**Example `inventory.csv`**:
```csv
Spaghetti,1000,g,0.0015
Eggs,12,unit,0.20
Pancetta,200,g,0.01
Parmesan,100,g,0.02
Chicken Breast,1500,g,0.008
Curry Paste,300,g,0.005
Coconut Milk,400,ml,0.003
Lettuce,500,g,0.006
Tomato,3,unit,0.30
Cucumber,1,unit,0.50
```

## Installation

You only need Python 3.6 or higher installed on your system.

Download Python
<!-- end list -->

Clone the repository:

```bash
git clone https://github.com/atinyduck/Meal-Planner.git
cd Meal-Planner
```

Create your recipes.csv and inventory.csv files in the project directory, following the formats described above.

## Usage
(This section will be filled in once we write the Python code)

## Future Enhancements

Support for different units and automatic unit conversion (e.g., kg to g, litres to ml).
Ability to add/remove ingredients directly from the CLI.
Interactive mode for meal planning.
Graphical User Interface (GUI).
Suggesting recipes based on available ingredients.
Contributing
Contributions are welcome! Please feel free to fork the repository and submit pull requests.

## Contributing
(This section will be filled in once v1.0 is released)

## Licence

Distributed under the MIT Licence. See LICENCE for more information.

## Contact

Jake Morgan - your_email@example.com

Project Link: https://github.com/atinyduck/Meal-Planner
