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
  - Indermohan: Create Github issues around the problems we see in the migrated content
  - Mentors: Ask Oleg/Community if we want to enable i18n support now or later
  - Indermohan: Create a Github issue to research around front matter linting
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

## 26 May 2022 (Kickoff meeting)

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
