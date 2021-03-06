# FN (Python 3)

## What is it?

This is a tiny library to generate file names.

It will give you unique file names based on current git commit, as well as 
the time and date. You can also set your own prefix and/or postfix.

When called from terminal, `fn`, the file names look like this:

    20160428-001056-597392-2d95c86-b775190
    20160428-001056-153234-2d95c86-b775190

Which currently follows this format:

    yyyymmdd-hhmmss-10^(-6)seconds-gitsha-procsha

(Subject to change as I see fit, or on suggestion.)

If you use the package within python you can also:

  - Pass your own prefix and postfix.
  - Override the postfix.
  - Append incremental numbers.
  - Change the delimiter.
  - Override the length of the git sha.

Se `./example.py` for some usage

## Why?

I have a lot of projects where I make large amounts of files (images, 3D
models, 2D vector files), and I've always wanted a more efficient way of
maintaining unique file names.

I got inspired to write this when I saw this tweet about how Vera Molar names
her works in a Periscope video:

    https://twitter.com/inconvergent/status/700341427344113665

## Install

Install using (as `sudo`) either

  `./setup.py install`

Or

  `./setup.py develop`

The latter is most convenient if you will be editing the code.

## Does it guarantee unique file names in any way?

No. It only uses the current time to make a relatively distinct string—don't
use this for anything remotely important.

## Todo

  - Pass in some arguments in terminal?
  - Git sha as folder, not in name?

