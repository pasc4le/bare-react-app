# bare-react-app
A simple react app template. `create-react-app` is meh. I've also added scss support by default, because I always use it.

## Install
Clone this repo, or use it as a template, and run `yarn`.

## Development
If you want to run your webapp in localhost, simply run 
```bash
yarn start
# or
npm run start
```

## Production
If you want to build this webapp, you can use `webpack` or:
```bash
yarn build
# or
npm run build
```

## Linting
If you want to check your lint errors with eslint, run `yarn lint`. To fix them you can use `yarn lint:fix`.

## Prettier
You can also format your files with prettier with `yarn format`.

## Styling
In your `index.scss` you'll find several useful things. I've added some "essential" css general styling and a way to generate CSS variables on the `:root` element from a scss map. This is useful if you want to add reactivity to those variables while still having the possibility to access the real and static ones with scss.
```scss
$variables: (
    "primary": (
        "100": "#ffdfa3",
        "500": "#FFA500",
        "900": "#b57c14",
    ),
    "secondary": "#6D0B29",
    ...
    "title-font": "'Calistoga', cursive",
    ...
);
```
The `$variables` map keys can be assigned to string or maps. The above map will generate a css file like the following:
```css
:root {
  ...
  --primary-100: "#ffdfa3",
  --primary-500: "#FFA500",
  --primary-900: "#b57c14",
  --secondary: "#6D0B29";
  --title-font: 'Calistoga', cursive;
  ...
}
```
