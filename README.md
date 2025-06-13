# CyberChef Recipes

This repository contains a list of CyberChef recipes you may find useful when working with data in cyber security. The repo is split into recipe types, each described below. Good luck with your data manipulations!


> CyberChef is the self-purported 'Cyber Swiss-Army Knife' created by GCHQ. It's a fantastic tool for data transformation, extraction & manipulation in your web-browser. For more details, visit https://gchq.github.io/CyberChef/.


## Tips for Getting Started

### Loading a Recipe
 
 1. Copy the recipe code under the "Code" section of recipe or from the associated `.json` file. The Code section conains the recipe in Chef format.
 2. Select the "Load recipe" button in CyberChef (folder icon).
 3. Paste in the code and press Load.

!!!
## Malware Analysis

> Recipes for working extracting useful information from malware.


### recipe1

- Convert data from Base64.

#### Code

`From_Base64('A-Za-z0-9+/=',true,false)`

!!!

## Decoding Tokens

### Decoding JWT Tokens

![Decoding JWT Tokens](./images/decoding-jwt-tokens.png)

A JSON Web Token (JWT) is a compact, self-contained, and secure way to transmit information between parties as a JSON object. It's digitally signed to ensure the data hasn't been tampered with and is commonly used for stateless authentication, allowing servers to verify user identity without storing session information. Essentially, it's a trusted digital ID card that carries user data and permissions.

This CyberChef recipe can be used to decode a JSON Web Token to reveal it's header and payload information. See [jwt.io](https://jwt.io/) for extended usage.

#### Recipe

```
URL_Decode(true)
Fork('.','\\n',false)
From_Base64('A-Za-z0-9+/=',true,false)
Filter('Line feed','^{.*}$',false)
JSON_Beautify('    ',false,true)
```

