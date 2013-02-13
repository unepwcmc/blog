# Informatics blog howto

We're using the blog deploying strategy described here: http://octopress.org/docs/deploying/github/ under "With Github Project pages (gh-pages)"

## Getting started

In order to publish to Informatics UNEP-WCMC blog, please start by cloning this directory:

  git clone git@github.com:unepwcmc/blog-src.git


Now there must be a simpler way to go from there, but while I haven't found out please foolow these steps: 

Next, you need to configure octopress so that it knows to deploy the blog to the 'blog' repo gh-pages branch:

  cd blog-src
  rake setup_github_pages

When asked for a repository url, enter: git@github.com:unepwcmc/blog.git

Now this might have the side effect of changing the blog url in _config.tml file -- please open that file and make sure it has:

  url: http://informatics.unep-wcmc.org/blog

## Writing a new post

  rake new_post["my great new post"]

This command will create the file for you and place it in the octopress date-driven directory structure. You can then edit this file using plain html / markdown.

## Previewing

  rake preview

This starts a local server, you can preview the blog at localhost:4000/blog

## Publishing vs pushing

After any changes to the blog you can publish them to the 'blog' repo using:

  rake generate
  rake deploy

However, that does not push to 'blog-src', you need to do that manually:

  cd blog-src
  git add .
  git commit -m "my commit msg"
  git push origin source


## License
(The MIT License)

Copyright © 2009-2011 Brandon Mathis

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the ‘Software’), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED ‘AS IS’, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

