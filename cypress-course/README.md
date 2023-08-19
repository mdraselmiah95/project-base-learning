# Learning Cypress ecosystem and Testing 🧪

### You can open Cypress from your project root one of the following ways:

```bash
npx cypress open
```

### Testing Fundamentals

- Your tests will exist in a describe block. This block takes two arguments. The first is a description of what you are testing. The second is a callback function for your actually tests within that block

- Within your describe block, you will also have it blocks. It blocks will be single tests within an overall test file. The API for it() is the same as describe. The first argument is the title of an individual test, and the second argument is a callback function containing your test code

- Cypress gives you various commands to help you test. You can use these commands on the cy object. For example, cy.visit('/') will navigate the cypress runner to your home page. You have various other commands like cy.click(), cy.type(), cy.check(), etc. *docs NOTE: You must have your dev server running for Cypress to work. NOTE: Cypress has an async nature *docs

- You're often going to want to get an element from the DOM and make some sort of assertion. For example, my h1 element contains certain text. You can get elements in Cypress by using the get function, and pass in a CSS query selector

- After you get an element, you probably want to do something with that element, like make an assertion. You can to this by chaining on an assertion after getting an element. For example, get(h1).contains('text'). Cypress has various ways of making an assertion \*docs

- You can use it.only() to run a single test

- You can use a beforeEach function to perform certain actions prior to every test

- You aren't limited to just the cy.X commands, but you can create your own custom commands. You add your custom commands to cypress/support/commands.ts For example, you might add a custom command getData that gets an element by data-test
