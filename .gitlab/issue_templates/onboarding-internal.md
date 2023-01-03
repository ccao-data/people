Welcome to the Cook County Assessor's Office (CCAO) Data Department! We're excited to have you! This webpage is a GitLab issue. An issue is a way to track work that needs to be done. This particular issue outlines the tasks you need to complete to onboard with the Data Department. Once you complete each task, please mark the checkbox as shown below:

- [x] This task is complete.

If a task does not apply to you, please mark it anyways so we can track the progress of this issue. If you have a question at any point, please feel free to comment on this issue ticket and tag Billy (@sweatyhandshake), Dan (@dfsnow), or Nicole (@ccaojardine).

# GitLab

Nearly all of the Data Department's work is tracked using GitLab. In order to participate in this issue and contribute to the Department, you will need a GitLab account.

- [ ] Create a [GitLab](https://gitlab.com/) account. If you do not already have one, create a free [GitLab](https://gitlab.com/) account using your personal email address.
- [ ] Log in to [GitLab](https://gitlab.com/) and comment on this issue ticket to let us know your username.

Please note that your GitLab account can persist after your employment/internship has ended and can be a valuable resource in your career. Your work will mostly be public, so please take a moment to review [GitLab's communication guidelines](https://about.gitlab.com/handbook/communication/#effective--responsible-communication-guidelines).

You may also want to explore GitLab to familiarize yourself with the platform. The main CCAO GitLab group can be found [here](https://gitlab.com/ccao-data-science---modeling).

# Before Your First Day

There are a number of administrative tasks you need to complete before you start working with the Data Department. These will typically occur before your first day.

## HR Paperwork

Official onboarding paperwork is handled by the CCAO's Human Resources Department. They will reach out to you directly before you start to provide paperwork and guidance. If you have questions or have not received any paperwork, email [HR](assessor.ccaohr@cookcountyil.gov).

- [ ] Complete any HR onboarding paperwork (I-9, employee info, etc.) and return it to [HR](assessor.ccaohr@cookcountyil.gov).

## Email

When you work in the public sector in Illinois your work correspondence is considered an official record. It is important that you do not use your personal email account, Dropbox, Google Drive, or any other personal digital accounts or systems to do your work. **All CCAO work should be done using CCAO provided emails and file storage locations.** 

HR/IT will provide login credentials for your CCAO email account. This is your main account at the CCAO. It is used to access email, Teams, and all Microsoft products.

- [ ] Login to your CCAO email.

## VPN

If you plan to work remotely, you will need to use the county VPN to access internal files and servers. You should receive an email from Admins or NCC (at your county email address) with instructions on how to setup and use the VPN. You will receive a second, separate email to enroll in Duo, which provides multi-factor authentication. For VPN troubleshooting, email the [CCAO Admins](Assessor.admins@cookcountyil.gov). For more information on the VPN, see the [Data Department wiki](https://gitlab.com/groups/ccao-data-science---modeling/-/wikis/How-To/Setup-the-Cook-County-VPN).

- [ ] Complete the [Cook County VPN Access](/forms/new-hire/5.%20VPN%20Remote%20Access%20Waiver.pdf) form and email it to the CCAO's [Admins](Assessor.admins@cookcountyil.gov). You must use your CCAO email address when completing this form.
- [ ] Install the Cook County VPN client on your computer and successfully connect (test by visiting the [CCAO intranet](http://intranet/)).

## Teams

Ask or [email](mailto:nicole.jardine@cookcountyil.gov) @ccaojardine for an invite to the Data Department "Team" within the CCAO group and the "General" chat within that Team.

- [ ] Send a Teams message to the Data Department "General" chat introducing yourself.

## Federal W4

You'll need to complete/update a Federal W4 as part of the onboarding process with [HR](assessor.ccaohr@cookcountyil.gov). This form must be filled out using Cook County's Employee Self Service (ESS) system. It usually takes about a week to receive access to this system once you are onboarded. If you've already completed this step, simply check the box and continue on.

Once you are given access to the ESS system, go to the [intranet](intranet/) and select “New EBS Employee Self Service” on the right side of the page. You will be directed to an Oracle webportal, where you’ll open the CCG Employee Self Service folder and select “Tax Form.” There, you can make any necessary updates to your Federal W4.

- [ ] Complete/update your Federal W4 in the Employee Self Service system.

Once your W4 is filled out, you can (optionally) enroll in direct deposit using the same system. If you don't enroll in direct deposit, then your paychecks will be mailed to the address you provided on your I-9.

# Your First Week

## Working Remotely

The CCAO Data Department is currently working on a hybrid schedule. We are in-office on Wednesday and Thursday and remote the rest of the week. Interns are encourage to spend at least one day per week in-office with the team.

## Hardware and Software 

You will be issued a CCAO laptop as part of your onboarding. This laptop has all the software you need pre-installed. When working remotely, you can take your CCAO laptop home OR use a personal machine. You will need to use the [VPN](#vpn-client) to connect to CCAO resources while not in the office.

If using a personal machine, you will need to install the following tools for communication and accessing internal resources:

- [ ] [Teams](https://products.office.com/en-us/microsoft-teams/download-app) - Main CCAO communications method
- [ ] A web browser of your choice

If you're not using a personal machine, or already have the necessary tools installed, please check the boxes above.

## Server Setup

For actual coding and computation, the Data Department uses an on-premise server. The server can be accessed via SSH, RStudio, or JupyterLab as long as you are connected to the county VPN. To gain access to the server, you will need an account.

- [ ] Send a Teams message to Dan (@dfsnow) requesting an RStudio/server account.

Once your account is created, you can connect to the server via [RStudio](https://datascience.cookcountyassessor.com/rstudio/) or [JupyterLab](https://datascience.cookcountyassessor.com/jupyter).

- [ ] Successfully login to either [RStudio](https://datascience.cookcountyassessor.com/rstudio) or [JupyterLab](https://datascience.cookcountyassessor.com/jupyter).

## Projects and Git

You can use either RStudio's git integration or the command line (via SSH) to manage CCAO git repositories. If you are unfamiliar with git or RStudio's git integration, watch [this webinar](https://www.rstudio.com/resources/webinars/managing-part-2-github-and-rstudio/).

Additionally, the Data Department uses RStudio's projects feature to manage environments and switch between contexts.

- [ ] Read RStudio's [introduction to projects](https://support.rstudio.com/hc/en-us/articles/200526207-Using-RStudio-Projects).
- [ ] Clone a [CCAO repository](https://gitlab.com/ccao-data-science---modeling/models/ccao_res_avm) using RStudio's projects feature.

## Issue Resolution

The CCAO Data Department roughly uses [GitHub flow](https://docs.github.com/en/get-started/quickstart/github-flow) to manage its work. GitHub flow uses a basic branch-per-issue system. Each issue or new feature is tied to a branch and merge request. Work is done on the branch, then merged to `master` (or `main`) after testing and review. Here's an example of a typical workflow:

1. You are assigned **Issue #118, Update Internal Contribution Guidelines** within GitLab.
    * Check to see if there is a branch associated with your issue within GitLab. Branches created via issues usually have a similar name, in this case the branch name would be `118-update-internal-contribution-guidelines`.
    * If a branch doesn't exist, then create one yourself. Each issue has an associated "Create Merge Request" button which will create a branch and merge request for that issue.
2. Checkout the issue branch.
    * Within RStudio, navigate to the git pane, then click the branch name in the upper right-hand corner (usually **master**). Select the branch associated with the issue you have been assigned. In this case, `118-update-internal-contribution-guidelines`. You can also click different branch names to check them out.
    * The branch you selected should now appear in the upper right-hand corner of the git pane. You are now working within that branch.
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

Interns may work up to 20 hours per week and are encouraged to do so. Working 15 hours or less may limit the assignments you receive, as most of our departmental projects require a significant time investment. Intern schedules and certain events are tracked on a shared calendar (the Data Department calendar). 

- [ ] Email your preferred schedule to [Nicole](mailto:nicole.jardine@cookcountyil.gov) and [Dan](mailto:daniel.snow@cookcountyil.gov). Include the days and times you will be working and the date of your last day. Subject: 'YOUR NAME - Internship Hours'

During the first week of employment, interns _may_ need to manually record their hours on a paper timesheet which is turned in at the end of the week. The timesheet can be found [here :page_facing_up:](/forms/internship/intern-time-sheet.pdf). After the first week, interns will use the Cook County Time system to track their hours. Visit [this page](https://www.cookcountyil.gov/cct) and click **Dashboard Login** to access CCT. **We recommend that you create a recurring calendar event to remind you to clock in and out.**

Data Department fellows do not need to submit time sheets to the CCAO. They are still accountable for their time, but are paid by their academic institutions.

## Required Reading and Bookmarks

All new hires, interns, and fellows are required to read the following:

- [ ] [Data Department Handbook](https://gitlab.com/groups/ccao-data-science---modeling/-/wikis/Handbook/Handbook) - Outlines the purpose, procedures, and practices of the department
- [ ] [Data Department Mission, Vision, and Values](https://gitlab.com/groups/ccao-data-science---modeling/-/wikis/Handbook/Mission-Vision-Values) - Outlines the principles and goals of the department
- [ ] [Data Department Resources Page](https://gitlab.com/groups/ccao-data-science---modeling/-/wikis/Handbook/Resources) - Read everything marked with a :exclamation:. You can skip *R for Data Science* and *Select Star SQL* if you're already proficient in R/SQL.
- [ ] [Data Department Glossary](https://gitlab.com/groups/ccao-data-science---modeling/-/wikis/Handbook/Glossary) - The CCAO uses a lot of assessment- and office-specific jargon. Read through this glossary to get acquainted with some of the terms.

Additionally, take a moment to bookmark all the links marked with a :exclamation: under the "Useful Bookmarks" section of the [Resources](https://gitlab.com/groups/ccao-data-science---modeling/-/wikis/Handbook/Resources#useful-bookmarks) page.

If you have downtime while working, we highly recommend reading anything marked with a :star: on the [Resources](https://gitlab.com/groups/ccao-data-science---modeling/-/wikis/Handbook/Resources) page.

NOTE: Please report any broken links, spelling/grammar mistakes, or inaccurate instructions in this issue to @dfsnow.

/assign @dfsnow @ccaojardine
