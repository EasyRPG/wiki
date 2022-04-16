---
title: "Editor-GTK code formatting conventions"
---
Editor-GTK conventions are like player conventions, but with some changes since the editor is written in Vala.

### Naming

------------------------------------------------------------------------

##### Constants

All upper case, with underscores as name separators, but no leading/trailing underscores:

``` csharp
THIS_IS_A_CONSTANT
```

##### Type names

Clases should be UpperCamelCase.

``` csharp
class MainWindow : Gtk.Window {
class Armor : Item {
```

##### Functions

Functions should be lower case with underscores as word separators.

``` csharp
void this_is_a_function() {
```

Properties should have getter and setter defined:

``` csharp
class Foo {
    private int random_int { public get; private set; }
    public bool has_something { public get; public set; }
}
```

##### Variables

Variables should be lower case with underscores as word separators.

``` csharp
int this_is_a_variable;
```

### Comments

Use /\* This style \*/ preferably.

Please use Valadoc comment style (Javadoc like) for code documentation.

##### License File Header

Remember to copy (from any other existing file) the license header to all new created files.

##### Special comments

``` csharp
// TODO: what is left to do
// FIXME: what code and in what circumstances it does not work, and if possible why it does not work well
```
