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

- [x] Adding UI and UX changes, moving the content and search functionality to the new documentation engine.

  - [x] Implementing UI and UX changes in the documentation engine like creating components, templates, standalone pages, etc.

    > Created the new components, templates, standalone pages, etc for the documentation engine. I had refactored the default components and templates of the Docusaurus site which were added when the Docusaurus site was initialized.

    > Above task is done and I have pushed the changes directly to the repository. Commit can be found here [https://github.com/keptn-sandbox/new-keptn-docs-engine/commit/b749bbdfebfeaa41c789cd4c91ac29032ac1bbfa](https://github.com/keptn-sandbox/new-keptn-docs-engine/commit/b749bbdfebfeaa41c789cd4c91ac29032ac1bbfa).

    > After getting feedback from mentors on the new documentation engine, I have refactored the documentation engine. PR can be found here [https://github.com/keptn-sandbox/new-keptn-docs-engine/pull/9](https://github.com/keptn-sandbox/new-keptn-docs-engine/pull/9).

  - [x] Finalizing the things that need to be copied from the current documentation engine to the new documentation engine with proper structure.

  - [x] Copying content from the current documentation engine to the new documentation engine which has been finalized.

    > As of now not all contents are copied from the current documentation engine to the new documentation engine instead, some documents are copied to the new documentation engine.

  - [x] Adding documentation search functionality.

    > As of now I have added local search support using a [docusaurus-lunr-search](https://github.com/praveenn77/docusaurus-lunr-search) local search plugin but in the future, we can update this to [Algolia DocSearch](https://docsearch.algolia.com/).

    > Adding Algolia DocSearch support to the documentation engine is not part of this proposal but it is a suggestion to add it in the future.

    > PR related to adding documentation search functionality can be found here [https://github.com/keptn-sandbox/new-keptn-docs-engine/pull/11](https://github.com/keptn-sandbox/new-keptn-docs-engine/pull/11).

Issue link: [https://github.com/keptn-sandbox/new-keptn-docs-engine/issues/5](https://github.com/keptn-sandbox/new-keptn-docs-engine/issues/5)

---

- [x] Adding Versioning of docs support feature.

In current docs, we don't have versioning of docs support feature. As of now, we were versioning the docs manually. To solve this problem we have added versioning of the docs support feature using Docusaurus. We can use the versioning CLI to create a new documentation version based on the latest content in the `docs` directory. That specific set of documentation will then be preserved and accessible even as the documentation in the `docs` directory continues to evolve.

> PR related to adding versioning support can be found here [https://github.com/keptn-sandbox/new-keptn-docs-engine/pull/10](https://github.com/keptn-sandbox/new-keptn-docs-engine/pull/10).

---

- [ ] Adding Multiple repository docs support feature.

Some reasons why we want the Multiple repository docs support feature:

- Keptn CLI docs are generated using the `keptn generate docs` command. As of now, we run it in GitHub action [here](https://github.com/keptn/keptn.github.io/blob/9c649b434c9081028e0cc3535c9fa3a4217941fb/.github/workflows/auto-update.yml#L72) to populate our docs repo with CLI docs.
- If we look at the architecture doc [here](https://keptn.sh/docs/concepts/architecture/), the Keptn control plan consists of multiple services which have their READMEs in the main Keptn repository ([example](https://github.com/keptn/keptn/tree/master/jmeter-service)). Just look for any directory with `service` in [https://github.com/keptn/keptn](https://github.com/keptn/keptn), we can see individual READMEs for all such services. It's a good idea to move these READMEs to the docs site because the people who develop and maintain these services are responsible for updating the READMEs. Having them in a single place just makes it easier to update the READMEs and read them later as well.
- We also have services that extend the control plane which sits in a separate repository. Check [dynatrace-service](https://github.com/keptn-contrib/dynatrace-service) for example. As of now, if we add a new service that extends the control plane, we also have to add some documentation around it manually in the main docs repository.
- We have a miscellaneous repository like [Keptn spec](https://github.com/keptn/spec), documentation around what different values mean in the Keptn helm chart which we can't put in the main docs repository because they serve a different purpose.

  - [x] Adding Docusaurus Multi-instance support.

    > PR related to adding Docusaurus Multi-instance support can be found here [https://github.com/keptn-sandbox/new-keptn-docs-engine/pull/12](https://github.com/keptn-sandbox/new-keptn-docs-engine/pull/12).

  - [ ] Adding GitHub Action that can pull the docs from multiple repositories.

  > We want a GitHub Action which can pull the docs from [https://github.com/keptn/keptn.github.io](https://github.com/keptn/keptn.github.io) to [https://github.com/keptn-sandbox/new-keptn-docs-engine](https://github.com/keptn-sandbox/new-keptn-docs-engine) repository and organize the docs accordingly.

**NOTE:** Multiple repository docs support feature is not yet implemented completely and it is still in progress. As of now `Docs Multi-instance` support is added which is a`@docusaurus/plugin-content-docs` plugin. Adding GitHub Action which can pull the docs from multiple repositories is not yet implemented.

---

#### Phase 2

> **Week 7 - Week 12 (July 26 - September 5, 2022)**

---

- [x] Integrating [Lighthouse](https://developers.google.com/web/tools/lighthouse) CI.

Every webpage that is crawled by a search engine is evaluated with a score from 5 categories: Performance, Accessibility, Best Practices, SEO, and PWA. This is given a score between 0 – 100. The better your lighthouse score will affect how high up your webpage will appear on a search engine.

With a high score, your site meets the best practices and SEO standards outlined by Google in terms of performance and accessibility. Lighthouse is an important tool because it can identify common problems that affect the quality of your websites and propose solutions for them.

Lighthouse CI is a suite of tools that make continuously running, saving, retrieving, and asserting against [Lighthouse](https://github.com/GoogleChrome/lighthouse) results as easily as possible. So we have integrated Lighthouse CI GitHub Action into the new documentation engine.

> PR related to adding Lighthouse CI can be found here [https://github.com/keptn-sandbox/new-keptn-docs-engine/pull/17](https://github.com/keptn-sandbox/new-keptn-docs-engine/pull/17).

Issue link: [https://github.com/keptn-sandbox/new-keptn-docs-engine/issues/16](https://github.com/keptn-sandbox/new-keptn-docs-engine/issues/16)

---

- [x] Adding [Vale](https://github.com/errata-ai/vale) linter for doc quality checks.

To solve problems related to the styling of documentation, linting, doc quality checks, etc we wanted some tool to achieve these things.

We research and found [proselint](https://github.com/amperser/proselint) and [Vale](https://github.com/errata-ai) which can full fill our needs. After going through both we feel Vale has a lot of features as compared to `proselint` and is widely used in many popular open source organizations.

So, we integrated [vale-action](https://github.com/errata-ai/vale-action) in the new documentation engine.

Also, for the time being, I have adopted the [Google Style Guide](https://google.github.io/styleguide/) because my main motivation is to integrate the Vale GitHub Action into the docs engine. Yeah, I think we can have a separate discussion about which style guide to follow or we can have our custom style guide as well.

One of the limitations of Vale is that we have to update things in `vocab.txt` which is required for false positives. Some keywords, and names (e.g. `Keptn`, `KEP` etc) are considered as `vale.Spelling` errors, so we have to add them inside `vocab.txt` file. We can list all unique words which are considered errors in `vocab.txt` using the below command.

```shell
yarn run lint:docs | grep -o "'[a-z A-Z]*'" | grep -o "[a-z A-Z]*" | sort | uniq > .github/styles/vocab.txt
```

Now we have to manually validate all words listed in `vocab.txt`, discard which are invalid and correct them in the file where they were located.

Now we have to manually validate all words listed in `vocab.txt`, discard which are invalid and correct them in the file where they were located.

> PR related to adding Vale linter can be found here [https://github.com/keptn-sandbox/new-keptn-docs-engine/issues/19](https://github.com/keptn-sandbox/new-keptn-docs-engine/issues/19)

Issue link: [https://github.com/keptn-sandbox/new-keptn-docs-engine/issues/19](https://github.com/keptn-sandbox/new-keptn-docs-engine/issues/19)

---

- [x] Adding [Prettier](https://prettier.io/) GitHub Action support to format docs.

[Prettier](https://prettier.io/) is a very popular code formatter that uses very opinionated but sensible styles to format your code and prevent ongoing debates about code styles. So we wanted a GitHub action to automatically format your code using Prettier.

To set up the GitHub action, all we need to do is install our dependencies (e.g. `yarn install`), run our format script (e.g. `yarn format`), and then commit any changes if necessary.

By utilizing Prettier with GitHub Actions, we can ensure that our code is formatted consistently and without any issues.
It also helps to reduce manual work when formatting code.

> PR related to adding Prettier GitHub Action can be found here [https://github.com/keptn-sandbox/new-keptn-docs-engine/pull/25](https://github.com/keptn-sandbox/new-keptn-docs-engine/pull/25)

Issue link: [https://github.com/keptn-sandbox/new-keptn-docs-engine/issues/23](https://github.com/keptn-sandbox/new-keptn-docs-engine/issues/23)

---

- [ ] Adding GitHub Action to check broken links, spelling mistakes, check code style, etc.

---

- [ ] Finalizing the project deliverables and refactoring the code if any, based on the feedback.
- [ ] Making the project report and requesting mentors to review the project report.
- [ ] Finalizing and submitting the project report and other related documents.

---

#### Miscleaneous Phase

- Adding internationalization ([i18n](https://en.wikipedia.org/wiki/Internationalization_and_localization)) support. A possible translation strategy is to version control the translation files with Git (or any other VCS).

  > Discussion on this is done [here](https://keptn.slack.com/archives/C017T4KUAG3/p1657235519862879) and we have put this on lower priority.

- Implementing all SEO approaches listed in [https://docusaurus.io/docs/seo](https://docusaurus.io/docs/seo) like adding metadata in site configuration, adding metadata for all single pages, adding metadata in the front matter of all markdown files, etc.

  > This will take some time to implement as we will be adding metadata in the front matter of all files and will be implementing slowly as we still moving the content to the new documentation engine.
