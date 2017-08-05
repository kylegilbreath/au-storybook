Storybook is a development environment for UI components.
It allows you to browse a component library, view the different states of each component, and interactively develop and test components.

## Intro

![Storybook for React Demo](http://i.imgur.com/7CIAWpB.gif)

Storybook runs outside of your app. This allows you to develop UI components in isolation, which can improve component reuse, testability, and development speed. You can build quickly without having to worry about application-specific dependencies.

Here are some featured examples that you can reference to see how Storybook works: <https://storybook.js.org/examples/>

Storybook comes with a lot of [addons](https://storybook.js.org/addons/introduction/) for component design, documentation, testing, interactivity, and so on. Storybook's easy-to-use API makes it easy to configure and extend in various ways. It has even been extended to support React Native development for mobile.

## Table of contents

-   [Getting Started](#getting-started)
-   [Projects](#projects)
    -   [Main Projects](#main-projects)
    -   [Sub Projects](#sub-projects)
    -   [Addons](#addons)
-   [Contributing](#contributing)
    -   [Development scripts](#development-scripts)
    -   [Backers](#backers)
    -   [Sponsors](#sponsors)

## Getting Started

First install storybook:

```sh
npm i -g @storybook/cli
cd my-react-app
getstorybook
```

Once it's installed, you can `npm run storybook` and it will run the development server on your local machine, and give you a URL to browse some sample stories.

**Storybook v2.x migration note**: If you're using Storybook v2.x and want to shift to 3.x version the easiest way is:

```sh
npm i -g @storybook/cli
cd my-storybook-v2-app
getstorybook
```

It runs a codemod to update all package names. Read all migration details in our [Migration Guide](MIGRATION.md)

For full documentation on using Storybook visit: [storybook.js.org](https://storybook.js.org)

## Projects

### Main Projects

-   [Storybook for react](app/react) - Storybook for React components
-   [Storybook for react-native](app/react-native) - Storybook for React components

### Sub Projects

-   [CLI](lib/cli) - Streamlined installation for a variety of app types
-   [examples](examples) - Code examples to illustrate different Storybook use cases

### Addons

-   [storyshots](addons/storyshots) - Easy snapshot testing for storybook
-   [actions](addons/actions/) - Log actions as users interact with components in storybook
-   [links](addons/links/) - Create links between stories
-   [comments](addons/comments/) - Comment on storybook stories
-   [graphql](addons/graphql/) - Query a GraphQL server within Storybook stories
-   [info](addons/info/) - Annotate stories with extra component usage information
-   [knobs](addons/knobs/) - Interactively edit component prop data in the Storybook UI
-   [notes](addons/notes/) - Annotate storybook stories with notes
-   [options](addons/options/) - Customize the storybook UI in code

## Contributing

We welcome contributions to Storybook!

-   ⇄ Pull requests and ★ Stars are always welcome.
-   Read our [contributing guide](CONTRIBUTING.md) to get started.

### Development scripts

#### `npm run bootstrap`

> Installs package dependencies and links packages together - using lerna

#### `npm run publish`

> Push a release to git and npm
> will ask for version in interactive mode - using lerna.

#### `npm run lint`

> boolean check if code conforms to linting rules - uses remark & eslint

-   `npm run lint:js` - will check js
-   `npm run lint:md` - will check markdown + code samples

-   `npm run lint:js -- --fix` - will automatically fix js
-   `npm run lint:md -- -o` - will automatically fix markdown

#### `npm run test`

> boolean check if unit tests all pass - uses jest

-   `npm run test:watch` - will run tests in watch-mode
