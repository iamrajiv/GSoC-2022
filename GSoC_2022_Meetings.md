<div align="center">
<img src="assets/gsoc-2022-1.svg" height="auto" width="600" />
<br />
<img src="assets/gsoc-2022-2.svg" height= "auto" width="400" />
<br />
<h1>Keptn</h1>
<h3>
New Documentation Site Engine
<br />
Meetings
</h3>
</div>

## 29th August 2022

- Attendees
  - Meg McRoberts
  - Moritz Wiesinger
  - Rajiv Ranjan Singh
  - Suraj Banakar
- A discussion was done on [keptn-sandbox#23](https://github.com/keptn-sandbox/new-keptn-docs-engine/issues/23) and also whether should we use auto-commit pipelines or not.
- We discussed how we can integrate Keptn CLI to the Docusaurus site.
- Suraj gave an overview about [https://github.com/rdilweb/docusaurus-plugin-remote-content](https://github.com/rdilweb/docusaurus-plugin-remote-content) and how we can use it to achieve multiple repository docs support.

## 18th August 2022

- Attendees
  - Meg McRoberts
  - Rajiv Ranjan Singh
  - Suraj Banakar
- Notes
  - Meg has reviewed [keptn-sandbox#20](https://github.com/keptn-sandbox/new-keptn-docs-engine/pull/20)
- Rajiv
  - We are using local search right now
  - We need to apply for the Algolia search engine (which takes 1 to 10 days according to Google)
  - TODO: Add expectations and comments around migrations in [keptn-sandbox#1](https://github.com/keptn-sandbox/new-keptn-docs-engine/issues/1)
- Meg
  - [Questions around Vale](https://github.com/keptn-sandbox/new-keptn-docs-engine/issues/19#issuecomment-1219077675)
  - To Rajiv: think of the final presentation as a presentation to the customers who know nothing about the docs engine
  - TODO: Add expectations and comments around migrations in [keptn-sandbox#1](https://github.com/keptn-sandbox/new-keptn-docs-engine/issues/1)
- Indermohan
  - TODO: Add expectations and comments around migrations in [keptn-sandbox#1](https://github.com/keptn-sandbox/new-keptn-docs-engine/issues/1)
- Suraj
  - TODO: review [keptn-sandbox#20](https://github.com/keptn-sandbox/new-keptn-docs-engine/pull/20)
  - TODO: Add expectations and comments around migrations in [keptn-sandbox#1](https://github.com/keptn-sandbox/new-keptn-docs-engine/issues/1)

## 8th August 2022

- Attendees
  - Indermohan Singh
  - Meg McRoberts
  - Rajiv Ranjan Singh
  - Suraj Banakar
- Notes
  - Meg has reviewed [keptn-sandbox#15](https://github.com/keptn-sandbox/new-keptn-docs-engine/pull/15)
- Rajiv
  - Would be good to add docs around Lighthouse Audit in the CI
- Meg
  - What do Best Practices include for Lighthouse Audit?
    - [https://storage.googleapis.com/lighthouse-infrastructure.appspot.com/reports/1659673593422-98502.report.html#best-practices](https://storage.googleapis.com/lighthouse-infrastructure.appspot.com/reports/1659673593422-98502.report.html#best-practices)
  - Do we have a linter for unclosed italic tags, checking broken xrefs?
    - We need another issue for this
- Suraj
  - What is expected of the end result?

1. Docs Engine
   1. Users:
      1. Someone who writes docs
      2. Someone who develops integration and needs to document it.
   2. Expectations
      1. Suraj:
         1. As a User (i), I want to be able to migrate my docs without any technical help using the Docs Engine. As User (ii) I would like to add my docs to the official docs without any help using Docs Engine
      2. Meg:
         1. What checks will we have for docs and how do those compare to what we currently have?
            1. Checks for xref
            2. Lighthouse is adding checks we don’t currently have
            3. Markdown coding errors
         2. A clear approach to include docs from other repositories (what is supported)
            1. Can I include a file from another repo in my docusaurus markdown file? For example, something like #include keptn/keptn/…values.yaml in the Synopsis section of the values.yaml reference page
            2. Can I have a common code in another repo that can be pulled in?
            3. If I do, can I have variables so that when it’s pulled in I can change the value of the string depending on the context?
            4. Can I have a list of random markdown files in the software repo that are pulled into the doc build? So the full markdown for a reference file might be coded in the software source.
      3. Indermohan:
      4. Rajiv: Completing the work which is in the proposal like I thought giving priority to those works first.
2. Docs migration (includes look and feel, restructuring of the docs)
   1. Expectations
      1. Suraj:
      2. Indermohan:
      3. Meg:
         1. Docs look and feel – probably need to prototype a few samples and put them out for community review and discussion
            1. Do we use cards for subsections? This duplicate information in the left frame would obscure any introductory text that might be coded in the top level of the section but some people seem to like the cards.
            2. If we use cards, what do they look like?
         2. Script(s) to migrate doc content
            1. Need to move some sections – the landing page for the docs will no longer show release numbers. Instead, this will be the “latest” and docs for older releases will be available from a drop-down.
            2. Need to rename files. Currently, all content is in \_index.md and index.md files. So, for example, what is currently shipyard/index.md should be just shipyard.md (or whatever the suffix is)
            3. How to convert xrefs within the doc set, which are currently coded by file pathname
            4. Where will “assets” (mostly .png and .jpeg files) be located in the new repository? The script must move these files appropriately.
         3. Can we implement “Fix this page” for the published docs so that the user is just put into the GitHub editor to suggest a change and that is bundled into a commit/PR that can be reviewed and merged? I think that the major hurdle is DCO (which transfers intellectual property ownership to the Keptn project)
      4. Rajiv: Docs migration and structure will go one as we get feedback from users so this is never ending work I guess but we can have a minimum viable design.

## 15th July 2022

- Attendees
  - Rajiv Ranjan Singh
  - Suraj Banakar
- Suraj
  - Demo in GSoC Community meeting
    - Rajiv is going to prepare a presentation
    - If all the PRs don’t get merged, we demo Rajiv’s branch. That being said let’s try to get all of his PRs merged
  - Rajiv needs review on [https://github.com/keptn-sandbox/new-keptn-docs-engine/pull/9/files](https://github.com/keptn-sandbox/new-keptn-docs-engine/pull/9/files)
  - There’s one more PR around versioning which Rajiv is going to create
  - Rajiv will reach out to the team for input on multi-repo support
  - Rajiv is going to work on the presentation for the GSoC Community meeting

## 1st July 2022

- Attendees
  - Indermohan Singh
  - Meha Bhalodiya
  - Rajiv Ranjan Singh
  - Suraj Banakar
- Rajiv
  - Migrating content from Hugo to Docusaurus leads to issues with CSS and some Hugo-specific constructs which can’t be used in Docusaurus
- Suraj
  - Adding SEO tags sounds like a lot of manual work
- Indermohan
  - Add Indermohan and Suraj for PRs with technical things
  - Add Meg as a reviewer for PRs around structuring, writing, or anything where you need input on how content should be written or structured
- Todo
  - Indermohan: Create GitHub issues around the problems we see in the migrated content
  - Mentors: Ask Oleg/Community if we want to enable i18n support now or later
  - Indermohan: Create a GitHub issue to research around front matter linting
  - Rajiv: Ask for early feedback for [https://keptn-experimental-docs-site.netlify.app/quickstart/quickstart](https://keptn-experimental-docs-site.netlify.app/quickstart/quickstart)
  - Indermohan: Create an issue around multiple docusaurus instances like [this](https://github.com/keptn-sandbox/new-keptn-docs-engine/blob/a4115b723125e456917b5d0281387255b6a02517/docusaurus.config.js#L92-L149)

## 17th June 2022

- Attendees
  - Indermohan Singh
  - Meg McRoberts
  - Rajiv Ranjan Singh
- Rajiv shared the progress of the doc engine and initialization of the Docusaurus site
- Indermohan will make an issue with the restructuring of docs
- Discussion on what contents and section we have to move to Docusaurus at starting phase of the project

## 3rd June 2022

- Attendees
  - Rajiv Ranjan Singh
  - Suraj Banakar
- Discussion about Rajiv's work and what he did and explore things related to Keptn docs last week
- Updates about work that we discussed last week
- Suraj gave knowledge transfer to Rajiv about Keptn docs and Keptn CLI

## 26th May 2022 (Kickoff meeting)

- Attendees
  - Indermohan Singh
  - Meg McRoberts
  - Rajiv Ranjan Singh
  - Suraj Banakar
- Introductions
  - Indermohan Singh
  - Meg McRoberts
  - Rajiv Ranjan Singh
  - Suraj Banakar
- Communication
  - Scheduled meetings
  - Slack for ad hoc conversations
- Feature list
  - A very unofficial and probably incomplete list of requirements at [Doc Tools Requirements](https://docs.google.com/document/d/1VvDtVW-zV8bfhHNrXBNZdJz5s81a1M1eulov8_ahqo0/edit#heading=h.fyeyfl7x8jho)
  - Let’s take a quick look so we know if we have any outages – I don’t think we do
  - Rajiv’s list of features – need to finalize
- Multiple repository doc support
  - [zero-md](https://zerodevx.github.io/zero-md/) (it fetches content at runtime)
  - Fetch content at build time
  - Others?
- Any blockers for Rajiv to get started?
- Action Items
  - Set up #wg-doc-engine slack channel (@Suraj)
    - Use public channels and GitHub issues for communication
  - Ask around about what repo to use for Github issues(@Indermohan)
    - Need repo for Docusaurus (probably same can be used for GitHub issues)
    - Dev docs using GitHub Actions
    - Access for Netlify
  - Create a doodle for the biweekly meeting (@Suraj)
    - Create a recurring biweekly meeting for the Keptn community calendar
  - Reach out to Oleg to for scheduling meetings with Bevy – try it out (@Suraj)
    - Record meetings – use CNCF Bevy
  - Clarify with Oleg if we have to redo the landing page (@Indermohan)
  - Create the structure of new documentation (@Meg)
    - [Restructure documentation](https://docs.google.com/document/d/12xVgFSV5Q7keDXOqVFE8pqY0Qkhq--nKsP-7NkVuyjA/edit#heading=h.vm22oe3mkivh)
    - Developer docs + User docs
