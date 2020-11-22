# gitlab-clone-group

Tool for cloning all projects in a gitlab group.

## Installation

```
pip install gitlab-clone-group
```

## Usage

```
usage: gitlab-clone-group [-h] [--token TOKEN] [--url URL] [--dry-run] [--exclude EXCLUDE] [--include INCLUDE]
                          [--verbose]
                          group

Clone all respositories in a gitlab group.

positional arguments:
  group                 The gitlab group

optional arguments:
  -h, --help            show this help message and exit
  --token TOKEN, -t TOKEN
                        Your gitlab API token. Alternatively set the GITLAB_TOKEN environment variable.
  --url URL, -u URL     The gitlab API endpoint. Alternatively set the GITLAB_URL environment variable
  --dry-run, -d         Dry run, just print the repositories to clone
  --exclude EXCLUDE, -e EXCLUDE
                        Repositories matching this regular expression are excluded.
  --include INCLUDE, -i INCLUDE
                        Only repositories matching this regular expression are included.
  --verbose, -v         Verbose mode
```

Example:

```
% export GITLAB_TOKEN='XXXXXXXXXXX'
% gitlab-clone-group --url https://example.org/gitlab foo/bar
```

See [Personal access tokens](https://docs.gitlab.com/ee/user/profile/personal_access_tokens.html) for instructions on generating an access token.  The token needs access to the **api** scope.
