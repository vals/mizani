##############
How to release
##############

Testing
=======

* `cd` to the root of project and run
  ::

    make test

* Or, to test in all environments
  ::

    tox

* Once all the tests pass move on





Tagging
=======

Check out the master branch, edit the changelog and add the tag
release date, tag with the version number & push the tags

  ::

    git checkout master
    vim doc/changelog.rst
    git add doc/changelog.rst
    git commit -m 'Prepare changelog for release'
    git tag -a v0.1.0 -m 'Version: 0.1.0'
    git push upstream --tags

Note the `v` before the version number.


Release
=======

* Make sure your `.pypirc` file is setup
  `correctly <http://docs.python.org/2/distutils/packageindex.html>`_.
  ::

    cat ~/.pypirc

* Release

 ::

    make release
