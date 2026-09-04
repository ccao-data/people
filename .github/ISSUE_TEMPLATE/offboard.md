---
name: Offboard
about: For offboarding departing employees, interns, and fellows
title: Offboard [FULL NAME]
labels: internal
assignees: ''

---

If you're reading this, then it's finally time to say goodbye. :sob: We're sad to see you go, but hope you've gained something from being a part of the Data Department! After leaving, you'll automatically lose access to your CCAO email address, CCAO private GitHub repos, the VPN, and Teams. Here are the things you need to do before you leave:

# Tasks for the Departing Employee

- [ ] Schedule an informal exit chat with your supervisor
- [ ] Email [HR](assessor.ccaohr@cookcountyil.gov) to confirm your last day
- [ ] Email your personal contact information to the Chief Data Officer and Directors, in case we need to follow-up on something you worked on
- [ ] (Interns only) Deliver your [wrap-up memo](#memo-interns-only) to your project lead and the Chief Data Officer via PR
- [ ] Return any CCAO equipment in your possession
  - Laptops should be returned directly to the IT department and should include any accessories (case, charger, etc.)

## Memo (Interns Only)

In addition to the items above, we ask that interns write up a short (one page) document summarizing your most substantial project of the quarter. The document should be understandable to an executive without a coding background and should cover:

- The problem you encountered
- The solution you implemented and any methods used
- The duration of the project
- The impact of the project
- Links to the relevant repository and/or issues
- Any remaining next steps

The memo should be submitted as a pull request to the [CCAO blog repository](https://github.com/ccao-data/blog). See that repository for examples of previous intern memos and their format. Upon completion, anticipate the memo will be sent by the project lead/CDO to other executives, such as the Chief of Staff and the Assessor.

If you so choose, the memo may also be used as the basis for a Data Department blog post, which will publicly summarize your work. We will share this post with you upon completion. If you do not wish to be featured in public posts, leave the boxes below unchecked.

- [ ] I consent to my work being featured publicly, such as a Data Department blog post or on the Assessor's website
- [ ] I approve of the CCAO using my memo as the background material for such posts

# Tasks for Data Leadership

- [ ] Remove the departing employee/intern from our GitHub org
- [ ] Revoke all private API/deploy keys
- [ ] Delete the AWS user account for the departing employee/intern if they are leaving permanently, or disable the account if the employee/intern will be returning soon
  - See the wiki page documenting how to [Administer Users on CCAO Services](https://github.com/ccao-data/wiki/blob/master/How-To/Administer-Users-on-CCAO-Services.md#aws) for a detailed explanation of the processes for deleting/disabling AWS accounts
- [ ] Archive and delete the user from the Data team server ([docs](https://github.com/ccao-data/wiki/blob/master/How-To/Administer-Users-on-CCAO-Services.md#data-server))
- [ ] Rotate passwords for any [shared accounts](https://github.com/ccao-data/wiki/blob/master/Handbook/Accounts.md) that the departing employee had access to
- [ ] Add the departing employee/intern to the [list of former interns and employees that we use to generate unique model identifiers](https://github.com/ccao-data/data-architecture/blob/master/dbt/seeds/ccao/ccao.person.csv)
