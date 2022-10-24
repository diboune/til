### Tailwind and Stitches like variants

---

When looking for an alternative to [Stitches css](https://stitches.dev/) (after react 18 [made it hard](https://github.com/reactwg/react-18/discussions/110) for css-in-js libraries to work properly) and because everyone else is using/recommending [Tailwind](https://tailwindcss.com/), I found this: [classname-variants](https://github.com/fgnass/classname-variants), the best of both worlds!

This is how to create a component:

```jsx
import { styled } from "classname-variants/react";

const Button = styled("button", {
  variants: {
    size: {
      small: "text-xs",
      large: "text-base",
    },
  },
});
```

And this is how to use it

```jsx
const Index = () => {
  return (
    <div>
      <Button size="small">Hello Small World</Button>
      <Button size="large">Hello Large World</Button>
    </div>
  );
};
```

oh yeah and it's typesafe and work with the Tailwind CSS IntelliSense extension.
