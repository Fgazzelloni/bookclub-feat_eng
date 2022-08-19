# R4DS Feature Engineering and Selection Book Club

Welcome to the R4DS Feature Engineering and Selection Book Club!

We are working together to read [_Feature Engineering and Selection: A Practical Approach for Predictive Models_](http://www.feat.engineering/) by Max Kuhn and Kjell Johnson (Chapman and Hall/CRC, copyright August 2, 2019, [9781138079229](https://www.routledge.com/Feature-Engineering-and-Selection-A-Practical-Approach-for-Predictive-Models/Kuhn-Johnson/p/book/9781138079229)).
Join the [#book_club-feat_eng](https://rfordatascience.slack.com/archives/C02Q3JUL8BY) channel on the [R4DS Slack](https://r4ds.io/join) to participate.
As we read, we are producing [notes about the book](https://r4ds.io/feat_eng).

## Meeting Schedule

If you would like to present, please see the sign-up sheet for your cohort (linked below, and pinned in the [#book_club-feat_eng](https://rfordatascience.slack.com/archives/C02Q3JUL8BY) channel on Slack)!

- [Cohort 1](https://docs.google.com/spreadsheets/d/1_7IxmdZf-3MRPDy-rlNHdzuI2d4QH7gG6LQQIQpDMnI/edit) (started 2022-08-19): [Fridays, 12:00 noon CST/CDT](https://www.timeanddate.com/worldclock/converter.html?iso=20220819T170000&p1=24&p2=179&p3=5148&p4=53&p5=1440) | [meeting videos](https://www.youtube.com/playlist?list=PL3x6DOfs2NGgVpjjKEIYzSu26ex6p78-W)

<hr>


## How to Present

This repository is structured as a [{bookdown}](https://CRAN.R-project.org/package=bookdown) site.
To present, follow these instructions:

Do these steps once:

1. [Setup Github Locally](https://www.youtube.com/watch?v=hNUNPkoledI) (also see [_Happy Git and GitHub for the useR_](https://happygitwithr.com/github-acct.html))
2. Install {usethis} and {devtools} `install.packages(c("usethis", "devtools"))`
3. Set up a default {usethis} directory:
  - `usethis::edit_r_profile()` to open your profile for editing.
  - Add this line: `options(usethis.destdir = "YOURDIR")` (replace `YOURDIR` with the root directory under which you want your R projects to appear; or you can skip these steps, and the project will be saved to your Desktop).
  - Restart your R session (Session/Restart R in Rstudio).
4. `usethis::create_from_github("r4ds/bookclub-feat_eng")` (cleanly creates your own copy of this repository).

Do these steps each time you present another chapter:

1. Open your project for this book.
2. `usethis::pr_init("my-chapter")` (creates a branch for your work, to avoid confusion, making sure that you have the latest changes from other contributors; replace `my-chapter` with a descriptive name, ideally).
3. `devtools::install_dev_deps()` (installs any packages used by the book that you don't already have installed).
4. Edit the appropriate chapter file, if necessary. Use `##` to indicate new slides (new sections).
5. If you use any packages that are not already in the `DESCRIPTION`, add them. You can use `usethis::use_package("myCoolPackage")` to add them quickly!
6. Build the book! ctrl-shift-b (or command-shift-b) will render the full book, or ctrl-shift-k (command-shift-k) to render just your slide. Please do this to make sure it works before you push your changes up to the main repo!
7. Commit your changes (either through the command line or using Rstudio's Git tab).
8. `usethis::pr_push()` (pushes the changes up to github, and opens a "pull request" (PR) to let us know your work is ready).
9. (If we request changes, make them)
10. When your PR has been accepted ("merged"), `usethis::pr_finish()` to close out your branch and prepare your local repository for future work.
11. Now that your local copy is up-to-date with the main repo, you need to update your remote fork. Run `gert::git_push("origin")` or click the `Push` button on the `Git` tab of Rstudio.

When your PR is checked into the main branch, the bookdown site will rebuild, adding your slides to [this site](https://r4ds.io/feat_eng).
