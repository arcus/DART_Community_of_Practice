# DART Community of Practice

This repository contains the email templates and community building prompts for the 16 week [DART Program](https://arcus.github.io/education_modules/).

The [syllabus](syllabus.md), shorter [schedule](schedule.md) and [Weekly Emails](Weekly_Emails) are built from the information inside the [Prompts folder](Prompts).

## Using this Repository

Before using the materials in this repository, make sure to update the links (emphasized with 🔴) in the following places:

* [ ] Mid-program survey in [`Prompts/3_Learning_to_Learn/4_Processing_Learning/activity.md`](https://github.com/arcus/DART_Community_of_Practice/blob/main/Prompts/3_Learning_to_Learn/4_Processing_Learning/activity.md)
* [ ] Post-intervention survey in [`Prompts/6_Wrapping_Up/1_Reflecting_on_DART/activity.md`](https://github.com/arcus/DART_Community_of_Practice/blob/main/Prompts/6_Wrapping_Up/1_Reflecting_on_DART/activity.md)
* [ ] Post-intervention survey in [`Prompts/6_Wrapping_Up/2_Beyond_DART/activity.md`](https://github.com/arcus/DART_Community_of_Practice/blob/main/Prompts/6_Wrapping_Up/2_Beyond_DART/activity.md)

When all links are updated, run the `run_all.sh` script to update the emails, schedule, and syllabus.

Also note that the week 1 email references an additional email with information from orientation, including links to a recording, and specific times for drop-in help hours.

## Prompts Structure

Any update to the order or contents of the community of practice prompts should be made in the file containing it in that week's folder under Prompts.

Each week has 5 markdown files describing it. 

NOTE: list formatting in these files must be in html to ensure proper rendering in emails and syllabus.

- `activities.md`
- `discussion_topic.md`
- `extra.md` this file may contain an opportunity to explore further or plan the community, or may be left empty. Formatting should be:
```
**Bolded Title**
Description of the extra activity. So far these are either instructions about planning communication or exploring the week's topic further.
```
- `social_warm_up.md`
- `theme.md` which contains the week's data:
```
program_week:
section: 
section_week: 
topic: 
signature: 
```
Some weeks (6 and 7) have an additional file which will be attached to the email as part of the week's activities.

## Weekly Emails

The weekly emails are generated from the Prompts and **should not be edited directly**.

**WARNING:** If you do update a weekly email directly, your changes will be overwritten the next time a file in Prompts or Weekly_Emails/Email_Text is changed.

The language in the prompts can be updated in their respective markdown files, and the other text of the emails can be changed in the subfolder [Email_Text](https://github.com/arcus/DART_Community_of_Practice/tree/main/Weekly_Emails/Email_Text).

## Automation

Any update to a file in Prompts, Weekly_Emails/Email_Text, or scripts will trigger a GitHub Action that will rebuild the weekly emails, schedule, and syllabus on `push`ing to the repository.

**WARNING / TODO:** If a change is made that does not alter the weekly emails, schedule, or syllabus, (e.g. adding comments to scripts) the build will fail because it has nothing to change. It is okay to ignore this failure.

### Scripts

If you want to recreate this automation outside of GitHub, the scripts used are in the scripts folder:

- `syllabus.sh` creates [syllabus.md](syllabus.md) which contains the weekly themes and activities as a table.
- `schedule.sh` creates a shorter list version with links to the prompts folder for each week in [schedule.md](schedule.md)
- `emails.sh` creates the weekly emails
- `run_all.sh` should be run each time a prompt is updated or a section of email text changed.


These scripts should be run from the main `DART_Community_of_Practice` directory.
