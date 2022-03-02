#README for the LDaCA website

The theme used is [LoveIt theme](https://hugoloveit.com/){:target="_blank"} and has been customised throughout. The theme installation is a sub-module and alterations have been made in many different places.

- Customised SCSS files are located in the assets folder.
- Customised layouts in the layout folder.
- Xconfig.toml is an exemplar TOML file including settings that have not be utilised in the ATAP website build (yet).

Because the theme is installed as a sub-module - do not manually commit this to the ATAP-website repo or make any changes in the theme itself. Moises will probably cry if this happens again (Leah has already accidentally pushed him to the edge!)

##Adding and changing content

There shouldn't be any more layout changes needed to the site. 

All the content is in markdown files in the content folder. The
[Markdown Cheat Sheet](https://www.markdownguide.org/cheat-sheet/){:target="_blank"} is very helpful when formatting using markdown! HTML tags can also be used for formatting, just be aware that HTML and markdown often don't play nicely without a blank line in between them. The [LoveIt Extended Shortcodes](https://hugoloveit.com/theme-documentation-extended-shortcodes/){:target="_blank"} page may help with some of this as well.

New markdown pages created in the content folder will need to be linked to from one of the primary pages (Blog, Text Analysis, Resources, and Organisation). New markdown files generated within the posts folder will automatically show up on the blog page.

Use the front matter! Drafts need to be set to false, otherwise they won't show up on the site. There are two taxonomies defined for classifying content and getting it to show up in the search. 

All the images are stored in the static folder. To display on a page use
{{ .Site.BaseURL }}/ImageName.png within the appropriate HTML tags or markdown.

##Committing those changes

All commits should go to the master branch of the ATAP-website repository. There is a workflow that pushes master commits to the the gh-pages branch automatically.

These instructions are for after your own local .git has been set up. The repo uses SSH so you will need a key.

To push changes to the repo. Check first with 'code' git status 
to check what changes have been made.

git add .
git commit -m " Whatever notes describe the changes in the commit "
git push

If the submodule needs to be updated, run the following git command:
'code' git submodule update --init --recursive

