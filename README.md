# About

This repository contains a knowledgebase of repair app. It's built on [Hugo](https://gohugo.io/), based on great [Matcornic Learn theme](https://github.com/matcornic/hugo-theme-learn/).

Visit the [theme documentation](http://docdock.netlify.com/) to see what is going on. It is actually built with this theme. 

## Prerequisite 
* Go
* Hugo 
* Markdown

## Contribution 

You can refer theme [documentation](http://docdock.netlify.com/) for generating various pages.

We will go through each of our features (i.e tickets, invoices, customers etc) and create pages for the same.

Let me give you an example to create pages of appointments:

* Go to terminal execute below command
` hugo new appointments/_index.md` ( we will need _index.md in each of the folder we create. )

* All the new pages will be in drafts mode, go to your file and remove drafts tag and add `weight = 1` and `alwaysopen = true`

