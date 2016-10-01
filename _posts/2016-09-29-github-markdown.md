---
layout: post
nav: true
title: Github Markdown
category: computer
tags: [github, markdown]
---
## Getting started with writing and formatting on Github
You can use simple features to format your comments and interact with others in issues, pull requests, and wikis on GitHub.

### About writing and formatting on Github
GitHub combines a syntax for formatting text called GitHub Flavored Markdown with a few unique writing features.

[Markdown](http://daringfireball.net/projects/markdown/) is an easy-to-read, easy-to-write syntax for formatting plain text.

We've added some custom functionality to create GitHub Flavored Markdown, used to format prose and code across our site.

You can also interact with other users in pull requests, issues, and wikis with features like [@mentions](https://help.github.com/articles/basic-writing-and-formatting-syntax/#mentioning-users-and-teams), [issue and PR references](https://help.github.com/articles/basic-writing-and-formatting-syntax/#referencing-issues-and-pull-requests), and [emoji](https://help.github.com/articles/basic-writing-and-formatting-syntax/#using-emoji).

#### Text formatting toobar
Every comment field on GitHub contains a text formatting toolbar, allowing you to format your text without learning Markdown syntax. In addition to Markdown formatting like bold and italic styles and creating headers, links, and lists, the toolbar includes GitHub-specific features such as @mentions, task lists, and links to issues and pull requests.

![Markdown toolbar](https://help.github.com/assets/images/help/writing/markdown-toolbar.gif)

#### Further reading
- "[Basic writing and formatting syntax](https://help.github.com/articles/basic-writing-and-formatting-syntax)"
- "[Working with advanced formatting](https://help.github.com/articles/working-with-advanced-formatting)"
- "[Mastering Markdown](https://guides.github.com/features/mastering-markdown/)"
- "[Markdown Tutorial](http://markdowntutorial.com/)"

### Basic writing and formatting syntax
Create sophisticated formatting for your prose and code on GitHub with simple syntax.

#### Headings
To create a heading, add one to six # symbols before your heading text. The number of # you use will determine the size of the heading.

```
# The largest heading
## The second largest heading
###### The smallest heading
```
![Rendered H1, H2, and H6 headings](https://help.github.com/assets/images/help/writing/headings-rendered.png)

#### Styling text
You can indicate emphasis with bold, italic, or strikethrough text.

|  Style  |  Syntax  |  Keyboard shortcut  | Example | Output  |
|:---     |:---      |:---                 |:---     |:---     |
|Bold|`** **` or `__ __` |command/control + b|`**This is bold text**`|**This is bold text**|
|Italic|`* *` or `_ _`|command/control + i|`*This text is italicized*`|*This text is italicized*|
|Strikethrough|`~~ ~~`|	|`~~This was mistaken text~~`|~~This was mistaken text~~|
|Bold and italic|`** **` and` _ _`| |`**This text is _extremely_ important**`|	**This text is _extremely_ important**|


#### Quoting text
You can quote text with a `>`.

```
In the words of Abraham Lincoln:
> Pardon my French
```
![Rendered quoted text](https://help.github.com/assets/images/help/writing/quoted-text-rendered.png)

#### Quoting code
You can call out code or a command within a sentence with single backticks. The text within the backticks will not be formatted.

```
Use `git status` to list all new or modified files that haven't yet been committed.
```

![Rendered inline code block](https://help.github.com/assets/images/help/writing/inline-code-rendered.png)

To format code or text into its own distinct block, use triple backticks.

```
	Some basic Git commands are:
	```
	git status
	git add
	git commit
	```
```
![Rendered code block](https://help.github.com/assets/images/help/writing/code-block-rendered.png)

For more information, see "[Creating and highlighting code blocks](https://help.github.com/articles/creating-and-highlighting-code-blocks)."

#### Links
You can create an inline link by wrapping link text in brackets `[ ]`, and then wrapping the URL in parentheses `( )`. You can also use the keyboard shortcut `command + k` to create a link.

```
This site was built using [GitHub Pages](https://pages.github.com/).
```

![Rendered link](https://help.github.com/assets/images/help/writing/link-rendered.png)

#### Lists
You can make a list by preceding one or more lines of text with `-` or `*`.

```
- George Washington
- John Adams
- Thomas Jefferson
```

![Rendered unordered list](https://help.github.com/assets/images/help/writing/unordered-list-rendered.png)

To order your list, precede each line with a number.

```
1. James Madison
2. James Monroe
3. John Quincy Adams
```

[Rendered ordered list](https://help.github.com/assets/images/help/writing/ordered-list-rendered.png)

You can create nested lists by indenting lines by two spaces.

```
1. Make my changes
  1. Fix bug
  2. Improve formatting
    * Make the headings bigger
2. Push my commits to GitHub
3. Open a pull request
  * Describe my changes
  * Mention all the members of my team
    * Ask for feedback
```

![Rendered nested list](https://help.github.com/assets/images/help/writing/nested-list-rendered.png)

#### Task lists
You can create [task lists](https://github.com/blog/1375%0A-task-lists-in-gfm-issues-pulls-comments) by prefacing list items with `[ ]`. To mark a task as complete, use `[x]`.

Task lists render with checkboxes in all comments and Markdown files. Select or unselect the checkboxes to mark them as complete or incomplete.

```
- [x] Finish my changes
- [ ] Push my commits to GitHub
- [ ] Open a pull request
```

![Rendered task list](https://help.github.com/assets/images/help/writing/task-list-rendered.png)

You can reorder task lists by clicking to the left of a task's checkbox, dragging it to a new location, and dropping it. If you have multiple lists within a comment, you can reorder tasks across them. You can't add or reorder tasks in other comments.

![Reordered task list](https://help.github.com/assets/images/help/writing/task-list-reordered.gif)

#### Mentioning users and teams
You can mention a user or [team](https://help.github.com/articles/setting-up-teams/) on GitHub by typing `@` plus their username or team name to bring their attention to an issue or pull request.

```
@github/support What do you think about these updates?
```

![Rendered @mention](https://help.github.com/assets/images/help/writing/mention-rendered.png)

Typing an `@` symbol will bring up a list of people or teams on a project. The list filters as you type, so once you find the name of the person or team you are looking for, you can use the arrow keys to select it and hit either tab or enter to complete the name. For teams, just enter the @organization/team-name and all members of that team will get subscribed to the issue.

The autocomplete results are restricted to repository collaborators and any other participants on the thread.

#### Referencing issues and pull requests
You can bring up a list of suggested Issues and Pull Requests within the repository by typing `#`. Type the issue or PR number or title to filter the list, then hit either tab or enter to complete the highlighted result.

For more information, see "[Autolinked references and URLs](https://help.github.com/articles/autolinked-references-and-urls)."

#### Using emoji
You can add emoji to your writing by typing `:EMOJICODE:`.

```
@octocat :+1: This PR looks great - it's ready to merge! :shipit:
```

![Rendered emoji](https://help.github.com/assets/images/help/writing/emoji-rendered.png)

Typing `:` will bring up a list of suggested emoji. The list will filter as you type, so once you find the emoji you're looking for, press **Tab** or **Enter** to complete the highlighted result.

For a full list of available emoji and codes, check out [emoji-cheat-sheet.com](http://emoji-cheat-sheet.com/).

#### Paragraphs and line breaks
You can create a new paragraph by leaving a blank line between lines of text.

#### Ignoring Markdown formatting
You can tell GitHub to ignore (or escape) Markdown formatting by using `\` before the Markdown character.

```
Let's rename \*our-new-project\* to \*our-old-project\*.
```

![Rendered escaped character](https://help.github.com/assets/images/help/writing/escaped-character-rendered.png)

#### Further reading
- "[About writing and formatting on GitHub](https://help.github.com/articles/about-writing-and-formatting-on-github)"
- "[Working with advanced formatting](https://help.github.com/articles/working-with-advanced-formatting)"
- "[Mastering Markdown](https://guides.github.com/features/mastering-markdown/)"
- "[Markdown Tutorial](http://markdowntutorial.com/)"

## Working with advanced formatting
Formatting like tables, syntax highlighting, and automatic linking allows you to arrange complex information clearly in your pull requests, issues, and comments.

### Organizing information with tables
You can build tables to organize information in comments, issues, pull requests, and wikis.

#### Creating a table
You can create tables with pipes `|` and hyphens `-`. Hyphens are used to create each column's header, while pipes separate each column.

```
| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |
```

![Rendered table](https://help.github.com/assets/images/help/writing/table-basic-rendered.png)

The pipes on either end of the table are optional.

Cells can vary in width and do not need to be perfectly aligned within columns. There must be at least three hyphens in each column of the header row.

```
| Command | Description |
| --- | --- |
| git status | List all new or modified files |
| git diff | Show file differences that haven't been staged |
```

![Rendered table with varied cell width](https://help.github.com/assets/images/help/writing/table-varied-columns-rendered.png)

#### Formatting content within your table
You can use [formatting](https://help.github.com/articles/basic-writing-and-formatting-syntax) such as links, inline code blocks, and text styling within your table:

```
| Command | Description |
| --- | --- |
| `git status` | List all *new or modified* files |
| `git diff` | Show file differences that **haven't been** staged |
```

![Rendered table with formatted text](https://help.github.com/assets/images/help/writing/table-inline-formatting-rendered.png)

You can align text to the left, right, or center of a column by including colons : to the left, right, or on both sides of the hyphens within the header row.

```
| Left-aligned | Center-aligned | Right-aligned |
| :---         |     :---:      |          ---: |
| git status   | git status     | git status    |
| git diff     | git diff       | git diff      |
```

![Rendered table with left, center, and right text alignment](https://help.github.com/assets/images/help/writing/table-aligned-text-rendered.png)

To include a pipe `|` as content within your cell, use a `\` before the pipe:

```
| Name     | Character |
| ---      | ---       |
| Backtick | `         |
| Pipe     | \|        |
```

![Rendered table with an escaped pipe](https://help.github.com/assets/images/help/writing/table-escaped-character-rendered.png)

#### Further reading
- "[Basic writing and formatting syntax](https://help.github.com/articles/basic-writing-and-formatting-syntax)"

### Creating and highlighting code blocks
Share samples of code with fenced code blocks and enabling syntax highlighting.

#### Fenced code blocks
You can create fenced code blocks by placing triple backticks ```` before and after the code block. We recommend placing a blank line before and after code blocks to make the raw formatting easier to read.

```
	```
	function test() {
	  console.log("notice the blank line before this function?");
	}
	```
```

![Rendered fenced code block](https://help.github.com/assets/images/help/writing/fenced-code-block-rendered.png)

#### Syntax highlighting
You can add an optional language identifier to enable syntax highlighting in your fenced code block.

For example, to syntax highlight Ruby code:

```
	```ruby
	require 'redcarpet'
	markdown = Redcarpet.new("Hello World!")
	puts markdown.to_html
	```
```

![Rendered code block with Ruby syntax highlighting](https://help.github.com/assets/images/help/writing/code-block-syntax-highlighting-rendered.png)

We use [Linguist](https://github.com/github/linguist) to perform language detection and syntax highlighting. You can find out which keywords are valid in [the languages YAML file](https://github.com/github/linguist/blob/master/lib/linguist/languages.yml).

#### Further reading
- "[Basic writing and formatting syntax](https://help.github.com/articles/basic-writing-and-formatting-syntax)"

### Autolinked references URLs
References to URLs, issues, pull requests, and commits are automatically shortened and converted into links.

#### URLs
GitHub automatically creates links from standard URLs.

```
Visit https://github.com
```

For more information on creating links, see "[Basic writing and formatting syntax](https://help.github.com/articles/basic-writing-and-formatting-syntax/#links)."

#### Issues and pull requests
Within repositories, references to issues and pull requests are automatically converted to shortened links to the issue or pull request.

| Reference type | Raw reference | Short link |
|: ---           |:---           |:---        |
|Issue or pull request URL|<https://github.com/jlord/sheetsee.js/issues/26>|[#26](https://github.com/jlord/sheetsee.js/issues/26)|
|`#`and issue or pull request number|#26|[#26](https://github.com/jlord/sheetsee.js/issues/26)|
|`GH-`and issue or pull request number||#26|[#26](https://github.com/jlord/sheetsee.js/issues/26)|
|`Username#`and issue or pull request number||jlord#26|[jlord#26](https://github.com/jlord/sheetsee.js/issues/26)|
|`Username/Repository`and issue or pull request number||jlord/sheetsee.js#26|[jlord/sheetsee.js#26](https://github.com/jlord/sheetsee.js/issues/26)|

#### Commit SHAs
References to a commit's SHA hash are automatically converted into shortened links to the commit on GitHub.

## Working with saved replies
To save time and make sure you're delivering a consistent message, you can add saved replies to issue and pull request comments.

Once you've [added a saved reply](https://help.github.com/articles/creating-a-saved-reply), it can be [used in both issues and pull requests](https://help.github.com/articles/creating-a-saved-reply). Saved replies are tied to your user account. Once they're created, you'll be able to use them across repositories and organizations.

### Creating a saved reply
If you frequently add the same comment over and over, you can create a saved reply.

### Changing a saved reply
If you have a saved reply that has an error or isn't saying exactly what you'd like, you can make it more useful by changing it.

### Deleting a saved reply
If you find that you're no longer using a saved reply, you can delete it.

### Using saved replies
When commenting on an issue or pull request, you can add a saved reply that you've already set up. The saved reply can be the entire comment or if you want to customize it, you can add or delete content.


> View the original page: <https://help.github.com/categories/writing-on-github/>
{: .thanks}
