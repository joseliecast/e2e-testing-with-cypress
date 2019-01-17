# End to end testing with [Cypress.io](https://www.cypress.io/)

## Setting up Cypress on the repo

1. install cypress as devDependency `npm install -D cypress`
2. at `package.json` add script `"cy:open": "cypress open"`
3. on your terminal run `npm run cy:open`

## Adding test

1. cypress will automatically create folders

![created folder](folder.png "test")

2. we will put our tests in `integration` folder
3. cypress has methods that first require us to pass a handler like ID, class or a customized attribute

```javascript
cy.registerNewUser().then(() => {
    cy.visit('/')
        .contains('Become a Host')
        .click()
        .get('input[id="officeName"]')
        .type(OFFICE_NAME)
})
```
