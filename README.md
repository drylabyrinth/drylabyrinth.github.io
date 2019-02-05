# OHSU Computational Forum Website

## Adding yourself to the forum

We want everyone who is interested to be a member of the Computational Forum, regardless of skill level or interest. All that's required is that you have a GitHub Id.

Before you add yourself, open these two links in another tab:

- [List of Departments](https://github.com/drylabyrinth/drylabyrinth.github.io/blob/master/_data/groups.yml)  
- [List of Research Interests](https://github.com/drylabyrinth/drylabyrinth.github.io/blob/master/_data/research_interests.yml)

1. Fork the repository and create a new branch with your name, such as "ted-laderas". You can do this on GitHub.

2. In the `_people` folder, create a new file with your name (you can use the "Create New File Button"). Make sure it ends with the `.md` extension, such as `ted-laderas.md`.

3. Paste the following template into your new file and fill it out. 

```
---
first_name: ""      
last_name: ""  
title: "Assistant Professor" #your title (use your primary one)
department: ["BME", "comp-bio"] #can have multiple departments  
research_interests: ["python", "comp-bio"] #can have multiple interests  
github: "" #just the id, like "laderast"
email: ""  #optional
link: "" #any url, include the https://  
excerpt: "" # a little bio - no more than 200 characters. We may integrate this.
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

## Adding a page

Adding a page is pretty easy. You can just add a `.md` at the root of the site, and it will show up. For example, I can create a `ideas.md` in the root of the folder, and you can see it at http://drylabyrinth.netlify.com/ideas/.

In order to add it to the menu, you'll have to edit the `_data/navigation.yml` file. 

## Adding your courses to the list

Coming soon - there will be an editable google sheet that will populate the course list.