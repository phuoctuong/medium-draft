# medium-draft - [demo](http://bitwiser.in/medium-draft/)

A medium like rich text editor built upon [draft-js](https://facebook.github.io/draft-js/) with an emphasis on eliminating mouse usage by adding relevant keyboard shortcuts.

### Fetures

- Focus on keyboard shortucts and auto transform of text blocks.
- Image addition via URL.
- Minimize mouse usage
- Autolists
- Proper handling of `RETURN` presses.
- It also has implementations of some custom blocks like:
    - `caption` - Can be used as a caption for media blocks like image or video instead of nested `draft-js` instances for simplicity.
    - `block-quote-caption` - Caption for `blockquote`s.
    - `todo` - Todo text with a checkbox.

##### Following are the keyboard shortcuts to toggle block types (<kbd>Alt and CTRL</kbd> for Windows/Linux and <kbd>Option and Command</kbd> for OSX)
*   <kbd>Alt/Option</kbd> +

    *   <kbd>1</kbd> - Toggle Ordered list item
    *   <kbd>*</kbd> - Toggle Unordered list item
    *   <kbd>@</kbd> - Add link to selected text.
    *   <kbd>#</kbd> - Toggle Header-three.
    *   <kbd><</kbd> - Toggle Caption block.
    *   <kbd>></kbd> - Toggle unstyled or paragraph block.

##### Editor level commands

*   <kbd>Command/CTRL</kbd> + <kbd>S</kbd> - Save current data to `localstorage`.
*   <kbd>Alt + Shift</kbd> + <kbd>D</kbd> - Load previously saved data from `localstorage`.

##### Special characters while typing: While typing in an empty block, if the content matches one of the following, that particular block's type and look will be changed to the corresponding block specified below

*   `--` `(2 hyphens)` - If current block is `blockquote`, it will be changed to `block-quote-caption`, else `caption`.
*   `''` `(2 single or double quotes)` or `> ` - `blockquote`.
*   `*.` `(An asterisk and a period)` - `unordered-list-item`.
*   `*<SPACE>` `(An asterisk and a space)` - `unordered-list-item`.
*   `-<SPACE>` `(A hyphen and a space)` - `unordered-list-item`.
*   `1.` `(The number 1 and a period)` - `unordered-list-item`.
*   `##` - `header-two`.
*   `[]` - `todo`.
*   `==` - `unstyled`.

### Issues

- [x] Currently, the toolbar that appears when text is selected needs to be fixed regarding its position in the viewport.

#### LICENSE

MIT