# eslint - prettier

[how to get started](https://eslint.org/docs/latest/use/getting-started)
[this is the new form of preparing ESLint](https://dev.to/rgolawski/how-to-make-eslint-and-prettier-work-together-2i5g)

First we create our Vite project

using this command (we need to have a package.json already in our project):

```

npm init @eslint/config@latest

# or

yarn create @eslint/config

# or

pnpm create @eslint/config@latest

```

We'll receive some prompts by the cli, choose this configuration:
![alt text](src/assets/https___dev-to-uploads.s3.amazonaws.com_uploads_articles_mfaki8dmc0n6kt2r6fnj.avif)

we install all the dependencies needed for working with eslint.


---

The next dependencies needed are the "Prettier ones":

```$

npm install -D eslint-plugin-prettier eslint-config-prettier
npm install -D prettier

```

Now if we are using the new configuration (eslint.config.js), we should add this to the configuration file at the beginning to make use of the prettier functionalities:

```javascript
import eslintPluginPrettierRecommended from 'eslint-plugin-prettier/recommended';

export default [
  // any other config imports go at the top
  eslintPluginPrettierRecommended
]
```

Otherwise, if we are using an older version (.eslintrc), we should add: 

```javascript
{
  "extends": ["plugin:prettier/recommended"]
}
```

