+----------------------------------+------------------------+----------+
| ![](vertopal_                    |                        |          |
| c4eeb71d263543689004798449f53e87 |                        |          |
| /media/image1.png){width="2.4in" |                        |          |
| height="0.5881944444444445in"}   |                        |          |
|                                  |                        |          |
| SCHOOL OF INFORMATION AND        |                        |          |
| TECHNOLOGY                       |                        |          |
+----------------------------------+------------------------+----------+
| NAME: TALUSIG, NIKOS A.          | DATE PERFORMED:        |          |
|                                  | 11/21/24               |          |
+----------------------------------+------------------------+----------+
| Section: IDC2                    | DATE SUBMITTED:        |          |
|                                  | 11/21/24               |          |
+----------------------------------+------------------------+----------+

# SYSADM1 -- Git Basics

Answer the following research questions about Git, GitLab desktop and
GitHub.

1.  What is Git, and why is it important in software development?

-   Git is a distributed version control system that allows multiple
    developers to work on a project simultaneously. It manages changes
    to files and coordinates work among teams, enabling efficient
    collaboration. Git's importance in software development comes from
    its ability to track changes; allowing developers to revert to
    previous versions if necessary, branch and merge; create branches
    for new features which can later be merged back into the main
    database, and collaboration; allows developers to work independently
    on their local copes before integrating change with others.

2.  How does Git track changes in a project?

-   Git tracks changes through a system of snapshot. Each time a
    developer commits changes, Git creates a snapshot of the current
    state of the project.

3.  What is the difference between a local repository and a remote
    repository in Git?

-   A local repository includes copies of projects stored on a
    developer's local device, allowing for offline work and testing
    before pushing changes to a shared location. As for remote
    repository, this is hosted on a server like GitHub or GitLab and
    serves as a central point for collabotion.

4.  What are the basic Git commands?

-   'git init': Create a new local repository.

-   'git clone \<repository\>': Clone an existing remote repository.

-   'git add \<file\>': Stage changes for commit.

-   'git commit --m "message" ': Commit staged changes with a message.

-   'git push origin \<branch\>': Push local commits to the specified
    branch on the remote repository.

-   'git pull': Fetch and merge changes from the remote repository into
    the local branch.

-   'git status': Check the status of files in the working directory.

5.  How do you check the status of a Git repository?

-   To check the status of a Git repository, use the command 'git
    status'.

6.  What is the purpose of branches in Git, and how do you create and
    switch between them?

-   Branches in Git allow developers to work on different features or
    fixes in isolation from one another. This helps maintain stability
    while enabling parallel development. To create a new branch; use the
    command 'git checkout --b \<branch name\>. To switch to an existing
    branch; use the command 'git checkout \<branch name\>. To list all
    branches; use the command 'git branch'.

7.  What are GitLab Desktop and GitHub, and how are they different from
    Git?

-   GitHub and GitLab are web-based platforms that provide hosting for
    Git repositories alongside additional features such as issues
    tracking, project management tools, and CI/CD piplines. GitHub
    primarily focuses on open-sources projects and has extensive
    community features like pull requests and social coding. GitLab on
    the other hand offers integrated CI/CD capabilities directly within
    its platform, making it suitable for DevOps practices.

8.  How do you connect a local Git repository to a GitLab or GitHub
    repository?

-   To connect a local repository to a remote repository, use the
    command 'git remote add origin \<repository url\>.

9.  What are the steps to collaborate with others using GitLab or
    GitHub?

-   Clone the repository: Use the command 'git clone \<repository url\>
    to get a copy of the project.

-   Create a new branch: Use the command 'git checkout --b \<branch
    name\> for features or fixing.

-   Make changes and commit: Use the command 'git add' and 'git commit'.

-   Push branch: Use the command 'git push origin \<branch name\>' to
    upload changes to remote repository.

> These process allows team members to review each other's work before
> integration into the main codebase.

10. How do you resolve merge conflicts in Git?

-   To resolve merge conflicts, open the conflicted files and edit them
    to combine changes as needed, removing the conflict markers. Once
    resolved, use 'git add \<file\>' to mark the conflicts as resolved
    and complete the merge with 'git commit'. If needed, abort the merge
    with 'git merge --abort' and try again.

11. What is a pull request, and why is it used in GitHub?

-   A pull request is made by one developer to merge their branch into
    another branch---usually the main branch---on platforms like GitHub.
    It serves several purposes such as facilitation of code review, and
    provides opportunity for discussion about implementation details
    before final integration.

12. What are some best practices for writing commit messages?

-   Some best practices include keeping the messages concise---ideally
    under 50 characters, include detailed explanations if necessary, and
    reference relevant issues or pull requests when applicable.
    Following these practices helps maintain clarity about project
    history and facilitates easier navigation through commits.

***[References:]{.underline}***

Haffiyan, R. D. (2020, March 9). *Why Git is important in software
development?*
https://www.linkedin.com/pulse/why-git-important-software-development-razaqa-dhafin-haffiyan

*Git - Recording changes to the repository*. (n.d.).
https://git-scm.com/book/ms/v2/Git-Basics-Recording-Changes-to-the-Repository

GeeksforGeeks. (2024, July 3). *Working with Git repositories*.
GeeksforGeeks.
https://www.geeksforgeeks.org/working-with-git-repositories/

*Basic Git commands \| Bitbucket Data Center 9.3 \| Atlassian
Documentation*. (n.d.). Atlassian Documentation.
https://confluence.atlassian.com/bitbucketserver/basic-git-commands-776639767.html
