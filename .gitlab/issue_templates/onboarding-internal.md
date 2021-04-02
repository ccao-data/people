Welcome aboard! This issue ticket will guide you through your first day. If at any point you need help, please reach out to Billy @sweatyhandshake, Dan @dfsnow, or Sam @ssimpson.

## Email

When you work in the public sector in Illinois, and many other places, your work correspondence is considered an official record. It is very important that you do not use your personal email account, personal Dropbox, Google Drive, or any other personal digital accounts or systems to do your work. **All CCAO work should be done using CCAO provided emails and file storage locations.** 

HR/IT should contact you with login credentials for your CCAO email account.

- [ ] Login to your CCAO email.

## Teams

Ask or [email](mailto:wridgeway@cookcountyassessor.com) @sweatyhandshake for an invite to the Data Science "Team" within the CCAO group.

- [ ] Send a Teams message to the General Data Science chat introducing yourself.

## Accounts

Please create accounts with the following services using your CCAO email. If you already have a GitLab account or created one during pre-onboarding, please change your contact email to your @cookcountyassessor.com email address. All commits to CCAO repositories should be made with a CCAO email address.

- [ ] [GitLab](https://gitlab.com/) - Change your contact email to your @cookcountyassessor.com email.
- [ ] [Bitbucket](https://bitbucket.org/) - Needed only for Sourcetree install. Feel free to skip this if you use CLI git.

## Install Software 

The CCAO Data Science Department uses a variety of tools and software packages. We do not *require* that you use the tools listed below. However, if you choose to use something else, then you are responsible for debugging any issues with your toolchain.

- [ ] [Sourcetree](https://www.sourcetreeapp.com/) - Frontend UI for git version control and GitLab (optional, you can use CLI git/git bash if you prefer)
   - Link your Bitbucket account to Sourcetree during Sourcetree installation
   - When Sourcetree asks you to install mercurial and git, select **Yes** for both
- [ ] [R](https://cloud.r-project.org/) - Main CCAO programming language (use version 4.0.0 or greater)
- [ ] [RStudio](https://rstudio.com/products/rstudio/download/#download) - Integrated development environment for R
- [ ] [PuTTY](https://www.putty.org/) - SSH client and key generator
- [ ] [Teams](https://products.office.com/en-us/microsoft-teams/download-app) - Main CCAO communications method

## Software Setup

### Git, GitLab, and Sourcetree

- [ ] Check your email for an invitation to join GitLab. If you don't already have a pending invite to the [CCAO GitLab](https://gitlab.com/ccao-data-science---modeling) group, request one from `@sweatyhandshake`.
- [ ] Create a .ssh folder in your home directory.
   * One way to do this is to open the Start Menu and type `cmd` in the search box. Click on `cmd.exe` when it comes up in the search results. This will open up a Windows command prompt. Enter `mkdir .ssh` in the command prompt. This will create a folder called `.ssh` in your home directory.
- [ ] Generate SSH keys with Sourcetree (if you'd like to generate an SSH key pair without Sourcetree, see instructions [here](https://docs.gitlab.com/ee/ssh/#generating-a-new-ssh-key-pair)).
   * Open Sourcetree and go to **Tools**
   * Select **Create or import SSH keys**
   * Select **Generate**
   * Save the public and private keys to your `.ssh` folder (add a password to your private key if you desire)
   * Copy your newly generated SSH keys from the Sourcetree window. **Pasting this version of your ssh key into PuTTY and GitLab will help avoid errors.**
- [ ] Right click the PuTTY icon in the system tray (bottom right portion of task bar).
   * Click **Add key**
   * Locate the private key in your `.ssh` folder (no .pub ending) and add it to PuTTY
- [ ] Add your SSH keys to GitLab.
   * In GitLab, go to **Settings** under your profile icon in the top-right corner
   * On the left-hand side of the settings window, click **SSH Keys**, then paste your public key into the box (the title and expiration date are arbitrary and can be whatever you'd like)
- [ ] Clone your desired CCAO project.
   * In Sourcetree, select **Clone**
   * Within GitLab, find the repository you'd like to clone
   * From the main page of the project, select the blue **Clone** button on the top right-hand side of the page. Click the **Clone with SSH** button to copy the SSH URI to your clipboard
   * Paste this into the top line of the **Clone** page in Sourcetree, and click out of the box
   * If Sourcetree encounters an error, restart it and repaste the text into the **Clone** field
   * Under **Advanced Options**, select the `master` branch
   * Press the **Clone** button at the bottom of the page

### VPN Client

 You should receive an email from Admins or NCC with instructions on how to access the CCAO network through a VPN. For VPN troubleshooting, email the CCAO [Admins](mailto:admins@cookcountyassessor.com).

- [ ] Install the Cook County VPN on your computer and successfully connect (test by visiting the [CCAO intranet](http://intranet/)).

## Issue Resolution

The CCAO Data Science team uses [GitLab Flow](https://docs.gitlab.com/ee/topics/gitlab_flow.html) to manage its work. GitLab Flow uses a basic branch-per-issue system. Each issue or new feature is tied to a branch and merge request. Work is done on the branch, then merged to `master` after testing and review. Here's an example of a typical workflow:

1. You are assigned **Issue #118, Update Internal Contribution Guidelines** within GitLab.
   * Check to see if there is a branch associated with your issue within GitLab. Branches created via issues usually have a similar name, in this case the branch name would be `118-update-internal-contribution-guidelines`.
   * If a branch doesn't exist, please ask your supervisor to create one. Please *do not* create a branch yourself.

2. Checkout the issue branch.
   * Within Sourcetree, click **Repository --> Checkout**, then select the branch associated with the issue you have been assigned. In this case, `118-update-internal-contribution-guidelines`. You can also double-click different branch names to check them out.
   * The branch you selected should now appear in bold under **BRANCHES** on the left side of Sourcetree. You are now working within that branch.

2. Work the issue. Use the issue page comments to communicate with your supervisor about the issue.

3. Commit often and use [descriptive commit messages](https://commit.style/). Only push to your issue branch, never directly to `master`.

4. When you have finished working on the issue:
   * Push all work to your issue branch
   * Create a merge request if one doesn't exist already
   * If a merge request exists but is tagged as **Work-in-progress**, remove the WIP tag using the GitLab UI
   * Request approval for your merge request to let your supervisor know you've finished working the issue
   * Merge your code. You can select **Merge Immediately** from the merge dropdown (we rarely use merge trains)

See the [Version Control and Workflow](https://gitlab.com/groups/ccao-data-science---modeling/-/wikis/Handbook/Handbook#version-control-and-workflow) section of the handbook for more information.

## Intern Hours, Projects, and Time Tracking

Interns may work up to 20 hours per week and are encouraged to do so. Working 15 hours or less may limit the assignments you receive, as most of our departmental projects require a significant time investment.

Intern schedules and certain events are tracked on a shared calendar (the Data Science calendar). Interns are expected to input and update their own schedule on this calendar. You will need to email the [Admins](mailto:admins@cookcountyassessor.com) to receive calendar write access.

- [ ] Email your preferred schedule to [Samantha Simpson](mailto:ssimpson@cookcountyassessor.com). Include the days and times you will be working and the date of your last day. Subject: 'YOUR NAME - Internship Hours'
- [ ] Email [Admins](mailto:admins@cookcountyassessor.com) to ask for write access to the Data Science calendar. Once access is granted, record the hours you plan to work on the calendar.

During the first week of employment, interns will need to manually record their hours on a paper timesheet which is turned in at the end of the week. The timesheet can be found [here :page_facing_up:](/forms/internship/intern-time-sheet.pdf). After the first week, interns will use the Cook County Time system to track their hours. Visit [this page](https://www.cookcountyil.gov/cct) and click **Dashboard Login** to access CCT. **We recommend that you create a recurring calendar event to remind you to clock in and out.**

Data science fellows do not need to submit time sheets to the CCAO. They are still accountable for their time, but are paid by their academic institutions.

## Required Reading and Bookmarks

All new hires, interns, and fellows are required to read the following:

- [ ] [Data Science Department Handbook](https://gitlab.com/groups/ccao-data-science---modeling/-/wikis/Handbook/Handbook) - Outlines the purpose, procedures, and practices of the department
- [ ] [Data Science Department Mission, Vision, and Values](https://gitlab.com/groups/ccao-data-science---modeling/-/wikis/Handbook/Mission%20Vision%20Values) - Outlines the principles and goals of the department
- [ ] [Data Science Resources Page](https://gitlab.com/groups/ccao-data-science---modeling/-/wikis/Handbook/Resources) - Read everything marked with a :exclamation:. You can skip *R for Data Science* and *Select Star SQL* if you're already proficient in R/SQL.
- [ ] [Data Science Glossary](https://gitlab.com/groups/ccao-data-science---modeling/-/wikis/Handbook/Glossary) - The CCAO uses a lot of assessment-specific and office-specific jargon. Read through this glossary to get acquainted with some of the terms.

Additionally, take a moment to bookmark all the links marked with a :exclamation: under the "Useful Bookmarks" section of the [Resources](https://gitlab.com/groups/ccao-data-science---modeling/-/wikis/Handbook/Resources#useful-bookmarks) page.

If you have downtime while working, we highly recommend reading anything marked with a :star: on the [Resources](https://gitlab.com/groups/ccao-data-science---modeling/-/wikis/Handbook/Resources) page.

## Offboarding

You will notice that you have been assigned an offboarding issue ticket. This should be completed at the end of your tenure at the CCAO.

NOTE: Please report any broken links, spelling/grammar mistakes, or inaccurate instructions in this issue to @dfsnow.

/assign @sweatyhandshake @dfsnow @ssimpson
/label ~"type::management::onboarding" ~"stakeholder::internal::data" ~"priority::high" ~"status::to do"
