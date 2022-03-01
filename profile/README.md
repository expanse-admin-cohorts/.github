## Welcome

This is the GitHub Organization for EXPANSE's administrative cohorts analyses. The site allows members of the working group to easily share and collaborate on the analyses using version control.

## Getting Started

You can find the pilot analysis plan in the [pilot-analysis-plan](https://github.com/expanse-admin-cohorts/pilot-analysis-plan) repository. You can ask questions related to the analysis by opening an issue in that repo.

### Repositories

>**Important**: Confidential data should not be stored in GitHub and therefore should not be version controlled. Make sure the possibly sensitive data files are included in your .gitignore file. Contact the GitHub Organization's maintainer when in doubt.

Each cohort should have its own repository within the Organization.

Consider naming your repository according to the following pattern:

```
<NAME INITIALS>_expanse-admin-pilot_<COHORT>
```

`<NAME INITIALS>` refers to the main person that will be writing the analysis code for each cohort. `<COHORT>` refers to a short name identifying the specific cohort.

In the case of the Spanish cohort containing data from the Catalunya region this would be: `SO_expanse-admin-pilot_catalunya`.

### Creating a new repository

1. Create a new private GitHub repo in this organization using the available template at [repo-template](). Note that this repo has common data folders and files included in its .gitignore file. Any sensitive files not covered by the template should added to this .gitignore file.

2. Clone this remote repository inside the appropriate folder in your machine. If using RStudio, use *`File > New Project > Version Control > Git`*.

3. Work on the analysis locally commiting when significant changes/additions have been made.

4. Push your commits to the remote repository regularly.

### Adding an existing non-Git repository

1. Create a .gitignore file. Make sure all possibly sensitive data files are included in this file.

2. Make your non-version controlled project a local Git repository.

3. Connect local repo to GitHub repo.

4. Work on the analysis locally commiting when significant changes/additions have been made.

5. Push your commits to the remote repository regularly.

### Adding an existing Git repository

1. Make sure the possibly sensitive data in your existing project has not been version controlled at any stage.

2. Create an *empty* GitHub repository with the same name as your existing project directory.

3. Connect local repo to GitHub repo.

4. Work on the analysis locally commiting when significant changes/additions have been made.

5. Push your commits to the remote repository regularly.
