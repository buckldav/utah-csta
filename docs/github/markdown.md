---
sidebar_position: 1
---

# GitHub and Markdown

Coders are writers of code and technical documentation. They need to be able to share content and communicate quickly. These tools will help you do that.

- **GitHub** is the #1 cloud platform for storing, sharing, and versioning code. Think of it like Google Drive for developers, with some extra CS-specific features.
- **Markdown** is the language for writing documentation and other CS-related content. This page was [written in Markdown](https://github.com/buckldav/utah-csta/tree/master/docs/github/markdown.md)!

We will dive into Markdown first, which we will use to provide `README.md` files (containing instructions for usage and descriptions of functionality) to our code projects.

## Markdown

With Markdown, you can format plain text to look like headings, links, images, and more!

<details markdown="block">
  <summary>Show Markdown Example</summary>

```markdown
# Heading 1

## Heading 2

...

##### Heading 5

###### Heading 6

This is a paragraph.

[link text](https://example.com)

![image alt text](https://linktoimage.png)

- Bulleted list 1
- Bulleted list 2

1. Numbered list 1
2. Numbered list 2
```

</details>

<details markdown="block">
  <summary>Show Example Output</summary>

<div style={{"height": "400px", "overflow": "scroll"}} markdown="block">

# Heading 1

## Heading 2

...

##### Heading 5

###### Heading 6

This is a paragraph.

[link text](https://example.com)

<img src="https://cdn2.thecatapi.com/images/MTgyNTkyNw.jpg" style={{"height": "150px"}} />

<ul style={{"list-style":"disc"}}>
<li>Bulleted list 1</li>
<li>Bulleted list 2</li>
</ul>

1. Numbered list 1
2. Numbered list 2

</div>
</details>

### Try Markdown Yourself

1. [Markdown Cheat Sheet](https://www.markdownguide.org/cheat-sheet/)
2. [Online Markdown Editor](https://dillinger.io)

## GitHub

If you haven't already, create an account on [github.com](https://github.com).

### Create Your First Git Repository

Once logged in, on the left side of the screen, click the green "New" repository button.

![New Repository](/utah-csta/img/github/newrepo.png)

> IMPORTANT: Name the repository the same name as your username.

This will make this your GitHub profile README repository. Here, you can put information about yourself. Be sure to check the "Add a README file" box (circled in red below). Then, click "Create Repository" at the bottom of the page.

![Global README](/utah-csta/img/github/easteregg.png)

You can then Edit the README.md file by clicking the pencil icon or the "Edit README" green button.

![Edit README](/utah-csta/img/github/editbutton.png)

Add your content here and toggle the "Edit file" and "Preview" tabs to add Markdown and see what it looks like.

![Editing page](/utah-csta/img/github/edit.png)

### Resources

- 🚀 Add some colored emojis from [Emojipedia](https://emojipedia.org/)
- 📃 Here's that [Markdown cheat sheet again](https://www.markdownguide.org/cheat-sheet/)

#### Commit = Save

When finished, scroll down to **commit** your changes. In the **git** code management tool (used by GitHub), a "commit" is a savepoint. Commits require brief messages that describe what changes were made.

![Commit](/utah-csta/img/github/commit.png)

#### [Mr. Buckley's README.md](https://github.com/buckldav)

![buckldav README](/utah-csta/img/github/buckldav.png)
