# assets.okfn.se
m.okfn.org: OKFN media server Files

Here we keep our media assets, such as vector files and large graphics used in publicity and in webdesign.

The content of this repo is deployed on Amazon S3 at http://assets.okfn.org and can be linked to from live websites.

Note: For general blogging purposes, use our Flickr account to link to images and photographs.

General layout

/ # default
  img/ # or images may symlink ...
  css/
  js/
  xsl/
  ....
  files/
p/{project-name}
  img/
  css/
  js/
  xsl/
  ....
{project-name}/ - DEPRECATED - please use p/{project-name}
  img/
  css/
  js/
  xsl/
  ....
ext/ # external libraries
  {library-name}/
    {library-files} e.g. jquery-1.4.2.js
    # or where no single set of files for a given version
    {version}/
      {library-files}
Usage

In general, everything should be in this repo but in some cases this is not feasible in which case you must provide explicit instructions either here or in a separate README as to what files need to be fetched and placed where (you could even provide a script which does the job automatically).

okftext
Check out okftext subversion reposistory from knowledgeforge. Then symlink trunk/dist to okftext.

Deploying to S3

./sync.sh
