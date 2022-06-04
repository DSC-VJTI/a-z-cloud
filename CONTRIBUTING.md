# How to Contribute

We'd love to accept your patches and contributions to this project. There are
just a few small guidelines you need to follow.

## General Guidelines (for ```/content/docs/```)

- Add a _References_ section towards the end of Markdown whenever external sources have been referred or used verbatim (except quotes).
- Add a caption or explanation for images whenever used. Always add alternative (alt) text for accessibility.
- Have an idea about Hugo [shortcodes](https://gohugo.io/content-management/shortcodes/#use-hugos-built-in-shortcodes).
- As this project uses the Hugo template - Docsy, you have access to several [shortcodes](https://www.docsy.dev/docs/adding-content/shortcodes/) that can make implementation of some formatting easy for you.

## Follow Conventional Commits

Pull requests should have a title that follows the specification, otherwise, merging is blocked. If you are not familiar with the specification simply ask maintainers to modify. You can also use this cheatsheet if you want:

- `fix: ` prefix in the title indicates that PR is a bug fix and PATCH release must be triggered.
- `feat: ` prefix in the title indicates that PR is a feature and MINOR release must be triggered.
- `docs: ` prefix in the title indicates that PR is only related to the documentation and there is no need to trigger release.     
Since this repository is mainly a documentation project; such commits are considered as features. Whereas changes in the README or other supporting Markdown files for the project are considered to be documentation changes.
- `chore: ` prefix in the title indicates that PR is only related to cleanup in the project and there is no need to trigger release.
- `test: ` prefix in the title indicates that PR is only related to tests and there is no need to trigger release.
- `refactor: ` prefix in the title indicates that PR is only related to refactoring and there is no need to trigger release.

What about MAJOR release? just add `!` to the prefix, like `fix!: ` or `refactor!: `

Prefix that follows specification is not enough though. Remember that the title must be clear and descriptive with usage of [imperative mood](https://chris.beams.io/posts/git-commit/#imperative).

## Code reviews

All submissions, including submissions by project members, require review. We
use GitHub pull requests for this purpose. Consult
[GitHub Help](https://help.github.com/articles/about-pull-requests/) for more
information on using pull requests.

## Community Guidelines

This project follows
[Google's Open Source Community Guidelines](https://opensource.google.com/conduct/).

## License
When you submit changes, your submissions are understood to be under the same [Apache 2.0 License](https://github.com/asyncapi/asyncapi/blob/master/LICENSE) that covers the project.

Happy contributing :heart:
