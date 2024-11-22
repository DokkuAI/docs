---
icon: globe-pointer
---

# Contributing

We would ❤️ you to contribute to Appwrite and help make it better! We want contributing to Appwrite to be fun, enjoyable, and educational for anyone and everyone. All contributions are welcome, including issues, and new docs, as well as updates and tweaks, blog posts, workshops, and more.

Please take a moment to review this document before submitting your first pull request. We also strongly recommend that you check for open issues and pull requests to see if someone else is working on something similar.

### 🤔 Contribution Approach

We love pull requests from everyone! We follow the standard Git workflow of <mark style="color:orange;">**`fork`**</mark> 👉 <mark style="color:orange;">**`change`**</mark> 👉 <mark style="color:orange;">**`pull request`**</mark> 👉 <mark style="color:orange;">**`merge`**</mark> 👉 <mark style="color:orange;">**`update fork`**</mark> 👉<mark style="color:orange;">**`change`**</mark> ... (**repeat forever**). If you are new to open source, we recommend GitHub's excellent guide on "[How to Contribute to Open Source](https://opensource.guide/how-to-contribute/)". In addition, please feel free to reach out to any of the maintainers or other members if you are struggling; we are here to help you learn!

### 💡 Opening an Issue

If you're experiencing an issue with any project or have a question you'd like help answering, please feel free to open an issue in the respective repository of the project. To help us prevent duplicates, we kindly ask that you briefly search for your problem or question in our issues before opening a new one.

Please note that if you open a bug report and your issue does not follow our template, we cannot help you until you have provided us all the relevant information in that format. Respectfully, we do not have the time to try and recreate an error given with minimal or no context, so by providing this information you are helping us help you! You will see this template when you open an issue; click on "Bug Report" and it will be populated with descriptions of what to put in each section. Replace the descriptions with your comments to the best of your ability, and please include screenshots and error logs if applicable.

### 💻 Contributing to Source Code

#### Branching Convention

Branch naming convention is as following

`TYPE-ISSUE_ID-DESCRIPTION`

{% hint style="warning" %}
Description should not be more than 6 words
{% endhint %}

Example:

```
doc-548-submit-PR-to-contribution-guide
```

When `TYPE` can be:

* **`feat`** - a new feature
* **`doc`** - documentation only changes
* **`cicd`** - changes related to CI/CD system
* **`fix`** - a bug fix
* **`refactor`** - code change that neither fixes a bug nor adds a feature

#### Forking

For the initial start, you are required to fork the repository on your Github. Follow the [guidelines by GitHub](https://docs.github.com/en/free-pro-team@latest/github/getting-started-with-github/fork-a-repo) in order to understand the steps to fork any repository.

#### Cloning

You should use git clone command to download the repository to your computer.  This step is needed only once. Using [`dokkuai`](https://github.com/DokkuAI/dokkuai) as an example below;

```git
$ git clone github.com:your-username/dokkuai.git
$ cd dokkuai/
```

#### Syncing with Upstream

To ensure that your fork is always up-to-date with the original repository, add an upstream remote. This allows you to pull in changes that might have been merged into the main repository:

```git
$ git remote add upstream https://github.com/original-author/dokkuai.git
```

Whenever you start working on a new feature or fix, make sure your local master branch is up to date:

```git
$ git pull upstream master
```

#### Making Commits

Now that you have the repository on your local machine, you can start making the desired changes to the codebase. Once you have made the changes:

Create a new branch to implement your changes. This helps in isolating different changes and allows easy collaboration:

```git
$ git checkout -b TYPE-ISSUE_ID-DESCRIPTION
```

For example:

```git
$ git checkout -b doc-548-submit-PR-to-contribution-guide
```

Commit your changes using clear and meaningful messages. Writing a well-crafted Git commit message helps communicate the context of a change to other developers.

Example of committing changes:

```git
$ git add .
$ git commit -m "doc: update contribution guide with PR instructions"
```

Make sure to follow the [seven rules of a great Git commit message](https://cbea.ms/git-commit/) when crafting your messages.

**Pushing Changes**

After making and committing the changes, push your branch to your fork on GitHub:

```
$ git push origin TYPE-ISSUE_ID-DESCRIPTION
```

**Sending Pull Request**

Now that your changes are on GitHub, you need to create a **Pull Request (PR)** to submit your contribution to the main repository:

1. Go to your fork of the repository on GitHub.
2. Click the **Compare & pull request** button next to the branch you just pushed.
3. Fill out the **PR description** clearly explaining the purpose of your changes. Add any relevant issue numbers and a summary of what was done.

For more detailed steps, follow [GitHub's guide to creating a Pull Request](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request).

**Pulling Updates from Upstream**

Before creating a new branch or sending a PR, make sure to pull the latest changes from the upstream repository to keep your fork synchronized with the original project:

```
$ git pull upstream master
```

**Standard Procedure**

Before creating a new branch, make sure your local `master` branch is updated with the latest changes from the upstream repository:

```
$ git pull
```

**Review Process**

At this point, you're waiting on us. We like to at least comment on pull requests within three business days (and, typically, one business day). Once one of our maintainers has had a chance to review your PR, we will either mark it as "needs review" and provide specific feedback on your changes, or we will go ahead and complete the pull request.

We require all commits to be signed off with a [Developer Certificate of Origin](https://developercertificate.org/) in accordance with the DokkuAI Code of Conduct. This can be easily done by using the `-s` flag when using `git commit`. For example: `git commit -s -m "Update README.md"`. This can be automated by using a browser plugin like [DCO GitHub UI](https://github.com/scottrigby/dco-gh-ui).

{% hint style="info" %}
**NOTE**: Any pull requests containing commits that are not signed off will not be eligible for merge until the commits have been signed off.
{% endhint %}
