# CyberChef Recipes

This repository contains a list of CyberChef recipes you may find useful when working with data in cyber security. The repo is split into recipe types, each described below. Good luck with your data manipulations!


> CyberChef is the self-purported 'Cyber Swiss-Army Knife' created by GCHQ. It's a fantastic tool for data transformation, extraction & manipulation in your web-browser. For more details, visit https://gchq.github.io/CyberChef/.


## Tips for Getting Started

### Loading a Recipe
 
 1. Copy the recipe code under the "Code" section of recipe or from the associated `.json` file. The Code section conains the recipe in Chef format.
 2. Select the "Load recipe" button in CyberChef (folder icon).
 3. Paste in the code and press Load.


## Malware Analysis

> Recipes for working extracting useful information from malware.


### recipe1

- Convert data from Base64.

#### Code

`From_Base64('A-Za-z0-9+/=',true,false)`
