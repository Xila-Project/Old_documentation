# 🏷️ Nomenclature

Although this is a complicated subject among programmers, here is the nomenclature used in Xila to name identifiers. It's far from perfect but I like it this way.

## General rules

For all the identifiers:
- All the names are in English.
- All the words start with a capital letter, even the first one.
- Each words are separated by an underscore `_`.
- Avoid abbreviations as much as possible.

## Types

| Type        | Suffix       | Example         |
| :---------- | :----------- | :-------------- |
| Enumeration | `_Type`      | `Foo_Type`      |
| Class       | `_Class`     | `Foo_Class`     |
| Structure   | `_Structure` | `Foo_Structure` |
| Union       | `_Union`     | `Foo_Union`     |

For `Class` and `Structure`, use the this name for internal definition and create an alias with the name followed by `_Type` for the public definition.

## Functions

Both methods and functions follow the following convention:
- If it is an accessor, it starts with `Get_` or `Set_`.
- If not, it starts with a verb corresponding to the main action it performs.
- If it is a callback, it ends with `_Callback`.
  
## Variables

For variables, just follow the general rules and add a suffix corresponding to the identifier of the variable.

## Constants

For constants, the same rules apply as for variables. (No capital letter)

## Comments

For comments, use the following rules:
- Use `//` for single line and multi-line comments (no `/* */`).
- If the comment concerns a block of code, add `-` corresponding to the scope level of the comment.