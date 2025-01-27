## Seatable Admin Docs

This repository contains the SeaTable Admin documentation. The documentation is built using [MkDocs](https://www.mkdocs.org/), a fast and simple static site generator. The pages are being built using Github workflows and hosted on Github Pages.

### Usage
To build and view the documentation locally, you can use these steps:

- Clone this repository & Checkout a new branch
- Make changes and review them locally (with docker)
- Commit and push your changes
- Create a pull request


```bash
git clone <this_repo>
cd <this_repos_directory>
git checkout -b <new_branch>
```
- Preview changes locally with docker / Preview at [http://127.0.0.1:8000](http://127.0.0.1:8000)
```bash
./preview.sh
```
```bash
git add <relevant_changes>
git commit -m "<commit_message>"
git push
```
- stop preview
```bash
./preview.sh -stop
```
