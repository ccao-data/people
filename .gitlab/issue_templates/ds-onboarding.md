# Onboarding for Internal CCAO Employees

Welcome to the Cook County Assessor's Office Data Science Department! We're excited to have you! Your department onboarding will be your first issue ticket to complete. Below you will find instructions and tasks. Please complete them in order. If you run into any trouble, please do not hesitate to reach out to @sweatyhandshake (Billy) or @dfsnow (Dan) for help.

> :warning:  Mac users should first obtain a remote desktop VPN from IT and follow the remaining instructions for that terminal. This tech stack does not seem to work well with mac OS.

# Working remotely

Make sure you have a quite space with good internet access from which to work. Please make sure you have a microphone to participate in remote meetings. A camera is also a good thing to have, though not required.

## VPN

- [ ] Compelete and return VPN request paperwork to admins@cookcountyassessor.com. While waiting for a response, complete the Teams and bookmarks sections below.
- [ ] Install VPN on your computer.

## Teams

 Ask @sweatyhandshake for an invite to the Data Science "Team" within the CCAO group.
# Bookmarks

Take a moment to bookmark these commonly used CCAO links:

**External**
- [ ] [CCAO GitLab](https://gitlab.com/ccao-data-science---modeling) - Main source for all Data Science Department code
- [ ] [IAAO Technical Standards](https://iaao.org/wcm/Resources/Technical_Standards/wcm/Resources_Content/Pubs/Technical_Standards.aspx) - Technical standards and measurements for the assessment field
- [ ] [CCAO GitLab](https://gitlab.com/ccao-data-science---modeling) - Main source for all Data Science Department code
- [ ] [IAAO Technical Standards](https://iaao.org/wcm/Resources/Technical_Standards/wcm/Resources_Content/Pubs/Technical_Standards.aspx) - Technical standards and measurements for the assessment field
- [ ] [The Cook County Assessor's PIN Search](https://www.cookcountyassessor.com/address-search) - Our office's application to find information about a PIN
- [ ] [Cook County Property Info](http://www.cookcountypropertyinfo.com/) - The County's application to find information about a PIN
- [ ] [Cook Viewer](https://maps.cookcountyil.gov/cookviewer/mapViewer.html) - A GIS application for finding PINs

**Internal**

> :warning: The internal application locations above will have a security warning when you first visit them. This warning can safely be ignored. Click **Advanced --> Accept the risk** to bypass the warning.

- [ ] [Data Science Wiki](https://datascience.cookcountyassessor.com/wiki) - This wiki, you're already here!
- [ ] [Data Science Application Server](https://datascience.cookcountyassessor.com/shiny) - Shiny server that launches CCAO Shiny applications. Login with Windows credentials
- [ ] [App Monitoring Server](https://datascience.cookcountyassessor.com/grafana/) - Dashboards for monitoring app usage, pipeline processes, etc. Ask `@dfsnow` for login

# Accounts

Please create accounts with the following services using your CCAO email.

- [ ] [GitLab](https://gitlab.com/) - Needed to contribute to the CCAO codebase (use your @cookcountyassessor.com email to make an account)
- [ ] [Bitbucket](https://bitbucket.org/) - Needed only for Sourcetree install

# Tech Stack

Install these programs.

- [ ] [Sourcetree](https://www.sourcetreeapp.com/) - Frontend UI for git version control and GitLab
   * Link your Bitbucket account to Sourcetree during Sourcetree installation
   * When Sourcetree asks you to install mercurial and git, select **Yes** for both
   
- [ ] [R](https://cloud.r-project.org/) - Main CCAO programming language (use version 3.6.3 or greater)
- [ ] [R Studio](https://rstudio.com/products/rstudio/download/#download) - Integrated development environment for R
- [ ] [SQL Server Management Studio (SMSS)](https://aka.ms/ssmsfullsetup) - SQL client that plays well with CCAO's SQL Server
- [ ] [SSMSBoost](https://www.ssmsboost.com/) - (Optional) Add-on to SMSS that adds handy features
- [ ] [PuTTY](https://www.putty.org/) - SSH client and key generator
- [ ] [Teams](https://products.office.com/en-us/microsoft-teams/download-app) - Main CCAO DS communications app
- [ ] [Microsoft ODBC Driver 17 for SQL Server](https://www.microsoft.com/en-us/download/details.aspx?id=56567) - Necessary to connect to SQL through R

# How to set up your work terminal

## Git, GitLab, and Sourcetree

- [ ] Check your email for an invitation to join GitLab. If you don't already have a pending invite to the [CCAO GitLab](https://gitlab.com/ccao-data-science---modeling) group, request one from `@sweatyhandshake`
- [ ] Create a .ssh folder in your home directory
   * One way to do this is to open the Start Menu and type `cmd` in the search box. Click on `cmd.exe` when it comes up in the search results. This will open up a Windows command prompt. Enter `mkdir .ssh` in the command prompt. This will create a folder called `.ssh` in your home directory.
- [ ] Generate SSH keys with Sourcetree (if you'd like to generate an SSH key pair without sourcetree, see instructions [here](https://docs.gitlab.com/ee/ssh/#generating-a-new-ssh-key-pair))
   * Open Sourcetree and go to **Tools**
   * Select **Create or import SSH keys**
   * Select **Generate**
   * Save the public and private keys to your `.ssh` folder (add a password to your private key if you desire)
   * Copy your newly generated SSH keys from the Sourcetree window. **Pasting this version of your ssh key into PuTTY and GitLab will help avoid errors.**
- [ ] Right click the PuTTY icon in the system tray (bottom right portion of task bar)
   * Click **Add key**
   * Locate the private key in your `.ssh` folder (no .pub ending) and add it to PuTTY
- [ ] Add your SSH keys to GitLab
   * In GitLab, go to **Settings** under your profile icon in the top-right corner
   * On the left-hand side of the settings window, click **SSH Keys**, then paste your public key into the box (the title and expiration date are arbitrary and can be whatever you'd like)
- [ ] Clone your desired CCAO project
   * In Sourcetree, select **Clone**
   * Within GitLab, find the repository you'd like to clone
   * From the main page of the project, select the blue **Clone** button on the top right-hand side of the page. Click the **Clone with SSH** button to copy the SSH URI to your clipboard.
   * Paste this into the top line of the **Clone** page in Sourcetree, and click out of the box
   * If Sourcetree encounters an error, restart it and repaste the text into the **Clone** field
   * Under **Advanced Options**, select the `master` branch
   * Press the **Clone** button at the bottom of the page
   * Clone the repositories to `"My Documents"`, or file paths will need to be rewritten in several scripts

## SQL Credentials

The Data Science Department uses a few SQL servers to store most of its backend data. The IP addresses and details of each database are:

| Common Name           | Usage                                  | IP Address     | Port | DB Name  | User      | Password | Permissions | Type     |
|-----------------------|----------------------------------------|----------------|------|----------|-----------|----------|-------------|----------|
| CCAODATA / SQL Server | All DS operations                      | 10.124.134.118 | 1433 | CCAODATA | CCAODATAR | Ask      | Read/write   | MS SQL   |
| Reporting Server      | Reporting only, has subset of CCAODATA | 10.124.134.121 | 1433 | CCAODATA | CCAORSRV  | Ask      | Read/index  | MS SQL   |
| RPIE Server           | RPIE backend data                      | 10.124.134.120 | 1433 | RPIE     | CCAORPIE  | Ask      | Read only   | MS SQL   |
| Monitoring Server     | Monitors DS applications               | 10.124.101.1   | 5432 | shiny    | shiny     | Ask      | Read/write  | Postgres |


**For use in R:**

R will automatically load [environmental variables](https://medium.com/chingu/an-introduction-to-environment-variables-and-how-to-use-them-f602f66d15fa) into memory from your [.Renviron file](https://www.dartistics.com/renviron.html). This can be used to load sensitive information like credentials and API keys without depending on a third-party library or function. To use this method:

- [ ] Create a `.Renviron` file inside your HOME folder (`"My Documents"` on Windows, `~` on *nix systems) (you should be able to run `usethis::edit_r_environ()` to both create and begin editting the file)
- [ ] Create an environmental variable equal to an ODBC-formatted connection string for the server you want to connect to within the `.Renviron` file. For example, `DB_CONFIG_CCAODATA=Driver={ODBC Driver 17 for SQL Server};Server=10.124.134.118;Database=CCAODATA;Uid=CCAODATAR;Pwd=PASSWORD;`. This will create a variable named `DB_CONFIG_CCAODATA`.
- [ ] Restart R/RStudio to load the environmental variable into R. You can access the variable's value using `Sys.getenv()`. For example, `Sys.getenv("DB_CONFIG_CCAODATA")` will access the variable created above.
- [ ] Connect to the database using the `.connection_string` argument of the `dbConnect()` function from `DBI`. A full example would look like:
 
```r
library(DBI) # required for DB connection
library(odbc) # required for ODBC specification

# Instantiate a database connection object, where DB_CONFIG_CCAODATA is equal
# to the environmental variable stored in the .Renviron file
CCAODATA <- dbConnect(odbc(), .connection_string = Sys.getenv("DB_CONFIG_CCAODATA"))

```

- [ ] If write access is needed for the CCAODATA database, ask @sweatyhandshake for the code needed to generate and store the necessary credentials. Using the code above, change `.connection_string = key_get("ccaodata_write", keyring = "ccaodata")` to connect with write priviledges.

**For use in SSMS (only if SMSSBoost is installed):**

- [ ] Go to **SSMSBoost > Settings > Preferred Connections > List**.  Here you can store server credentials provided by @sweatyhandshake for all databases you'll need to access.  Click the small yellow plus sign at the bottom of the screen to add server addresses and credentials.  Select **Connect object explorer at startup** for each connection
- [ ] Go to **Tools > Options > Environment > Startup** and select **Open empty environment**

## VPN Client

 You should recieve and email during onboarding from Admins or NCC with instructions on how to set up and access the CCAO network through a VPN. For VPN troubleshooting, email the CCAO [Admins](mailto:admins@cookcountyassessor.com).

# Issue Resolution

The CCAO Data Science team uses [GitLab Flow](https://docs.gitlab.com/ee/topics/gitlab_flow.html) to structure its workflow. GitLab Flow uses a basic branch-per-issue system. Each issue or new feature is tied to a branch and merge request. Work is done on the branch, then merged to `master` after testing and review. Here's an example of a typical workflow:

1. You are assigned **Issue #118, Update Internal Contribution Guidelines** within GitLab.
   * Check to see if there is a branch associated with your issue within GitLab. Branches created via issues usually have a similar name, in this case the branch name would be `118-update-internal-contribution-guidelines`.
   * If a branch doesn't exist, please ask your supervisor to create one. Please *do not* create a branch yourself.

2. Checkout the issue branch.
   * Within Sourcetree, click **Repository --> Checkout**, then select the branch associated with the issue you have been assigned. In this case, `118-update-internal-contribution-guidelines`. You can also double-click different branch names to check them out.
   * The branch you selected should now appear bolded under **BRANCHES** on the left side of Sourcetree. You are now working within that branch.

2. Work the issue. Please use the issue page comments to communicate with your supervisor about the issue.

3. Commit often and use [descriptive commit messages](https://commit.style/). Only push to your issue branch, never directly to `master`.

4. When you have finished working on the issue, request approval for your merge request let your supervisor know you've finished working the issue.

See the [Version Control and Workflow](handbook.md#version-control-and-workflow) section of the handbook for more information.

# Intern Timesheets

During the first week of employment, interns will need to manually record their hours on a paper timesheet which is turned in at the end of each week. The timesheet can be found [here :page_facing_up:](forms/Intern_Sign-in_Sheet.pdf). After that first week, interns will use the Cook County Time system to track their hours. Click [Dashboard login](https://www.cookcountyil.gov/cct) to log into CCT. **We recommend that you create a recurring calendar event to remind you to clock in and out.**

## Choosing your hours

Interns may work up to 20 hours per week. You are encouraged to do so; working 15 hours or less severly limits the quality of work you can do. Please email your preferred schedule to Rob rross@cookcountyassessor.com so that he can put it on the DS calendar.

## Fellow Timesheets

Data science fellows do not need to submit time sheets to the CCAO. They are still accountable for their time, but are paid by their academic institutions.

# Additional resources

[New Hire Orientation Slides](https://gitlab.com/ccao-data-science---modeling/ccao_ds_training/-/tree/master/Slides)
See the section [Working Remotely at the CCAO](https://datascience.cookcountyassessor.com/wiki/handbook/handbook.md) in our data science handbook.
The property assessment world involves a lot of real estate-specific jargon and vocabulary. A non-exhaustive list of commonly used vocabulary can be found in the [Sales Ratio Studies SOP](../sops/sales-ratio-studies.md#definitions).

---

:fire: