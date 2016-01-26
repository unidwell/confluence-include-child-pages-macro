# confluence-include-child-macro

Includes content of all immediate child pages into the current page. Used to assemble (include content) of all the subpages.

## Usage

To use it, one has to create a new user macro in confluence (go to /admin/usermacros.action). Name it as you like for instance "include_child_pages". In the macro's template put the content of the file *include_pages_macro.vm*.

When the macro is saved, it can be included on any page like this (or from the menu *Insert/Other macros*:

> {include_child_pages}


## Configuration


## Confluence version


Version 5.x are supported.
