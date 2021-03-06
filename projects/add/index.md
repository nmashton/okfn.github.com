---
title: Projects - Add a project
layout: two-column
bodyclass: code
---

# Add a project

Criteria for listing a project on Labs:

* Fit with [the set of general Labs community principles](/about/#principles).
  These aren't super strict but we suggest you read these through and consider
  whether your project fits (or what you could change to make it fit)
* You are an "Official Contributor" - to list a project as a Labs project you
  need to be an [Official Contributor][contributor]. We do make exceptions so
  if you think your project is super-deserving of this privilege you can [get
  in touch][contact] -- or even just submit the pull request and we can
  discuss there

[contact]: /contact/
[contributor]: /about/#contributors

## Steps to add a project

To add a project, you should have [signed up as a labs
member](/members/signup/).  We also strongly recommend [joining the mailing
list and following Labs on twitter](/contact/).

1. Put together a brief bit of info about the project. It has 2 parts, some
   structured data of form `item: value` at the top followed by some free text
   (general description). Here's what it should look like (all items are
   optional except those marked as required):

        ---
        layout: project [REQUIRED]
        title: {the project title e.g. Awesome Data Visualizer} [REQUIRED]
        slug: {URL-friendly version of the title e.g. awesome-data-visualizer} [REQUIRED]
        permalink: /projects/{slug}/index.html [REQUIRED]

        type: {list from the following project types: [library, data, webapp, running
               service, tool]}
        author: {author(s) names e.g. Joe Bloggs}
        maintainers: {list of labs username(s) of those who maintain the project}
        featured: {set to 'yes' to add to the list of featured projects}
        github_user: {the github user who owns the repo e.g. okfn}
        github_repo: {the github repo name e.g. awesome-data-visualizer}
        helpwanted: {set to 'yes' if the project requires assistance of any sort}
        typeofhelp: {list from the following types of help required: [coding, data
                     analysis, data wrangling, testing, documenting, blogging,
                     evangelism, project managing]}
        imageurl: {URL to a project image or logo of around 235px by 150px}
        language: {list of languages the project uses e.g. [python, javascript]}
        projecturl: {URL of an external project webpage e.g.
                     http://awesomedatavisualizer.org}
        stage: {one of [idea, alpha, prototype, production, deployed, mature]}
        status: {set to 'retired' if the project is no longer active}
        tags: {list of relevant tags e.g. [django, google spreadsheets]}
        ---

        A brief description of the project. You can use html (or markdown - if
        markdown please make sure the file you create to hold the info (see
        below) uses .md extension rather than .html)!

        Things to include are:

        - What is it
        - Who is it for?
        - What problem does it solve?
        - How someone could contribute


   Here's an example:

        ---
        layout: project
        title: Kartograph
        slug: kartograph
        permalink: /projects/kartograph/index.html

        type: [library]
        author: Gregor Aisch
        featured: yes
        github_user: kartograph
        github_repo: kartograph.js
        imageurl: http://kartograph.org/showcase/eastcoast/eastcoast-90dpi_export.png
        language: [javascript, coffeescript, css, shell]
        projecturl: http://kartograph.org/
        stage: mature
        tags: Visualization
        ---

        Kartograph is a simple and lightweight framework for building interactive
        map applications without Google Maps or any other mapping service. It was
        created with the needs of designers and data journalists in mind.

2. Put this in a file name

2. Get this added to the [Labs Github repo][repo] (and thereby to the website).
   There are 2 options:

    * More geeky route: add this info to the repo yourself via fork and pull
      &ndash; instructions below
    * Less geeky route: email it to labs@okfn.org and we'll take care of it for
      you

3. Think about writing a blog to give a longer-form explanation of your project,
   appropriate for a more general audience.

### Geek Route

This assumes you know how to add stuff to a git repo on github (preferably via fork and pull).

1. We need to add the info above to the [Labs website repo on github][repo]

2. Fork the [repo][]

3. Create a file at this location

        projects/_posts/yyyy-mm-dd-{slug}.html

   where yyyy-mm-dd is the date you added the project. As an example, if
   your project’s slug were `awesome-data-visualizer` and today's date were
   2013-05-17 you would create

        projects/_posts/2013-05-17-awesome-data-visualizer.html

4. Add the info you prepared above. Save the file.

5. Commit and push.

6. Submit a pull request

[repo]: https://github.com/okfn/okfn.github.com/
