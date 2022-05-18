# Videoreach

## Product Description (TBD)

This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app) and [Minimals](https://minimals.css) as the design component library.

## Developing

The development branch is **_develop_**. This is the branch that all pull requests should be made against. This is also the branch which should be the root branch for all new development.
To develop locally:

1. Create a new branch:

   ```bash
   git checkout -b MY_BRANCH_NAME
   ```

2. Install the dependencies with:

   ```bash
   npm install
   ```

3. Start developing and watch for code changes:

   ```bash
   npm run dev
   ```

Check out the [contribution](CONTRIBUTING.md) and [code](CODE_GUIDELINES.md) guidelines for more information.

## Testing

If you are fixing a bug or adding code that should be tested, add tests! Below rules are followed for testing:

1. Jest + RTL ([React Testing Library](https://testing-library.com/docs/react-testing-library/intro/)) is being used for writing unit and integration test.
2. Write test cases for behavorial testing.
3. Write component level unit test cases and page level integration tests.
4. Code coverage threshold is as below:
   - lines - 95%
   - statements - 95%
   - branch - 90%
   - functions - 100%
5. Regression test suite should be created and updated (as required).
6. Regression test suite should be executed before every prod release. (good to have)

All new test suites should be written in TypeScript either .ts (or .tsx for unit tests). This will help ensure we catch smaller issues in tests that could cause flakey or incorrect tests.

If a test suite already exists that relates closely to the item being tested (e.g. homepage text content changes) the new checks can be added in the existing test suite.

## Building

You can build the project, including all type definitions, with:

```bash
npm run build
```

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!
