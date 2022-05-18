# How to Contribute

Are you a developer working on a new feature or fixing a bug? There are a few things that you need to know before making any changes.

## Design Principle

[Atomic design](https://atomicdesign.bradfrost.com/) guidelines are being followed for development. If you are new to Atomic design or design systems, go through the below resources to have a overview:

- [Atomic Design by Brad Frost](https://atomicdesign.bradfrost.com/)
- [Atomic Design Principles & Methodology 101](https://xd.adobe.com/ideas/process/ui-design/atomic-design-principles-methodology-101/)
- [The guide to Atomic Design](https://www.justinmind.com/blog/atomic-design/)

Once you are acquainted with Atomic design, have a look at the [code structure](#code-structure) to understand how above prinicples are implemented in our code base.

## Code Structure

Any changes made should follow the below design structure. Add code and files in their respective place. Any deviation will result in PR getting rejected.

- [**assets**](assets) - All static assets go here (e.g. logo, images, svg, font-files, etc)
- [**components**](components) - relates to **Atoms & Molecules** hierarchy from Atmoic designs, all reusable components go here
  - [**Minimal**](components/Minimal) - design components provided by Minimal (Don't add custom code here)
- [**contexts**](contexts) - all context code (store, action, reducer) goes here
- [**hooks**](hooks) - custom hooks
  - [**Minimals**](hoooks/Minimals) - custom hooks provided by Minimal (Don't add custom code here)
- [**layouts**](layouts) - code related to page layout goes here
- [**pages**](pages) - next js pages folder, all the UI pages go here, relates to **page** hierarchy in Atomic design
- [**routes**](routes) - all the html routes used goes here
- [**sections**](sections) - relates to **organism** hierarchy in Atomic design
  - _<page_name>_ - all the block level sections for a particular page go inside this
- [**styles**](styles) - all global level style will go here (global style + variables + style utilities)
- [**tests**](tests) - page level tests will go here
  - _<page_name>.test.tsx_ - e.g. home.test.tsx
- [**theme**](theme) - theming provided by Minimals
  - [**overrides**](theme/overrides) - overrides Mui default themes
- [**translations**](translations) - Static text translations go here
  - _<lang_id>.tsx_ - e.g. en.tsx, fr.tsx
- [**utils**](utils)
  - [**Minimals**](utils/Minimals) - Utils provided by Minimals (Dont add custom code here)
  - [_utils_group_] - Group utils according to their usage / functionality

## Semantic Versioning

Videoreach follows semantic versioning. We release patch versions for critical bugfixes, minor versions for new features or non-essential changes, and major versions for any milestone changes.

Every significant change is documented in [changelog file](CHANGELOG.md).

## Branch Organization

- **main - production branch**
- **develop - development branch**
- **version-x - stable version release**

Submit all changes to the [develop branch](https://github.com/HealthiPeoples/videoreach-clinician/tree/main). We don't directly push changes to main branch.

Code that lands in **_develop_** must be stable and should be passing all test cases with required coverage thresholds. We should be able to create a pull request from the tip of **_develop_** to **_main_** at any time.

After signoff is given for development branch and a new production release is to be deployed, a PR should be raised from **_develop_** to **_main_**. With every production deployment, a new version is created as a new branch named **version-_x_** where **_x_** represents the new version number.

## Bugs

Create a new issue in [GitHub issues](https://github.com/HealthiPeoples/videoreach-clinician/issues) and inform one of the lead developer. Post validation of bug, a new bug will be raised in Monday.com board post which development will start to fix it.

## Git Flow

We are using git hooks with husky to ensure git conventions are followed and safe code is being pushed for merge.
All code changes should go through manual review. **No code changes will be merged without reviewer approval.**

### Branch name

For any code changes, create a new branch from develop following the below branch name convention:
`(feature|bug|tech|hotfix)` followed by `/{story/task#}-` and then a short description.
e.g. - `feature/00-initial-setup`

### Commit Message

For any commit message, it should follow the syntax `[{story/task#}]` followed by actual message.
e.g. - `[0] hello world`
Before any commit, pre-commit hook will execute which will check branch naming and commit message convention are being followed as well as no lint errors are present.

### Push

Before code is pushed to origin, husky will execute ensuring all test cases are being passed, code coverage thresholds are met and build is executing properly.
If any of the above conditions are not met, push will be failed.

### Skip git hooks

**NEVER** skip git hooks.

## Sending a Pull Request

Ensure you are following all the [contribution](CONTRIBUTING.md) and [code](CODE_GUIDELINES.md) guidelines.

**Before submitting a pull request**, please make sure the following is done:

1. Get the latest pull from **_develop_** branch so as to avoid any merge conflicts.
2. Run `npm install` in the root repository.
3. If you’ve fixed a bug or added code that should be tested, add tests!
4. Run `npm run test` in the root repositry and ensure all test suites pass.
5. Format your code with prettier (`npm run prettier`).
6. Ensure your code lints (`npm run lint`).
7. Make sure to commit and push as per the guidelines.
8. Make sure to assign a reviewer from the list of [authors](AUTHORS).
