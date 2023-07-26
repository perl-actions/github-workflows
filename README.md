
# Reusable workflows and related actions

## Workflows

### simple-perltester-workflow

Runs simple Perl tests using perl-tester docker images. Automagically creates
matrix for every perl since 5.10 up to newest.

Input parameters:
- `since-perl`: include only Perls since given version (starting with 5.8)
  Uses values from https://github.com/Perl/docker-perl-tester#using-docker-images-for-your-projects
- `with-devel`: include `devel` as well

Example usage
```
---
on:
  ...

jobs:
  call-simple-perl-test:
    uses: happy-barney/github-workflows/.github/workflows/simple-perltester-workflow.yml@main
    with:
      since-perl: 5.14
```
