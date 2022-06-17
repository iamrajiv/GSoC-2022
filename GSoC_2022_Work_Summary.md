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

Subtask

> **Week 1 - Week 6 (June 13 - July 25, 2022)**

- [x] Initialization of the documentation engine based on Docusaurus from scratch.

  - [x] Initialise the new Docusaurus site using `npx create-docusaurus@latest new-keptn-docs-engine classic` command and push the changes to [keptn-sandbox/new-keptn-docs-engine](https://github.com/keptn-sandbox/new-keptn-docs-engine).

  > Above task is done and I have pushed the changes directly to the repository.

- [x] Adding as basic documentation on how to use Docusaurus and what configuration of Docusaurus we are following like Project structure, Templates, etc.

  > I used the `npx create-docusaurus@latest new-keptn-docs-engine classic` command to create the new Docusaurus site so in this case, I used the `classic` template. Docusaurus recommend the `classic` template so that we can get started quickly, and it contains features found in Docusaurus 1. The `classic` template contains `@docusaurus/preset-classic` which includes standard documentation, a blog, custom pages, and a CSS framework (with dark mode support). We can get up and running extremely quickly with the classic template and customize things later on when you have gained more familiarity with Docusaurus. We can also use the template's TypeScript variant by passing the `--typescript` flag. See [TypeScript support](https://docusaurus.io/docs/typescript-support) for more information.

- [ ] Deploying the new Docusaurus site engine to Netlify.

- [ ] Adding `CONTRIBUTING.md` file with content related to how to add contents in Docusaurus and how to use it concerning Keptn. Also, this work will go on since we will be adding more content in the future according to documentation needs.

- [ ] Making a list of things that need to move from the current documentation engine to the new documentation engine with proper structure.
- [ ] Implementing UI and UX changes that have been discussed in the community bonding period.
- [ ] Creating standalone pages for `Why Keptn`, `Docs`, `Community`, `Resources`, `Tutorials`, `Integrations`, etc in the Docusaurus engine.
- [ ] Adding documentation search functionality to the documentation engine with [Algolia DocSearch](https://docsearch.algolia.com/) integration.
- [ ] Adding Versioning of docs support feature.
- [ ] Adding Multiple repository docs support feature.
- [ ] Moving content from the current doc site to the new doc site.
- [ ] Adding internationalization ([i18n](https://en.wikipedia.org/wiki/Internationalization_and_localization)) support. A possible translation strategy is to version control the translation files with Git (or any other VCS).
- [ ] Implementing all SEO approaches listed in [https://docusaurus.io/docs/seo](https://docusaurus.io/docs/seo) like adding metadata in site configuration, adding metadata for all single pages, adding metadata in the front matter of all markdown files, etc.

#### Phase 2

> **Week 7 - Week 12 (July 26 - September 5, 2022)**

- [ ] Adding [Vale](https://github.com/errata-ai/vale) linter or equivalent linter for doc quality checks.
- [ ] Adding [Prettier](https://prettier.io/) GitHub Action support to format markdown docs whenever there is a pull request or push towards the `master` branch.
- [ ] Adding other GitHub Action to check broken links, spelling mistakes, check code style, etc.
- [ ] Adding GitHub workflows for continuous deployment of the website to GitHub Pages, Netlify, Vercel, etc.
- [ ] Implementing previews for the website and support for staging changes (e.g. pre-release documentation).
- [ ] Integrating [Lighthouse](https://developers.google.com/web/tools/lighthouse) in the docs engine to check the quality of the documentation. We will be able to audit the performance, accessibility, SEO, etc of the doc site.
- [ ] Finalizing the project deliverables and refactoring the code if any, based on the feedback.
- [ ] Making the project report and requesting mentors to review the project report.
- [ ] Finalizing and submitting the project report and other related documents.
