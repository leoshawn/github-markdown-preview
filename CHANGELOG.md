# Changelog

## v2.0.0
* Add the ability to render a [preview of how Github renders comments/issues](https://github.com/dmarcotte/github-markdown-preview#comment-mode)
* Make the `github-linguist` dependency [optional](https://github.com/dmarcotte/github-markdown-preview/pull/14)
* [Update dependencies](https://github.com/dmarcotte/github-markdown-preview/pull/13)
* Breaking changes:
    - `preview.delete_on_exit` no longer exists.  To delete the preview on exit, pass the `:delete_on_exit = true` option ([example here](https://github.com/dmarcotte/github-markdown-preview#code))
    - Since `github-linguist` is not longer required, previews on systems without it installed will not have syntax highlighting

## v1.6.1
* Fix [#11](https://github.com/dmarcotte/github-markdown-preview/issues/11)

## v1.6.0
* Improve preview fidelity ([#9](https://github.com/dmarcotte/github-markdown-preview/pull/9))
* Update dependencies ([#7](https://github.com/dmarcotte/github-markdown-preview/pull/7))

## v1.5.0
* structure the app for gem deployment and add Bundler utilities
* move the main code into the GithubMarkdownPreview::HtmlPreview
class to allow other programs to include a preview
* add comprehensive tests
* improve the scripts output (especially in error cases)
* update to latest github css

## v1.4
* fix compatability with Listen 1.0+

## v1.3
* fix scroll issue which was causing page position to be lost on refresh
* update github css

## v1.2
* output help text on incorrect arguments
* output location of preview file for easy viewing
* update install instructions to clarify some dependencies

## v1.1
* write the `.html` preview beside the source `.md` file to support [relative links](https://github.com/blog/1395-relative-links-in-markup-files)
* remove the MentionFilter (which makes `@username` links) since these are not linked on Github

## v1.0
* initial release
* writes a `.html` high-fidelity preview of a given github flavored `.md` file to `/tmp/markdownPreview.html`