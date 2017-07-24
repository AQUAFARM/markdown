## 0.9.29 (beta)

24, Apr, 2017

1. Fix a critical bug.

## 0.9.28 (beta)

22, Apr, 2017

1. Fix launch errors.

## 0.9.27 (beta)

17, Apr, 2017

1. Support setting line ending char. Support CRLF line ending.
2. Add syntax highlight support for `ProtoBuf`, fix syntax highlight for `php+html` and `diff`.
3. Fix styles for "unibody" style.
4. Fix font not applied when exporting.
5. Improve copy/paste to prevent data or style lost.
6. Fix key navigation on context menu.
7. Fix a few typos in text resource.
8. Fix header anchor cannot support some unicode char.
9. Fix spellcheck sometimes not working in Linux.

## 0.9.25 (beta)

09, Mar, 2017

1. Fix "import" does not work.
2. Imporve encoding detecting logic for better compatibility.

## 0.9.24 (beta)

27, Feb, 2017

1. Support `alt` key on Windows to popup related menu.
2. Support open recent files from menubar.
3. Fix a bug that Typora cannot detect the encode of some files correctly. Allow manually select file encode from menubar.
4. Fix bugs that table headers and bold Chinese characters cannot be printed (export to PDF) correctly.
5. Fix crash when export contents into jpg file.
6. Show horizontal scrollbar when some table or dialog is too width.
7. Set default extensions for save and export dialog.
8. Add syntax highligh for `fortran`. Fix bugs of syntax highlight function for `Scala` and `C#`.
9. Exported HTML (without class) for code fences could follow w3c recommendations and be more friendly with Prism.
10. Fix some bugs relates to crash and data lose.
11. Fix bugs that some behavior for links are not correct.
12. Fix table parsing logic for special characters.
13. Fix a bug that some math block is invalid in exported EPub.
14. Fix a bug that `\{` is not correctly handled in inline math.
15. Other bug fix.

## 0.9.23 (beta)

4, Jan, 2017

1. Support move table row/col when drag on left/top side of table row/col or using shortcut keys: shift + ctrl + arrow key.
2. Add syntax highlighting for `cmake`, `cypher`, `dart`, `django`, `dtd`, `dylan`, `handlebars`, `idl`, `web idl`, `yacas`, `mbox`, `vhdl`, `julia`, `haxe`, and `hxml`.
3. Remove `//` after `mailto:` for auto generated mail link.
4. Fix image position for flowchart.
5. Fix a bug that some link url or image url are escaped twice.
6. Fix a  bug that `:+1:` is not recognized as emoji.
7. Fix refresh mathjax will convert inline math when inline math is not enabled.
8. Fix freeze when insert images.
9. Other bug fix and improvements.

## 0.9.22 (beta)

20, Nov, 2016

1. Fix the logic for relative path for `typora-root-url`.
2. Support recent used files on Windows jumplist.
3. Support paste images into Typora(after set-up).
4. Support copy images to selected folder when insert images.
5. Fix bugs related to collapsible outline panel.
6. Fix bugs that exported PDF may contain  HTML in bookmark.
7. Fix bugs about undo/redo for nest task list.
8. Fix mermaid no responding when Chinese character exists.
9. Change `copy as markdown` option from opt-in to opt-out.
10. Support elixir for code fences.
11. Fix cli support on Linux.
12. Fix some typo on interface.

## 0.9.21 (beta)

18, Oct, 2016

1. Support insert image from local file. Support drag & drop multiple images.
2. Add preference to use relative path when insert images.
3. Improve footnote export and behavior.
4. Add option for auto-numbering math blocks. Support command for refreshing math expression.
5. Add option set left outline panel collapsible.
6. Support `<img>` tag without a close tag.
7. Remove unnecessary math delimiter for exported LaTeX. 
8. Add syntax highlight for `ocaml`, `F#`, `elm`, `spreadsheet` and `pgp(Ascii Armor)`.
9. Auto-save time schedule can be configured in advanced options.

## 0.9.20 (beta)

6, Oct, 2016

1. Add support for simple HTML fragments, only includes: `<!--comments-->`, `<a href="http://typora.io">link</a>`, `<img src="http://www.w3.org/html/logo/img/mark-word-icon.png" width="200px" />`.
2. Fix syntax highlight for `Octave` is not working, and add `matlab` as its alias. 
3. Math expressions now support export to epub. Diagrams will be converted to images when export to epub/docx.
4. Fix a bug that arrow of diagrams is missing when export to HTML/PDF.
5. Fix a critical bug on tables.
6. Fix some export options are missing in `Export` menu.
7. Other bug fix.

## 0.9.19 (beta)

26, Sep, 2016

1. Launched our [Theme Gallery](http://theme.typora.io) to share and download Typora themes.
2. Fix a bug the menubar won't show automatically when Typora is fullscreened.
3. Improve paste behavior.
4. Fix unnecessary scroll.
5. Fix backspace after UTF-32 character.
6. Fix bugs related to inline code inside table.
7. Recover outline panel status when switch from source code mode.
8. Other bug fix.
9. A Linux build (Debian/Ubuntu) is [available](https://typora.io/#linux).

## 0.9.18 (beta)

4, Sep, 2016

1. Add options to auto pair common markdown symbols, like `*_ etc.
2. Add options to show markdown source for simple blocks when focus, like headings.
3. Fix a bug that sometimes special characters will cause inline math not rendered.
4. Fix a bug that sometime `Enter` key is not working. 
5. Fix some bugs under high DPI screen.
6. Fix a bug that footnote definition cannot be correctly input.

## 0.9.17 (beta)

27, Aug, 2016

1. Fix special characters cannot be input inside inline math.
2. Fix backspace cannot expand inline style.

## 0.9.16 (beta)

19, Aug, 2016

1. Support diagrams, includes sequence, flowchart and mermaid ([doc](http://support.typora.io/Draw-Diagrams-With-Markdown/)).
2. Fix a bug related to parsing `*` and escaped character.
3. Fix backspace inside code fences.
4. Fix escape character will gone in inline math, inline code, and other inline styles.
5. Fix special character, such as `#` cannot be inserted in ceylon code block.
6. Fix quote mark would cause typora not respond sometimes.
7. Allow custom keybindings ([doc](http://support.typora.io/Custom-Key-Binding/)).
8. Allow custom search service ([doc](http://support.typora.io/Add-Search-Service/)).
9. Fix shift+ctrl+home/end key on Windows.
10. Other bug fix and improvements.

## 0.9.15 (beta)

29, Jul, 2016

1. Fix a bug that `**` is not correctly parsed.
2. Fix bookmark not generated when export to PDF when there's h5 and h6 in article.
3. Fix list indentation not correctly saved.
4. Fix footnotes contains "_" cannot be exported correctly.
5. Fix a bug some file format cannot be exported via pandoc.
6. Add "Textile" as one export option.
7. Improve URL auto detection.
8. Fix content will be pasted twice when paste from typora to Word.
9. Other bug fix.

## 0.9.14 (beta)

25, Jul, 2016

1. Fix print/export PDF not work.

## 0.9.13 (beta)

24, Jul, 2016

1. Release x64 build.
2. Add focus mode and typewriter mode support.
3. Remember last status of outline bar.
4. Add syntax support for assembly and TOML.
5. Avoid the usage of 'AltGr' key combination in assigned shortcut.
6. Support kramdown style `[toc]` syntax.
7. Improve list indent/outdent logic.
8. Fix HTML entities not escaped in meta block.
9. Fix a bug that triple click cannot select current line correctly.
10. Fix auto indent for brackets in code fences.
11. Add options to export reStructuredText, and OPML format.
12. Fix user.css not included in exported HTML/PDF.
13. Fix some export option not work in unibody window style.
14. Fix cannot export/print in dark theme.
15. Other bug fix.

## 0.9.12 (beta)

22, Jun, 2016

1. Fix a critical bug that the indent in multi-level lists may keep increasing after save.
2. Fix the scrollbar style on side panel.

## 0.9.11 (beta)

21, Jun, 2016

1. Fix a critical bug that the indents of multi-level lists are wrong when parsing and generating markdown source.
2. Better ECMAScript6 syntax highlight support for javascript code fences. Add syntax highlight support for NSIS, JSX ([React](http://facebook.github.io/react)'s JavaScript syntax extension), vue, LiveScript, mathematica, properties (and .ini), tiki wiki, dockerfile in code fences.
3. Hide auto-complete lists when scrolling.
4. Fix internal link to heading (like [this](#0.9.4.5-(beta))) not work.
5. Fix a bug sometimes, pasting would append duplicate texts.
6. Rule change: capitalized characters are not allowed in filenames for theme css file
7. Make link clickable in about page.
8. Support single column table in insert table dialog.
9. Add enabled optional inline style support, like highlight or inline math, in menubar.

## 0.9.10 (beta)

15, Jun, 2016

1. Fix style that sometimes user can see script content.
2. Fix auto pair match inside image and avoid glitch when complete brackets.
3. Fix paste table, and paste inside footnotes.
4. Fix `]` cannot be escaped in footnotes.
5. Fix `h6` indent inside `[TOC]`.
6. Fix multiple level lists inside blockquote cannot be parsed correctly.
7. Enable ESC key to close insert table dialog.
8. Fix outline sidebar jumpping around when scrolling.
9. Fix ctrl+home/end not working.

## 0.9.9 (beta)

2, Jun, 2016

1. Fix a bug that Typora cannot be launched by opening md files on PCs without *Visual C++ library* installed.

## 0.9.8 (beta)

1, Jun, 2016

1. Fix a critical bug about saving in source code mode.
2. Fix save dialog keep poping up sometimes.
3. Improve logic for auto match paired quotes and brackets.
4. Fix inline math cannot be exported to some file types via pandoc.
5. Fix a bug that improper file name is auto generated when the article contains YAML forn matters.

## 0.9.7 (beta)

30, May, 2016

1. Fix typora.exe is misreported by some anti virus software.


## 0.9.6 (beta)

27, May, 2016

1. Add mobile "responsive" support for exported HTML.
2. Pandoc requires 1.16 and above. Fix exporting fail using Pandoc.
3. Better support for monitoring file content change by external apps.
4. Fix generating PDF takes too much time and reduce file size for PDF. Also fix a bug anchor link in PDF not working and Chinese character in printed PDF is not selectable.
5. Fix shortcut keys for `h6` not working.
6. Add syntax highlight for Powershell. 
7. Remember windows size when creating new window.
8. Can open `.md` file from `cmd.exe` directly, if typora is its default reader.
9. Fix that some advance options not work. Add options to auto hide menu bar.
10. Fix a critical bug in paste/undo which may case data lose.
11. Make `\label` work in math block.
12. Fix unnecessary empty char in inserted footnote.
13. Fix auto pair match and find&replace in math block.
14. Fix up/down key behavior on code fences.
15. Fix some HTML code  (like `&phone;`) not escaped in inline code.
16. Other bug fix.

## 0.9.5 (beta)

5, May, 2016

1. Add pandoc integration, import function and export function for docx, rtf, LaTeX, etc.
2. Able to open `.md` file or import supported files by drag and drop into typora's window.
3. Fix a bug that sometimes PDF cannot be exported correctly.
4. Fix `H4` style in `pixyll` theme.
5. Fix sql mode error for code blocks.
6. Fix a bug for parsing headers with underline style.
7. Fix a bug for undo/redo for editing lists.
8. Fix a bug when pasting lists.
9. Other bug fix.

## 0.9.4 (beta)

23, Apr, 2016

1. Fix LaTeX is not correctly exported after opening existing files.
2. Fix a bug which may cause content inside list items get lost.
3. Fix wrong indent for content inside list after parsing raw markdown.
4. Support "Open File Location" action.
5. Fix a bug that if image path contains special chars like quotes, the image cannot be displayed correctly.
6. Fix a bug related to paste lists.
7. Fix a bug some line breaks disappear in exported PDF.



## 0.9.3 (beta)

19, Apr, 2016

1. Fix the wrong bookmark structure in exported PDF.
2. Fix sometimes Chinese characters cannot be saved to file correctly.
3. In exported HTML, file name will be set to `<title>` tag.

## 0.9.2 (beta)

18, Apr, 2016

1. Better save feature: Support file auto save (need enable it from preference panel) and allow users to recover unsaved drafts form preference panel.
2. Better word count: Now click word count button from status bar, detailed info would show.
3. Better Print: Fix a bug that current window, instead of generated web view woulc be printted.
4. Better PDF exporting: Now exported PDF could contains Table of Contents as bookmarks, just like Mac version
5. Better fullscreen mode: Fullscreen mode can auto show menu bar for native style windows, and auto show/hide title bar control buttons for unibody windows. Newly created windows would also be fullscreen in fullscreen mode.
6. Fix table cannot be deleted in the beginning of the article.
7. Fix a bug that some lines will be duplicated after open.
8. Fix files on external disks cannot be opened.
9. Other bug fix.

## 0.9.1 (beta)

6, Apr, 2016

1. Fix a critical bug for saving.
2. Fix a critical bug for task list.

## 0.9.0 (beta)

4, Apr, 2016

1. Rewrite typora's Markdown parse engine and largely improve the performance on opening mid-sized files.
2. Fix bugs for pair auto-complete.
3. Fix bugs for Korean IME.
4. Fix a bug that typora will eat and replace non-breaking space.
5. Fix relative image path on exported HTML.
6. Fix a bug typora will detech wrong encoding sometimes.
7. Other bugs.

## 0.8.8 (beta)

13, Mar, 2016

1. Fix minor parse issue for URL, subscript and superscript.
2. Fix compatibility issue between Chinese IME and auto-pair feature
3. Include and autoload MathJax extension, including chemistry package and others (e.g. $\ce{C6H5-CHO}$).
4. Fix bug triggered by pressing `` ctrl+` `` twice.
5. Fix some menu item under "Edit" submenu does not work.
6. Support open hyperlink from context menu.
7. Other bug fix.

## 0.8.6 (beta)

4, Mar, 2016

1. Fix a critical bug on Delete key.

## 0.8.5 (beta)

3, Mar, 2016

1. Support ==highlight== syntax (should enable it from preference panel).
2. Support auto complete pairs of brackets, quotes and parentheses.
3. Fix bugs on lists.
4. Fix cut on windows. 
5. Fix selection styles in code fences, python code in code fences will use 4-space indent.
6. Fix customize font size, local image, local font does not work for exported PDF.
7. Fix bugs for LaTeX editing/rendering.
8. Auto insert path/urls from clipboard when insert images/hyperlinks from menubar or shortcut keys.
9. Other bug fix.

## 0.8.3 (beta)

24, Feb, 2015

1. Add basic support for editing in source code mode directly.
2. Support signle line break (shift+return).
3. Improve LaTeX rendering quality.
4. Support non-UTF8/16 encoded files, includes Shift-JIS, Big5, EUC-JP, EUC-KR, GB18030, ISO-8859-1, ISO-8859-2, ISO-8859-5, ISO-8859-6, ISO-8859-7, ISO-8859-8, ISO-8859-9, windows-1250, windows-1251, windows-1252, windows-1253, windows-1254, windows-1255, windows-1256. Other encodings is not supported yet.
5. Fix bug that tab+subbullet will be parsed as code fences.
6. Fix syntax highlight support for PHP, SQL, Objective-c, etc.
7. Fix then behavior when pressing ctrl or shift and arrow key.
8. Fix bugs in find/replace.
9. Fix small bugs in exported HTMLs.
10. Support drag & drop to insert images and fix images not shown with relative path.
11. Fix cut & paste function.

## 0.7.7 (beta)

11, Jun, 2015

1. Imporve stability and reliability on saving

## 0.7.6 (beta)

3, Jun, 2015

1. Fix a critical bug which may cause data lose.
2. Fix syntax parse for task list.
3. Improve theme `newsprint`.
4. Fix the unnecessary io operation when starting Typora.

## 0.7.5 (beta)

24, DEC, 2015

First beta version.

## 0.7.0 (alpha)

19, DEC, 2015

First alpha version.