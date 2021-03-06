# Git and GitHub configuration

## Git Installation and Setup

    $ sudo apt-get install git-all
    $ git config --global user.name "YOUR NAME"
    $ git config --global user.email "YOUR EMAIL ADDRESS"
    $ git config --global core.editor "vim"
    
    # proxy
    $ git config --global http.proxy http://username:password@proxyhost:proxyport

Check settings using `$ git config --list`.


## Authenticating with GitHub (using HTTPS)

    $ git config --global credential.helper cache
    # Set git to use the credential memory cache

    git config --global credential.helper 'cache --timeout=3600'
    # Set the cache to timeout after 1 hour (setting is in seconds)


## Notes:

* If following dpkg error is encountered, try [this](http://askubuntu.com/a/631619).

    Errors were encountered while processing:
      runit
      git-daemon-run

* In case of `failed to connect to upstart: connection refused` error, try [this](http://askubuntu.com/a/615086).  
* If error still exists, follow  :fire: [this](https://bugs.launchpad.net/ubuntu/+source/runit/+bug/1448164/comments/15) :fire: workaround.
 
## Sources

* [Installing Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
* [Set Up Git](https://help.github.com/articles/set-up-git/)
* [Caching your GitHub password in Git](https://help.github.com/articles/caching-your-github-password-in-git/)
* [runit cannot be installed (Unable to connect to Upstart: Failed to connect to socket /com/ubuntu/upstart: Connection refused)](https://bugs.launchpad.net/ubuntu/+source/runit/+bug/1448164)

