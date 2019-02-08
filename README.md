# OHSU Computational Forum Website

## Adding yourself to the forum

We want everyone who is interested to be a member of the Computational Forum, regardless of skill level or interest. All that's required is that you have a GitHub Id.

Before you add yourself, open these two links in another tab:

- [List of Departments](https://github.com/drylabyrinth/drylabyrinth.github.io/blob/master/_data/groups.yml)  
- [List of Research Interests](https://github.com/drylabyrinth/drylabyrinth.github.io/blob/master/_data/research_interests.yml)

1. Fork the repository and create a new branch with your name, such as "ted-laderas". You can do this on GitHub.

2. In the `_people` folder, create a new file with your name (you can use the "Create New File Button"). Make sure it ends with the `.md` extension, such as `ted-laderas.md`.

3. Paste the following template into your new file and fill it out. Note that the `---` before and after the text is important. If this is not included, your profile will not show.

```
---
first_name: ""      
last_name: ""  
#your title (use your primary one)
title: "Assistant Professor" 
#can have multiple departments
department: ["BME", "comp-bio"]   
#can have multiple interests 
research_interests: ["python", "comp-bio"]  
#just the id, like "laderast"
github: ""
#optional email - delete this line if you don't want to include it
email: ""
#any url, include the https:// 
link: ""   
# a little bio - no more than 200 characters. We may integrate this.
excerpt: "" 
---
```
4. Make sure that the entry in the `department:` field matches the `acronym` field for your department in the `_data/groups.yml` file. For example, in the `_data/groups.yml` file, you can see that `Department of Medical Informatics and Clinical Epidemiology` has the acronym `DMICE`. You can have multiple departments by separating them with a `,`.

5. Make sure that the entry in the `research_interests:` field matches the `tag` field for your research interests. Again, you can have multiple interests by separating them with a `,`.

If you have a github id and it has a profile photo, it will be included in your card on the `people` page. 

6. When you're done, submit a pull request to the `master` repo of `drylabyrinth.github.io`. You can preview what your changes looks like by clicking the `deploy preview`. Make sure that the change works. We will make sure your pull request works and merge it into the site.

## Adding your department/group/program to the site

We welcome everyone who wants to participate in the computational forum. You can quickly add your group by adding to the [groups.yml](https://github.com/drylabyrinth/drylabyrinth.github.io/blob/master/_data/groups.yml) file.

1. Fork the repository by hitting the fork button on the top right of the main repository page.
2. Make a new branch, such as "add-my-department".
3. Add a new entry to the `_data/groups.yml` file by cutting and pasting the template below into the file. You can edit the file directly on GitHub by clicking on the pencil icon in the top of the text window.

```
- name: ""
  acronym: ""
  url: ""
  excerpt: "" #no line breaks, please. keep this short, 2-3 sentences max.
```
4. Submit a pull request to our repo from your fork. When you've set up the pull request, you can see your changes by clicking on the `deploy preview`. We will review your request, make any needed fixes, and have it up as soon as possible.

## Adding a research interest

We want people to populate the [research interest list](https://github.com/drylabyrinth/drylabyrinth.github.io/blob/master/_data/research_interests.yml). We've added a few, but feel free to add more. Try to avoid too much granularity - we're trying to find commonalities and make the list easier to search.

1. Fork the repository by hitting the fork button on the top right of the main repository page.
2. Make a new branch, such as "add-my-interest".
3. Add a new entries to the `_data/research_interests.yml` file by cutting and pasting the template below into the file. You can edit the file directly on GitHub by clicking on the pencil icon in the top of the text window.

```
- name: ""
  tag: ""
```

4. Submit a pull request to our repo from your fork. When you've set up the pull request, you can see your changes by clicking on the `deploy preview`. 

## Adding a page to the site

Adding a page is pretty easy. You can just add a `.md` at the root of the site, and it will show up. For example, I can create a `ideas.md` in the root of the folder, and you can see it at http://drylabyrinth.netlify.com/ideas/.

In order to add it to the menu, you'll have to edit the `_data/navigation.yml` file. 

## Editing a page on the site

Each page mostly corresponds to a `.md` file. For example, the education page is at [`/education.md`](https://github.com/drylabyrinth/drylabyrinth.github.io/blob/master/education.md). You can make edits to any page and make a pull request. 

## Adding your courses to the list

Coming soon - there will be an editable google sheet that will populate the course list.

## Acknowledgements

This website is built from the [minimal-mistakes template](https://mmistakes.github.io/minimal-mistakes/). Code for the people page was adapted from https://github.com/cagrimmett/jekyll-tools. CSS card template was adapted from https://codepen.io/Masquetina/pen/dYYxeM/. 

This website uses JQuery, Isotope, and ImagesLoaded.
