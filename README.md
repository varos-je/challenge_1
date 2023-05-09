# Challenge 1 - HTML, CSS, Git
### by James Varos

#### Github repository: https://github.com/varos-je/challenge_1
#### Github Pages: https://varos-je.github.io/challenge_1/

## Description
The basis of this project is a drafted home page for a fictitious company, Horiseon. The basis already included an .html file, a .css file, and several images that appear on the home page, but the previous code was not as 'accessible' as it should be. Addutionally, the user-facing look of the home page following my edits should look identical to the mockup with accessibility issues (see desired mockup in "Visuals").

As a developer, I took the existing code and refactored it to meet the following user stories (and their accompanying acceptance criteria):

### User Story

```
AS A marketing agency
I WANT a codebase that follows accessibility standards
SO THAT our own site is optimized for search engines
```

### Acceptance Criteria

```
GIVEN a webpage meets accessibility standards
WHEN I view the source code
THEN I find semantic HTML elements
WHEN I view the structure of the HTML elements
THEN I find that the elements follow a logical structure independent of styling and positioning
WHEN I view the image elements
THEN I find accessible alt attributes
WHEN I view the heading attributes
THEN they fall in sequential order
WHEN I view the title element
THEN I find a concise, descriptive title
```

## Visuals
As previously mentioned, the user-facing look of the home page following my edits should look identical to the mockup with accessibility issues:

![As previously mentioned, the user-facing look of the home page following my edits should look identical to the mockup with accessibility issues:](./Assets/01-html-css-git-homework-demo.png)

## Changes

### Semantics

All `<div>` in index.html have been replaced with more descriptive semantic elements that follow the order of the home pages content, including (in order): 

```
<header>
    <nav>
<figure>
<main>
    <section>
<aside>
    <section>
<footer>

```

Many sections of the unedited index.html and style.css files contained repetitive - and sometimes unnecessary - class and id attributes. 

For example, the following code in the unedited style.css contained the following code to provide specificities to images in the 'benefits' section: 

```
.benefit-lead img {
    display: block;
    margin: 10px auto;
    max-width: 150px;
}

.benefit-brand img {
    display: block;
    margin: 10px auto;
    max-width: 150px;
}

.benefit-cost img {
    display: block;
    margin: 10px auto;
    max-width: 150px;
}
```

The current version fixes these repetitive descriptors by removing the class attribute from `.benefit` and its accompanying child attributes, changing the `<div>` element to the more descriptive `<aside>`, and condensing the code into a single attribute that can be applied to all images within `<aside>`:

```
/* consolidated all .benefit-xxxx img because same values */
aside img {
    display: block;
    margin: 10px auto;
    max-width: 150px;
}
```

## Authors and acknowledgments
I'd like to thank edX and its supporting developers, teachers, and staff for providing lessons and starter code from which this project is derived.

## License
There is no license on this project.

## Project status
This project may be revisited if outside parties (i.e. bootcamp graders) find reason for necessary changes.
