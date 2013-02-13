# Informatics blog howto

The source of the blog is kept in the 'source' branch, and the generated pages are published to the 'gh-pages' branch. This strategy is referred to as ["With Github Project pages (gh-pages)"](http://octopress.org/docs/deploying/github/)

## Getting started

In order to publish to Informatics UNEP-WCMC blog, please start by cloning this directory:

    git clone git@github.com:unepwcmc/blog.git

Next, you need to run a command to set up deployment:

    rake setup_github_pages

When it asks you for url repo, enter: git@github.com:unepwcmc/blog (without the ending .git)

Due to an [issue in octopress](https://github.com/imathis/octopress/issues/1025) you now need to revert the changes to blog url configuration:

    git checkout _config.yml

## Writing a new post

    rake new_post["my great new post"]

This command will create the new post file and place it in the octopress date-driven directory structure. You can then edit this file using plain html / markdown.

There is a similar command to create a new page.

## Previewing

    rake preview

This starts a local server, you can preview the blog at localhost:4000/blog

## Publishing vs pushing

After any changes to the blog you can publish them to [the   repo using:

    rake generate
    rake deploy

However, you still need to push the source:

    git add .
    git commit -m "my commit msg"
    git push origin source

## License
(The MIT License)

Copyright © 2009-2011 Brandon Mathis

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the ‘Software’), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED ‘AS IS’, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

