# Code guidelines

Please develop according to the below guidelines:

- Only `.tsx/.ts` files. No `.jsx/.js` files are allowed.
- Use `.scss` files for styling.
- Use descriptive function/variable naming.
- Always try to create reusable components as much as possible.
- Code should have the following order:-
  - Declaration of hooks
  - Custom functions
  - Logic
  - JSX/DOM rendering
- Always try to destroy async executing code from useEffects.
- Always use i18n variables / constants / enums for string instead of hardcoding.
- Include documentation for all complex functions, wherever required.
- No URLs should be maintained inside individual component.
- All the HTML paths should be defined in [src/routes/paths.ts](./src/routes/paths.ts) file and then imported.
- Create ENUM's wherever possible.
- Try to minimize repeated TS interfaces/types (use TS inbuilt functions / properties).
- I18n should be implemented and used.
- The code should conform to AA a11y (Internal understanding).
