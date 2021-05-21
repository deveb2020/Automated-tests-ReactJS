# Automated Tests for ReactJS

__This is a personal project for practicing purposes__

## Tech used

* React Testing Library [ https://testing-library.com/ ]
* Jest [ https://jestjs.io/ ]                 

## Project informations

__In this project I have created 2 projects inside so that I can familiarize myself with automated tests also I configured `ESLint`  to alert me to any syntax errors or best practices for Jest and Testing Library__

## ESLint & Prettier Config:

Start by installing ESLint using npm

```
  npm install eslint-plugin-testing-library eslint-plugin-jest-dom
```

Than go to package.json and `delete` the eslint config file

After that `create a file` in the glogabl directory with the name `.eslintrc.json`
  - Inside this file paste this 
  
``` 
{
  "plugins": ["testing-library", "jest-dom"],
  "extends": [
  "react-app",
  "react-app/jest",
  "plugin:testing-library/recommended",
  "plugin:testing-library/react",
  "plugin:jest-dom/recommended"
  ]
}
```
  
  And the last step in the directory of the project create a folder with the name `.vscode`.
    - inside this folder create a file with the name `settings.json`
      - Inside this file paste this
      
```
  {
    "eslint.options": {
    "configFile": ".eslintrc.json"
    },
    "eslint.validate": ["javascript", "javascriptreact"],
    "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true 
    },
    "editor.defaultFormatter": "esbenp.prettier-vscode",
    "editor.formatOnSave": true
  }
```

### I learned how to select DOM elements using `Queries` 

[ https://testing-library.com/docs/queries/about#priority ]   
 
* getByRole ( prefered by Testing Library )
* getByLabelText
* getByPlaceholderText
* getByText
* getByDisplayValue
* getByAltText
* getByTitle
* getByTestId ( not prefered )

### I learned  how to expect one result using Jest-Dom `Matchers` 

[ https://github.com/testing-library/jest-dom ]

* toBeDisabled
* toBeEnabled
* toBeEmpty
* toBeEmptyDOMElement
* toBeInTheDocument
* toBeInvalid
* toBeRequired
* toBeValid
* toBeVisible
* toContainElement
* toContainHTML
* toHaveAttribute
* toHaveClass
* toHaveFocus
* toHaveFormValues
* toHaveStyle
* toHaveTextContent
* toHaveValue
* toHaveDisplayValue
* toBeChecked
* toBePartiallyChecked
* toHaveDescription

### I learned how to Simulate an event using `userEvent's` 

[ https://testing-library.com/docs/ecosystem-user-event ]

