# Repository Management

## Adding New Batch of Projects

1. Create new separate repository for specific year of Fellowship Projects (i.e. 2026-Fellows-Projects)
   1. Make sure to include the Apache-2.0 License
2. Make new repository a submodule of this repository under **projects/\<year>/** where year is the
   year the fellowship projects are being developed.
   1. `git submodule add <Github URL> projects/<year>/`
3. Update submodule to point to main branch of submodule
   1. `cd projects/<year>/`
   2. `git fetch`
   3. `git checkout main`
   4. `git pull`
   5. `cd ../../`
   6. `git add projects/<year>/`
   7. `git commit -m "Update <year> repository submodule to point to main branch"`
   8. `git push`
4. Setup new year specific repository (Note: Can be done from submodule or clone of specific repository)
   1. Copy over files/structure in **template/** main repository to new repository
      Note: Best to do `cp -a template/. <submodule root>` as there are hidden files
      (i.e. .gitignore and .github/).
   2. Follow specific setup steps in *SETUP.md*

## General

- See [Github submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules)

