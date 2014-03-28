# test-case-berkshelf-cookbook

This is just a test repo to validate some Berkshelf behaviour.

## Issue:

    $ rm -rf ~/.berkshelf/.cache/
    $ rm -rf ~/.berkshelf/cookbooks/{one,two}-*
    $ cd test-case-berkshelf-1081/
    $ bundle exec berks install
      Resolving cookbook dependencies...
      Using one (1.0.0) from git://github.com/bazbremner/test-case-simple-chef-repo.git (at master/cookbooks/one)
      Using two (1.2.0) from git://github.com/bazbremner/test-case-simple-chef-repo.git (at master/cookbooks/two)
    $ bundle exec berks install
      Resolving cookbook dependencies...
      Using one (1.0.0) from git://github.com/bazbremner/test-case-simple-chef-repo.git (at master/cookbooks/one)
      Using two (1.2.0) from git://github.com/bazbremner/test-case-simple-chef-repo.git (at master/cookbooks/two)
    $ bundle exec berks install
      Git error: command `git filter-branch --subdirectory-filter "cookbooks/one"` failed. If this error persists, try removing the cache directory at '/Users/me/.berkshelf/.cache/git/20a689f6b33b827b6f06f377a9fd5eca49f931a1'.Output from the command:

      Cannot create a new backup.
      A previous backup already exists in refs/original/
      Force overwriting the backup with -f
