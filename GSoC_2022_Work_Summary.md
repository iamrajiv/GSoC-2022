<div align="center">
<img src="assets/gsoc-2022-1.svg" height="auto" width="600" />
<br />
<img src="assets/gsoc-2022-2.svg" height= "auto" width="400" />
<br />
<h1>Keptn</h1>
<h3>
New Documentation Site Engine
<br />
Work Summary
</h3>
</div>

## Table of Contents

- [Phase 1](#phase-1)
- [Phase 2](#phase-2)
- [Miscellaneous Phase](#miscellaneous-phase)

I have divided the Development Phase into two phases i.e. `Phase 1` and `Phase 2`.

> `Phase 1` will deal mostly with implementing core features and functionality needed in the documentation engine.

> `Phase 2` will deal mostly with implementing miscellaneous features and functionality of the documentation engine like Continuous Integration, Continuous Deployment, etc.

#### Phase 1

> **Week 1 - Week 6 (June 13 - July 25, 2022)**

---

- [x] Initialization and deployment of the documentation engine based on Docusaurus from scratch.

  - [x] Initialised the new Docusaurus site using `npx create-docusaurus@latest new-keptn-docs-engine classic` command and push the changes to [keptn-sandbox/new-keptn-docs-engine](https://github.com/keptn-sandbox/new-keptn-docs-engine).

    > Above task is done and I have pushed the changes directly to the repository. Commit can be found here [https://github.com/keptn-sandbox/new-keptn-docs-engine/commit/e2f2202b01894806e1d9e924d97abb2b98b2d8d1](https://github.com/keptn-sandbox/new-keptn-docs-engine/commit/e2f2202b01894806e1d9e924d97abb2b98b2d8d1).

  - [x] Adding as basic documentation on how to use Docusaurus and what configuration of Docusaurus we are following like Project structure, Templates, etc.

    > I used the `npx create-docusaurus@latest new-keptn-docs-engine classic` command to create the new Docusaurus site so in this case, I used the `classic` template. Docusaurus recommend the `classic` template so that we can get started quickly, and it contains features found in Docusaurus 1. The `classic` template contains `@docusaurus/preset-classic` which includes standard documentation, a blog, custom pages, and a CSS framework (with dark mode support). We can get up and running extremely quickly with the classic template and customize things later on when you have gained more familiarity with Docusaurus. We can also use the template's TypeScript variant by passing the `--typescript` flag. See [TypeScript support](https://docusaurus.io/docs/typescript-support) for more information.

  - [x] Deploying the new Docusaurus site engine to Netlify.

    > [https://github.com/keptn-sandbox/new-keptn-docs-engine](https://github.com/keptn-sandbox/new-keptn-docs-engine) has been deployed to Netlify at [https://keptn-experimental-docs-site.netlify.app/](https://keptn-experimental-docs-site.netlify.app/).

  - [x] Adding `CONTRIBUTING.md` file with content related to how to add contents in Docusaurus and how to use it concerning Keptn. Also, this work will go on since we will be adding more content in the future according to documentation needs.

    > PR related to adding `CONTRIBUTING.md` file is [https://github.com/keptn-sandbox/new-keptn-docs-engine/pull/4](https://github.com/keptn-sandbox/new-keptn-docs-engine/pull/4).

Issue link: [https://github.com/keptn-sandbox/new-keptn-docs-engine/issues/2](https://github.com/keptn-sandbox/new-keptn-docs-engine/issues/2)

---

- [ ] Adding UI and UX changes, moving the content and search functionality to the new documentation site engine.

  - [x] Implementing UI and UX changes in the documentation engine like creating components, templates, standalone pages, etc.

    > Created the new components, templates, standalone pages, etc for the documentation engine. I had refactored the default components and templates of the Docusaurus site which were added when the Docusaurus site was initialized.

    > Above task is done and I have pushed the changes directly to the repository. Commit can be found here [https://github.com/keptn-sandbox/new-keptn-docs-engine/commit/b749bbdfebfeaa41c789cd4c91ac29032ac1bbfa](https://github.com/keptn-sandbox/new-keptn-docs-engine/commit/b749bbdfebfeaa41c789cd4c91ac29032ac1bbfa).

    > After getting feedback from mentors on the new documentation site engine, I have refactored the documentation engine. PR can be found here [https://github.com/keptn-sandbox/new-keptn-docs-engine/pull/9](https://github.com/keptn-sandbox/new-keptn-docs-engine/pull/9).

    > The UI and UX change that I mentioned above are according to the Docusaurus site. When we initialize the Docusarus site, it comes with some default components, templates, etc. I have refactored the default components and templates of the Docusaurus site which were added when the Docusaurus site was initialized. I have also added some new components, templates, etc. which are required for the new documentation site engine. But the new components, templates, etc. which I have added are just the basic ones. As of now, we have not decided on the proper structure and looks of the new documentation site engine i.e. how the pages will look like and which content will be put where, etc. I have mentioned this work in the [Future Work to be done](#future-work-to-be-done) section.

  - [x] Finalizing the things that need to be copied from the current documentation engine to the new documentation site engine with proper structure.

  - [ ] Copying content from the current documentation engine to the new documentation site engine which has been finalized.

    > As of now not all contents are copied from the current documentation engine to the new documentation site engine instead, some documents are copied to the new documentation site engine. The reason for not moving all content from the current documentation engine to the new documentation site engine is that we are still working on the features and structure of the new documentation site engine.

  - [x] Adding documentation search functionality.

    > As of now I have added local search support using a [docusaurus-lunr-search](https://github.com/praveenn77/docusaurus-lunr-search) local search plugin but in the future, we can update this to [Algolia DocSearch](https://docsearch.algolia.com/).

    > Adding Algolia DocSearch support to the documentation engine is not part of this proposal but it is a suggestion to add it in the future.

    > PR related to adding documentation search functionality can be found here [https://github.com/keptn-sandbox/new-keptn-docs-engine/pull/11](https://github.com/keptn-sandbox/new-keptn-docs-engine/pull/11).

Issue link: [https://github.com/keptn-sandbox/new-keptn-docs-engine/issues/5](https://github.com/keptn-sandbox/new-keptn-docs-engine/issues/5)

---

- [x] Adding Versioning of docs support feature.

In current docs, we don't have versioning of docs support feature. As of now, we were versioning the docs manually. To solve this problem we have added versioning of the docs support feature using Docusaurus. We can use the versioning CLI to create a new documentation version based on the latest content in the `docs` directory. That specific set of documentation will then be preserved and accessible even as the documentation in the `docs` directory continues to evolve.
Here versioning CLI means running the commands which create versions of documentation like running the command `yarn run docusaurus docs:version 1.1.0` will create a new version of the documentation with the version number `1.1.0` and the content of the `docs` directory at the time of running the command will be copied to the new versioned documentation directory.

> PR related to adding versioning support can be found here [https://github.com/keptn-sandbox/new-keptn-docs-engine/pull/10](https://github.com/keptn-sandbox/new-keptn-docs-engine/pull/10).

---

- [ ] Adding Multiple repository docs support feature.

This feature is partially done and we want more clarity on this feature. Earlier we thought adding Docusaurus Multi-instance support will solve this problem but it is not the case. The thing is using Docusaurus Multi-instance we can have multiple `docs` folders in the same Docusaurus site and for every `docs` folder, we can put our documentation accordingly. But we wanted something automatic stuff so that we can pull docs from other repository and organize it in these `docs` folder instances.

I got clarity about this feature a little late so I was not able to implement this feature completely.

Some reasons why we want the Multiple repository docs support feature:

For the current documentation site engine, we generate docs using the Keptn CLI
The source for the Keptn CLI reference pages is moved from the software repository to the docs repository as a batch process (using the `keptn generate docs` command).

But that doesn't actually generate the docs -- it just copies the source for those pages to the doc repo and then the pages are generated each time the docs are rebuilt. For example, for the 0.18.x release, the source for the CLI reference pages is in https://github.com/keptn/keptn.github.io/tree/master/content/docs/0.18.x/reference/cli/commands and one can go in and modify those pages and instantly change what is built for the doc site. Of course, those changes get overwritten the next time we pull the source from keptn/keptn so we shouldn't be modifying it.

- The source for the Keptn CLI reference pages is moved from the software repository to the docs repository as a batch job. As of now, we run it in GitHub action [here](https://github.com/keptn/keptn.github.io/blob/9c649b434c9081028e0cc3535c9fa3a4217941fb/.github/workflows/auto-update.yml#L72) to populate our docs repo with CLI docs. We must achieve at least this functionality under Docusaurus. Ideally, we would enhance it so that a change to the source in the software repository would immediately trigger a PR to the docs repository so that the docs are constantly up-to-date and batch processing for a new release is not required.
- If we look at the architecture doc [here](https://keptn.sh/docs/concepts/architecture/), the Keptn control plan consists of multiple services which have their READMEs in the main Keptn repository ([example](https://github.com/keptn/keptn/tree/master/jmeter-service)). Just look for any directory with `service` in [https://github.com/keptn/keptn](https://github.com/keptn/keptn), we can see individual READMEs for all such services. It's a good idea to move these READMEs to the docs site because the people who develop and maintain these services are responsible for updating the READMEs. Having them in a single place just makes it easier to update the READMEs and read them later as well. We have other files in the software repositories that should be imported to the documentation, such as the `values.yaml` files that configure Helm charts. We need to define all such entities and then devise schemes that allow us to author content in the software repository but build an integrated doc set with that content.
- We also have services that extend the control plane which sits in a separate repository. Check [dynatrace-service](https://github.com/keptn-contrib/dynatrace-service) for example. As of now, if we add a new service that extends the control plane, we also have to add some documentation around it manually in the main docs repository.
- We have a miscellaneous repository like [Keptn spec](https://github.com/keptn/spec), documentation around what different values mean in the Keptn helm chart which we can't put in the main docs repository because they serve a different purpose.

  - [x] Adding Docusaurus Multi-instance support.

    > PR related to adding Docusaurus Multi-instance support can be found here [https://github.com/keptn-sandbox/new-keptn-docs-engine/pull/12](https://github.com/keptn-sandbox/new-keptn-docs-engine/pull/12).

But Docusaurus Multi-instance support does not work as expected. The problem with multiple repository docs support was at starting I thought we only need `Docusaurus Multi-instance support` which is the same as hosting multiple docs in a single docusaurus project but after that, I got to know that in addition to `Docusaurus Multi-instance support` we need to pull docs from other repositories and organize it in new documentation site engine. But again I was not sure where to pull docs from whether I have to pull from [https://github.com/keptn/keptn.github.io](https://github.com/keptn/keptn.github.io) repository or multiple repositories and combine and organize all docs to new documentation site engine. I discussed this with my mentors and I got clarity on this. We got to know a lot of ways we can implement this feature.

Some ways we can implement this feature:

- Writing a GitHub Action which can pull the docs from [https://github.com/keptn/keptn.github.io](https://github.com/keptn/keptn.github.io) to [https://github.com/keptn-sandbox/new-keptn-docs-engine](https://github.com/keptn-sandbox/new-keptn-docs-engine) repository and organize the docs accordingly.

I thought of using Dependabot to regularly check new docs in the `keptn/keptn.github.io` repository and pull it to the `keptn-sandbox/new-keptn-docs-engine` repository. Also, I tried writing a simple GitHub Action script that pulls docs but it is not robust enough to pull docs from multiple repositories and organize them in the new documentation site engine.

```shell
shell
run: |
    git clone https://.:${{ secrets.GITHUB_TOKEN }}@github.com/project target
    rm everything but the .git directory
    copy source\files target
    cd target
    git add .
    git diff-index --quiet HEAD || git commit -m "Automatic publish from github.com/project"
    git push target master
```

So, I tried the different approaches around GitHub Action but I was not able to make robust GitHub Action that can pull docs from multiple repositories and organize them in the new documentation site engine. I created a discussion around it [here](https://keptn.slack.com/archives/C017T4KUAG3/p1659322635479589) but did not get much feedback from the community.

- Writing a GitHub Action with Keptn CLI and running it for multiple folders to populate the docs in the new documentation site engine. Something like this [https://github.com/keptn/keptn.github.io/blob/master/.github/workflows/auto-update.yml](https://github.com/keptn/keptn.github.io/blob/master/.github/workflows/auto-update.yml).

For the current documentation site engine, we generate docs using the Keptn CLI. So, I tried writing GitHub Action same as [this](https://github.com/keptn/keptn.github.io/blob/master/.github/workflows/auto-update.yml) but in addition to this, I would be running the `keptn generate docs` command for multiple folders. But this does not work as expected. The problem is the front matter template in [https://github.com/keptn/keptn/blob/master/cli/cmd/generate_docs.go](https://github.com/keptn/keptn/blob/master/cli/cmd/generate_docs.go) is coded according to the Hugo theme but we wanted frontmatter to be according to Docusaurus format.

Something like this:

```go
const gendocFrontmatterTemplate = `---
sidebar_position: %d
title: "%s"
description: "%s
keywords: "%s"
slug: "%s"
tags: "%s"
---
`
```

We wanted frontmatter like this because it enhances the SEO of docs. But to do this we had to update the go code in [https://github.com/keptn/keptn/blob/master/cli/cmd/generate_docs.go](https://github.com/keptn/keptn/blob/master/cli/cmd/generate_docs.go) file but that will break the current documentation generation process so had to drop this approach.

- Using [docusaurus-plugin-remote-content](https://github.com/rdilweb/docusaurus-plugin-remote-content)

Its Docusaurus plugin downloads content from remote sources. With this plugin, we can write the Markdown for our content somewhere else, and use them on your Docusaurus site, without copying and pasting. This is something I am working on currently and trying to combine with GitHub action too.

> Since the `Adding Multiple repository docs support feature` task was taking a lot of time so I moved to other work and I thought I will pick this up at last because this work needs a lot of time and research and I was not sure how to implement this feature.

**NOTE:** Multiple repository docs support feature is not yet implemented completely and it is still in progress. As of now `Docs Multi-instance` support is added which is a`@docusaurus/plugin-content-docs` plugin. Still, we want some custom GitHub Action or automation to pull docs from multiple repositories and organize them in a new documentation site engine.

---

#### Phase 2

> **Week 7 - Week 12 (July 26 - September 5, 2022)**

---

- [x] Integrating [Lighthouse](https://developers.google.com/web/tools/lighthouse) CI.

Every webpage that is crawled by a search engine is evaluated with a score from 5 categories: Performance, Accessibility, Best Practices, SEO, and PWA. This is given a score between 0 – 100. The better your lighthouse score will affect how high up your webpage will appear on a search engine.

With a high score, your site meets the best practices and SEO standards outlined by Google in terms of performance and accessibility. Lighthouse is an important tool because it can identify common problems that affect the quality of your websites and propose solutions for them. Currently, the standard search engines are tending to report ancient versions of the Keptn docs rather than the latest version so this type of problem can be identified and fixed with the help of Lighthouse CI.

Lighthouse CI is a suite of tools that make continuously running, saving, retrieving, and asserting against [Lighthouse](https://github.com/GoogleChrome/lighthouse) results as easily as possible. So we have integrated Lighthouse CI GitHub Action into the new documentation site engine.

> PR related to adding Lighthouse CI can be found here [https://github.com/keptn-sandbox/new-keptn-docs-engine/pull/17](https://github.com/keptn-sandbox/new-keptn-docs-engine/pull/17).

Issue link: [https://github.com/keptn-sandbox/new-keptn-docs-engine/issues/16](https://github.com/keptn-sandbox/new-keptn-docs-engine/issues/16)

---

- [x] Adding [Vale](https://github.com/errata-ai/vale) linter for doc quality checks.

To solve problems related to the styling of documentation, linting, doc quality checks, etc we wanted some tool to achieve these things.

We research and found [proselint](https://github.com/amperser/proselint) and [Vale](https://github.com/errata-ai) which can full fill our needs. After going through both we feel Vale has a lot of features as compared to `proselint` and is widely used in many popular open source organizations.

So, we integrated [vale-action](https://github.com/errata-ai/vale-action) in the new documentation site engine.

Also, for the time being, I have adopted the [Google Style Guide](https://google.github.io/styleguide/) because my main motivation is to integrate the Vale GitHub Action into the new documentation site engine. We can easily switch to another standard style guide or a custom style guide in the future.

One of the limitations of Vale is that we have to update things in `vocab.txt` which is required for false positives. Some keywords, and names (e.g. `Keptn`, `KEP` etc) that are not included in standard dictionaries and so would be treated as `vale.Spelling` errors, so we have to add them inside `vocab.txt` file.

Use the following command to list all unique words which are considered errors and write them to the `vocab.txt` file:

```shell
yarn run lint:docs | grep -o "'[a-z A-Z]*'" | grep -o "[a-z A-Z]*" | sort | uniq > .github/styles/vocab.txt
```

We must then edit that file to remove the genuine spelling errors and only leave the Keptn terms that should be recognized as proper words.

> PR related to adding Vale linter can be found here [https://github.com/keptn-sandbox/new-keptn-docs-engine/issues/19](https://github.com/keptn-sandbox/new-keptn-docs-engine/issues/19)

Issue link: [https://github.com/keptn-sandbox/new-keptn-docs-engine/issues/19](https://github.com/keptn-sandbox/new-keptn-docs-engine/issues/19)

---

- [x] Adding [Prettier](https://prettier.io/) GitHub Action support to format docs.

[Prettier](https://prettier.io/) is a very popular code formatter that uses very opinionated but sensible styles to format your code and prevent ongoing debates about code styles. So we wanted a GitHub action to automatically format your code using Prettier.

To set up the GitHub action, all we need to do is install our dependencies (e.g. `yarn install`), run our format script (e.g. `yarn format`), and then commit any changes if necessary.

By utilizing Prettier with GitHub Actions, we can ensure that our code is formatted consistently and without any issues.
It also helps to reduce manual work when formatting code. Currently, we are running prettier checks for `docs/**/*.{md,mdx}` files only.

> PR related to adding Prettier GitHub Action can be found here [https://github.com/keptn-sandbox/new-keptn-docs-engine/pull/25](https://github.com/keptn-sandbox/new-keptn-docs-engine/pull/25)

Issue link: [https://github.com/keptn-sandbox/new-keptn-docs-engine/issues/23](https://github.com/keptn-sandbox/new-keptn-docs-engine/issues/23)

---

- [x] Adding GitHub Action to check broken links in docs.

It is a GitHub Action that can be run on the docs to check for broken links and xrefs. The GitHub Action can create an issue on the repository with the broken links report, add labels to the issue and assign it to the relevant maintainers.

> PR related to adding GitHub Action to check broken links in docs can be found here [https://github.com/keptn-sandbox/new-keptn-docs-engine/pull/28](https://github.com/keptn-sandbox/new-keptn-docs-engine/pull/28)

Issue link: [https://github.com/keptn-sandbox/new-keptn-docs-engine/issues/27](https://github.com/keptn-sandbox/new-keptn-docs-engine/issues/27)

---

- [x] Finalizing the project deliverables and refactoring the code if any, based on the feedback.
- [x] Making the project report and requesting mentors to review the project report.
- [x] Finalizing and submitting the project report and other related documents.

---

#### Miscellaneous Phase

- Adding internationalization ([i18n](https://en.wikipedia.org/wiki/Internationalization_and_localization)) support. A possible translation strategy is to version control the translation files with Git (or any other VCS).

  > Discussion on this is done [here](https://keptn.slack.com/archives/C017T4KUAG3/p1657235519862879) and we have put this on lower priority.

- Implementing all SEO approaches listed in [https://docusaurus.io/docs/seo](https://docusaurus.io/docs/seo) like adding metadata in site configuration, adding metadata for all single pages, adding metadata in the front matter of all markdown files, etc.

  > This will take some time to implement as we will be adding metadata in the front matter of all files and will be implementing slowly as we still moving the content to the new documentation site engine.
  > Adding metadata will help in SEO like we can provide a better description of the page, a title for the page, keywords for the page, etc. If we don’t proper metadata then the search engine will not be able to understand what the page is about and will not be able to rank it properly.

<div align="right">
<img src="assets/gsoc-2022-3.svg" height="auto" width="100" />
</div>
