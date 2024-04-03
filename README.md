# rn-constyle

Effortlessly create, combine, and manage React Native styles using shorthand properties and helpful utility functions.

## Installation

Install the package using `npm` or `yarn`:

```bash
npm install @ilz5753/rn-constyle
```

```bash
yarn add @ilz5753/rn-constyle
```

## Usage

To use `@ilz5753/rn-constyle`, import `getStyle`, individual style functions, or the entire package in your React Native component file:

```ts
import {
  getStyle,
  f1,
  center,
  fontSize,
  color,
  backgroundColor,
  isAndroid,
  rtlComparer,
  fw,
} from "@ilz5753/rn-constyle";

const Example = () => {
  return (
    <View style={[f1, center, backgroundColor("#fffff0")]}>
      <Text style={[fontSize(isAndroid ? 27 : 24), color("brown")]}>
        Hello world
      </Text>
    </View>
  );
};
const flexDirection = rtlComparer(getStyle(["fdr"]), getStyle(["fdrr"]));
const isRTL = true;
const RTLExample = () => {
  return (
    <View style={[fw, flexDirection(isRTL), getStyle(["aic", "jcse"])]}>
      <Text>1</Text>
      <Text>2</Text>
      <Text>3</Text>
    </View>
  );
};
```

## License

this package licensed under the [MIT License](/LICENSE).

## Contribution

Feel free to contribute by submitting issues or pull requests on the [GitHub repository](.).
