<img align="right" src="https://avatars.githubusercontent.com/u/9919?s=64&v=4" />

# IAR Build Tools for Arm on GitHub Actions
[![IAR project on GitHub Actions](https://github.com/iarsystems/github-actions-ci-example/actions/workflows/arm.yml/badge.svg)](https://github.com/iarsystems/github-actions-ci-example/actions/workflows/arm.yml)

>[!WARNING]
>The information in this repository is subject to change without notice and does not constitute a commitment by IAR. While it serves as reference model for implementing Continuous Integration with IAR Tools, IAR assumes no responsibility for any errors, omissions, or specific implementations.

## Introduction
This repository provides a reasonably simple example to start with, alongside general guidelines on how a CI/CD pipeline can be set up on [GitHub Actions](https://docs.github.com/en/actions), using [GitHub-hosted runners](https://docs.github.com/en/actions/using-github-hosted-runners) to automatically build, test, and deploy a project with the [IAR Build Tools for Arm](https://www.iar.com/embedded-development-tools/embedded-ci-cd).

## Prerequisites
Before you begin, you will need:
- A CI Token for the IAR Build Tools[^1].
- A [GitHub Account](https://docs.github.com/en/get-started/learning-about-github/types-of-github-accounts).

In case you need an introduction on how to get started with GitHub, use [GitHub Quickstart](https://docs.github.com/en/get-started).

## Quickstart
1. [Fork](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo) or [Import](https://docs.github.com/en/migrations/importing-source-code/using-github-importer/importing-a-repository-with-github-importer) this repository.
2. Create a [__New repository secret__](https://docs.github.com/en/actions/security-for-github-actions/security-guides/using-secrets-in-github-actions) for GitHub Actions. __Name__ it `IAR_LMS_BEARER_TOKEN`, paste your CI Token under __Secret__ and click __Add secret__

![image](https://github.com/user-attachments/assets/250c84f0-803a-4ae5-8355-5b359991ea9a)

3. [Manually run the workflow](https://docs.github.com/en/actions/managing-workflow-runs-and-deployments/managing-workflow-runs/manually-running-a-workflow), or else trigger a new build by commiting and pushing changes to your repository.

![image](https://github.com/user-attachments/assets/d7f93618-e993-47ae-91b0-9fe9929f1038)

## GitHub Actions workflow example
On your repository, navigate to the [`.github/workflows/arm.yml`](.github/workflows/arm.yml) workflow file. This file uses the [GitHub-flavored YAML syntax](https://docs.github.com/en/actions/using-workflows/workflow-syntax-for-github-actions) to describe a pipeline containing multiple jobs found in a typical embedded firmware project. This entire pipeline runs in [IAR Cloud-ready Containers](https://github.com/iarsystems/containers).

## Summary
This repository provided an overview of how simple it is to get started with the IAR Build Tools on GitHub Actions. By harnessing the massive parallization possibilities these modern workflows provide, your development teams can converge efficiently while delivering results with higher quality and reproducibility.

[__` Follow us `__](https://github.com/iarsystems) on GitHub to get updates about examples like this and more.


## Issues
For technical support contact [IAR Customer Support][url-iar-customer-support].

For questions or suggestions related to this example: try the [wiki][url-repo-wiki] or check [earlier issues][url-repo-issue-old]. If those don't help, create a [new issue][url-repo-issue-new] with detailed information.

[^1]: The use of the IAR Build Tools is subject to the [IAR Software License Agreement](https://github.com/iarsystems/github-actions-ci-example/blob/master/LICENSE.md) and requires a valid subscription-based activation token for operation. If you are not yet a subscriber, please [contact us](https://iar.com/about/contact) for more information.

<!-- links -->
[url-iar-customer-support]: https://iar.my.site.com/mypages/s/contactsupport

[gh-yaml-doc-url]: https://docs.github.com/en/free-pro-team@latest/actions/reference/workflow-syntax-for-github-actions
[gh-shr-url]: https://docs.github.com/en/free-pro-team@latest/actions/hosting-your-own-runners/about-self-hosted-runners 
[gh-actions-url]: https://docs.github.com/en/actions
[gh-iar-url]: https://github.com/iarsystems

[url-repo]: https://github.com/iarsystems/github-actions-ci-example
[url-repo-wiki]: https://github.com/iarsystems/github-actions-ci-example/wiki
[url-repo-issue-new]: https://github.com/iarsystems/github-actions-ci-example/issues/new
[url-repo-issue-old]: https://github.com/iarsystems/github-actions-ci-example/issues?q=is%3Aissue%20state%3Aopen%20OR%20state%3Aclosed

