# Metronome
A python sdk testing framework specializing in ensuring code base synchronization.

## Use case overview
Metronome is useful when you have two independent code bases which are being
updated at different rate, but contain shared files. For example, if we had an
OSS SDK exposing certain pieces of a proprietary software system.

deployment ->

[Open_Install]  <->  [Secret_Install]
    ^                     ^
    |                     |
    v                     v
[ Open_Repo  ]  <->  [ Secret_Repo  ]

The open repo shares some files with the secret repo and secret install. The open repo and the open
install share all files. The secret repo and the secret install share all files.

Metronome helps the system stay in time by indicating where and how the files
which should be in sync differ.
