# Remove Directory from the Remote Repository

The rules in your .gitignore file only apply to untracked files. Since the files
under that directory were already committed in your repository, you have to
unstage them, create a commit, and push that to GitHub:

git rm -r --cached some-directory
git commit -m 'Remove the now ignored directory "some-directory"'
git push origin master

Additionally, note the output from git rm -r --cached some-directory will be
something like:

rm 'some-directory/product/cache/1/small_image/130x130/small_image.jpg'
rm 'some-directory/product/cache/1/small_image/135x/small_image.jpg'
rm 'some-directory/.htaccess'
rm 'some-directory/logo.jpg'
The rm is feedback from git about the repository; the files are still in the
working directory.

