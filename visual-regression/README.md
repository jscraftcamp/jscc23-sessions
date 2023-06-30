# Visual regression testing with Storybook and cypress

**Session by Pavlo**

In this session on visual regression testing with Storybook and Cypress, we explored various aspects related to this testing approach. Here's a summary of the key points discussed:

* Cypress integration with Storybook was highlighted as the testing framework for visual regression testing.
* The presence of a UX team that frequently changes styles, including features like dark mode, was emphasized.
* Continuous Integration (CI) was set up to run visual regression tests, with parallel execution on 12 machines taking around 17 minutes. This time was reduced to 5 minutes using the NX framework.
* Snapshots were taken for different devices (desktop, iPhone, iPad) and multiple languages (English, German).
* Images were committed with git lsf to ensure consistency.
* Ensuring that the same docker image was used locally and in CI helped maintain consistent screenshots, as styling can differ between Mac and Linux.
* Different thresholds, such as pixels, viewport, and whole page, were employed to determine visual differences.
* Initially, focus was on components in different states, with snapshot integration tests being performed.
* The NX setup was implemented to facilitate the visual regression testing process.
* A decision was made to prioritize testing the most important pages and components that are frequently used.
* Visual regression testing proved effective in uncovering invisible bugs that could have been overlooked during component refactoring.
* The workflow involved developing new components in Storybook and generating snapshots once they were completed.
* Cypress was used to open Storybook and perform cypress image snapshots, aiding in the review process by highlighting styling changes.
* Reviewing all the snapshots can be challenging when there are significant style changes.
* E2E tests did not include screenshots due to dynamic text changes
* It was suggested that Cypress components could potentially replace Storybook, leading to faster testing.