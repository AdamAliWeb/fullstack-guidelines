# TypeScript

## References

- **[TypeScript Documentation](https://www.typescriptlang.org/docs/)**

## Tools

- **[QuickType](https://app.quicktype.io/)**: This is a tool that helps apply types or interfaces to API responses

## Tips & Tricks

1. You cannot use `name` as a variable name since it is a global variable (`window.name`) and a protected property.

2. To declare a variable without type inference, you can use `any`, but it disables type checking and causes you to lose **TypeScript**'s features for that variable. Prefer using `unknown` instead.
