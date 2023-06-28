# Restaurant Menu Pseudo
## Requirements
MoSCoW
1. MUST
- WIREFRAMES for website design
- Basic information regarding the name, address, and hours of restaurant
- BOOTSTRAP via NPM
- API retrieval through AXIOS
- DYNAMIC menu - SECTIONS such as appetizers, pasta, sandwiches, etc
               - AT LEAST 15 meals
               - ORGANISM display for each section
               - BOOTSTRAP card for each meal
- MANAGE react component state
- RESPONSIVE to mobile users

2. SHOULD
- ICONS for spicyness, vegan options, etc
- CHANGE menu based on time of day
- EMBEDDED NPM google map for location of restaurant

3. COULD
- CREATE own JSON
- MODIFY title and meta tags using create-react-app
- IMPLEMENTING a doordash style online shopping card with temp save data for purchase
- USE React context
- SPECIALS menu that changes each day, kept in local storage so it never changes

4. WONT
- SHOW the restaurants failing health score

## BEGIN
1. Atoms
    - Description for each corresponding meal
    - Location
    - Icons

2. Molecules
    - Each meal and collective descriptions 
    - NPM locational data retrievable through google
    - Wireframe representation

3. Organism
    - Each section containing several meals
    - Interactive meals based on time of day/day of week
    - Doordash implementation

## INIT - VARIABLES & FUNCTIONS
1. Menu
    - displayMenu
    - const meals
    - meal.name, meal.price, etc
    - dailySpecials
        - VARIABLES for rendering and displaying menu as well as additional icons/specials

2. Online ordering
    - selectedMeal
    - mealNumber
    - confirmOrder
    - const confirm
    - userInput
        - VARIABLES for performing the necessary steps to place an order, such as updating a database or sending a request

3. Location
    - locationalData
        - VARIABLES for finding the restaurant through a search engine

## RENDER - FUNCTION STRUCTURE and OBJECTS

import React, { useEffect, useState } from 'react';
import { getLocalStorage, setLocalStorage } from '../utils/localStorage';

1. function displayMenu () {
    - const ENDPOINT = 'MEALS';
    - const [meal] = useState([menu meals]);

    - const [dailySpecials] = useState([specials?]);

    - return (
      - <div>
        - <h2>Menu:</h2>
        - {menumeals.map((meal) => (
          - <div key={meal.name}>
            - <p>Name: {meal.name}</p>
            - <p>Price: {meal.price}</p>
            - <p>Spiciness: {meal.spicinessIcon}</p>
            - <p>Vegan: {meal.veganIcon}</p>
            - <p>Substitution Options: {meal.substitutionOptions}</p>
          - </div>
        - ))};
      - </div>
    - );
  - };


2. function location() {
    - const [locationalData] ([]); }

3. 



MAYBE ??
export function getLocalStorage(listName) {
  const saved = localStorage.getmeal(listName);
  return saved && saved.length > 0 ? JSON.parse(saved) : [];
}

## END