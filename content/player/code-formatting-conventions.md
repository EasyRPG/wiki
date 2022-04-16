---
title: "Code Formatting Conventions"
---
## Code Formatting Conventions

#### Common Sense

------------------------------------------------------------------------

Just use it, it may be better to break the convention rules in some cases.

#### Indentation

------------------------------------------------------------------------

Tabs, at four columns. Always indent within braces.

Remember to change your text editor/IDE configuration, so it automatically uses tabs instead of spaces.

#### Braces

------------------------------------------------------------------------

Braces in your code should look like the following example:

``` cpp
for (int i = 0; i < t; i++) {
    [...]
}
 
if (j < k) {
    [...]
} else {
    [...]
}
 
class Dummy {
    [...]
};
```

#### Whitespaces

------------------------------------------------------------------------

In no case there should be two whitespaces together. If you want align some code use tabs instead, that are easier to maintain. Pay attention to spaces or tabs at the ending of a line, remove them.

##### Conventional operators surrounded by a space character

``` cpp
a = (b + c) * d;
```

##### C++ reserved words separated from opening parentheses by a white space

``` cpp
while (true) {
```

##### Commas followed by a white space

``` cpp
SomeFunction(a, b, c);
```

``` cpp
int d, e;
```

##### Semicolons followed by a space character, if there is more on a line

``` cpp
for (int i = 0; i < 10; i++) {
```

``` cpp
DoSomething(e); DoSomething(f);    // This is probably bad style anyway
```

##### When declaring class inheritance and in a ? construct, colons should be surrounded by white space

``` cpp
class Foo : public Bar {
```

``` cpp
var1 ? var2 : var3;
```

##### Array delete operator has no whitespace before \[\]

``` cpp
delete[] foo;
```

##### STD library and \<\>

No whitespaces before or after \<, and whitespaces only after \>.

``` cpp
std::vector<int> array;
```

``` cpp
std::vector<std::vector<int> > array_of_arrays;
```

##### Operator overloading

Operator keyword is not separated from the name, except for type conversion operators where it is required.

``` cpp
struct Foo {
    void operator()() {
        // ...
    }
 
    operator bool() {
        return true;
    }
};
```

##### Pointers and casts

No whitespace after a cast; and in a pointer, we write a whitespace after it but not before it. Consider "\*" to be part of the type.

``` cpp
const char* ptr = (const char*)foobar;
```

##### References

Unlike pointers, use a whitespace before the "&" but not after it. Consider the & operator to affect the variable, not the type.

``` cpp
int i = 0;
int &ref = i;
```

``` cpp
void func(const int &foo) {
```

### Switch / Case constructs

------------------------------------------------------------------------

``` cpp
switch(command_window->GetIndex()) {
  case 0: // New Game
      CommandNewGame();
      break;
  case 1:  // Load Game
      CommandContinue();
      break;
  case 2:  // Exit Game
      CommandShutdown();
}
```

### Naming

------------------------------------------------------------------------

##### Constants

All upper case, with underscores as name separators, but no leading/trailing underscores:

``` cpp
THIS_IS_A_CONSTANT
```

`As a exception`, for headers use the following format:

``` cpp
#ifndef _WINDOW_COMMAND_H_
#define _WINDOW_COMMAND_H_
```

##### Type names

We use RPG Maker XP/VX RGSS and scripts as our API base. Normally classes should be named in UpperCamelCase, like EventCommand, but there are some exceptions when trying to mantain the names RPG Maker XP/VX use, like RPG or Scene_Title. Scripts or "Engine" classes use a word prefix with a underscore indicating what they are for: Game\_, Sprite\_, Spriteset\_, Window\_ and Scene\_.

``` cpp
class RPG::MoveRoute {
class Game_CommonEvent {
class Window_MenuStatus : public Window_Selectable {
class Scene_Battle : public Scene {
```

##### Functions

Functions should be UpperCamelCase.

``` cpp
void ThisIsAFunction() {
```

Property methods should start with Get or Set:

``` cpp
class Foo {
public:
    int GetThatInt() { return that_int; }
    void SetThatInt(int new_int) { that_int = new_int; }
private:
    int that_int;
}
```

##### Variables

Variables should be lower case with underscores as word separators.

``` cpp
int this_is_a_variable;
```

### Headers includes

------------------------------------------------------------------------

Use the following format:

``` cpp
#include "header1.h"
#include "header2.h"
```

And when possible use the following headers order:

-   System headers (e.g. windows.h)
-   C headers (e.g. math.h)
-   C++ headers (e.g. string)
-   system.h
-   Current class/namespace header (e.g. game_map.h for game_map.cpp)
-   Tools headers (e.g. output.h)
-   Backend/Multimedia headers (e.g. graphics.h)
-   Engine headers (e.g. game_character.h)
-   liblcf headers (e.g. lmu_reader.h)

For each headers group alphabetically sort the includes.

### Comments

------------------------------------------------------------------------

Use // preferably. Use /\*Multiline comments\*/ when disabling multiline code.

##### License File Header

Remember to copy (from any other existing file) the license header to all new created files.

##### Documentation

Use Doxygen like documentation, with the following format for functions:

``` cpp
/**
 * Description of MyFunction.
 * A more detailed description here.
 * @param var1 : this is a description for var1
 * @param var2 : this is a description for var2
 * @return here goes a description for return value
 */
virtual int MyFunction(double var1, std::string var2);
```

With the exception of getters and setters:

``` cpp
/** @return description of variable */
int GetVariable();

/** @param variable : description of variable */
void SetVariable(int variable);
```

And for variables:

``` cpp
/** Description of example_variable. */
std::string example_variable;
```

Remember to document only declarations and not implementations, i.e. in headers. An exception could be .cpp static functions or variables, if documenting is really necessary.

##### Code descriptions

We prefer a global function description with Doxygen headers rather than inside the function descriptions. Only when code is really hard to follow, or there is something hardcoded then add some comments explaining the situation. Do not add redundant comments, like actions that should be already understand easily.

##### Special comments

``` cpp
// TODO: what is left to do
// FIXME: what code and in what circumstances it does not work, and if possible why it does not work well
```
