# sh style guide

i'm going to try and use this with all of my scripts to prevent myself from going insane while scripting, like i did today while working on wmrc.

## bash vs sh

script with sh (which is /dash on void) and avoid bash as much as possible.

## file extensions

nada

## headers

example header:

```sh
#!/bin/sh
#
# program - it does things
# (c) arcetera 2015 - wtfpl
#
```

the first line is the shebang, which will hopefully be `#!/bin/sh`. if bash is needed, use `!#/usr/bin/env bash`<br>
then have a line with merely #.<br>
then have the program name, a dash, a short description.<br>
then have the copyright and license.<br>
then another #.

## functions

functions will be written with parentheses, not using `function`.

```sh
do_something_cool() {
  # code
}
```

## indentation

use two spaces, not tabs

```sh
# hell no
do_something_cool() {
        echo 'hi'
}

# much better
do_something_cool() {
  echo 'hi'
}
```

## while/for/if

put `; do` and `; then` on the same line as the loop statement

## case

case should be indented two spaces, unless on the same line, in which case it should be on the same line

## command subs

use `$()`.

## test

use brackets, not test itself. if using bash (which should be avoided), use double brackets

## comments

don't put a ton of comments everywhere where they aren't needed.

for large blocks of code which do something big, use a single octothorpe. for smaller comments, use two octothorpes.

## quotes

use '' when you don't need it, use "" when you do for variable interpolation
