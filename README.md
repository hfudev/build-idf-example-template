# Manually Trigger Build in GitHub Actions For ESP-IDF Examples

This is a github action template project to trigger a build in GitHub Actions for an ESP-IDF example project.

## Usage

Go to https://github.com/hfudev/build-idf-example-template, click the `Use this template` button to create a new repository based on this template.

Go to the new repository, click the `Actions` tab, then click the `build-idf-example-ad-hoc-yml` action.

![action](./docs/assets/action.png)

Click the `Run workflow` button, fill in the variables, then click the `Run workflow` button. (The variables should be self-explanatory.)

![variables](./docs/assets/variables.png)

After a short while, the build will be triggered, and the new build will be displayed.

![after](./docs/assets/after.png)

After the build is done, you may download the artifacts manually.

![done](./docs/assets/done.png)
