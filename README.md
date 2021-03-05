# try-storybook
 
## Get Started

A starter project created on 20210304, following [Storybook Get Started](https://storybook.js.org/docs/react/get-started/install).

```bash
npx sb init

npm run storybook
```

Fails due to `ERR! Error: Cannot find module 'react/package.json'`. Fixes with 

```bash
npm install --save-dev react react-dom
```

### Learnings and Observations
1. `.storybook/main.js`

This is where to define storybook files: 
```javascript
"stories": [
    "../stories/**/*.stories.mdx",
    "../stories/**/*.stories.@(js|jsx|ts|tsx)"
],
```

2. Powerful `Template.bind({})`

That's how a component of different variation is created:

```javascript
const Template = (args) => <Button {...args} />;

export const Primary = Template.bind({});
Primary.args = {
  primary: true,
  label: 'Button',
};

export const Secondary = Template.bind({});
Secondary.args = {
  label: 'Button',
};

```