# Confluence Include Child Pages User Macro


The macros includes content of all the immediate child pages of the selected or current page.


## Usage


To use it, one has to create a new user macro in confluence (in your confluence go to /admin/usermacros.action). Name it as you like for instance **include_child_pages**. In the macro's template put the content of the file *include_pages_macro.vm*.

When the macro is saved, it can be included on any page like this (or from the menu *Insert/Other macros*):

>
> {include_child_pages}
>

The next thing to do is to configure some of the parameters that guide the output. The macro can be used recursively, i.e. partially glue pages together on one level, glue them together again on a higher level in the page tree. Only some of the subpages can be selected by their label.

## Configuration

There are some configurations options that guide how the output should be displayed. The option (**SplitPages**) changes the output only in PDF files.

| Parameter            | Type / Options  | Description  |
| -------------        | -------------   | ------------ |
| Parent Page Title    | *string value*    | Include children of a specific parent page. If no page is defined, current page will be selected. |
| Show Title           | *boolean value* | Deselect to remove the title of the child page. Selected by default. |
| Link Title           | *boolean value* | Select to turn the titles of the child pages into links to those pages (Show Title must be selected). |
| Page Separator       | *boolean value* | Separate pages with horizontal ruler. |
| Split Pages          | *boolean value* | Split pages marker for PDF export will be inserted. Page separator will not be shown when exporting. |
| Filter on Page Label | *string value*  | Include only subpages with the specified label. |
| Order                | *Nav Order*, *Reverse Nav Order*, *Alphabetical*, *Reverse Alphabetical*, *Create Date*, *Reverse Create Date* | In what order should the child pages be displayed? **Nav Order** refers to the order of the child pages in the page tree. **Reverse Nav Order** simply reverses that. |
| Limit | *integer value*  | The number of pages to include. If the number is not specified all pages will be included. |

## Trivia

The user macros in Confluence are written in [Velocity](http://velocity.apache.org/engine/devel/docs/user-guide.html) template language. More on User Macros can be found on [Confluence](https://confluence.atlassian.com/doc/user-macro-template-syntax-223906130.html).

## Confluence version


Version 5.x are supported.


## Copyright and License


Code and documentation copyright 2016 (all contributors). Code released under [the MIT License](./LICENSE).
