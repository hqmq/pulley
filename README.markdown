# Deprecation Notice
This gem was recently updated to work with the newer version of github's api.
I was really excited to take over maintenance of the gem and then I found out
that defunkt/hub actually provides this functionality and lots more.

In view of how awesome the hub project is I must admit that this gem doesn't serve
much purpose so it is being deprecated.

# GithubPulley
### A ruby gem for creating github pull requests

This gem serves no other purpose but to allow github users
to quickly attach a branch to an issue via a pull request.
A feature which is currently only available via the API.

### Why

Our goal is to use GitHub issues for code reviews and tracking stories. In other words
we want to eschew using Pivotal Tracker until we're big enough to care.

### Install

    gem install github-pulley

### Use

    cd /myproject
    git co -b some_new_feature
    # Add the feature
    git ci -am "Added the ability to send emails"
    pulley attach 4  # push and attach this branch to issue #4

Later someone can review the pull request, and merge the code(which also closes
the issue)

### Respecting Forking

This gem respects the github forking process. It assumes that if you fork
a repository, the remote will be named 'upstream', and pull requests
will be sent to the upstream repository if it exists.
