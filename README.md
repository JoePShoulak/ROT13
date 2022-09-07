# ROT13 #
## Archived ##

This is an older project of mine from earlier in my coding career. I don't feel like making it private or deleting it, but this project does not necessarily reflect my current methodology as a developer. No further changes have been made. 

## About ##

A basic cryptographic algorithm acheived by shifting the alphabet 13 lettes chronologically and converting likewise. For example:

    A --> N
    B --> O 
    C --> P
    D --> Q
    E --> R
    F --> S
    G --> T
    H --> U
    I --> V
    J --> W
    K --> X
    L --> Y
    M --> Z
    N --> A
    O --> B
    P --> C
    Q --> D
    R --> E
    S --> F
    T --> G
    U --> H
    V --> I
    W --> J
    X --> K
    Y --> L
    Z --> M

One of the interesting things about this algorithm, is that if you do it twice in a row, you get back to where you started, since 13 past 13 is 26.

## Usage ##

    $ ls
      rot13  my_secret_document.txt
    $ cat my_secret_document.txt
      Too Many Secrets
    $ ./rot13 my_secret_docuemnt.txt
      converting my_secret_document.txt using rot13
    $ ls
      rot13  my_secret_document.txt  my_secret_document.txt.rot13
    $ cat my_secret_document.txt.rot13
      Gbb znal frpergf
    $ rm my_secret_document.txt
    $ ls
      rot13  my_secret_document.txt.rot13
    $ ./rot13 my_secret_document.txt.rot13
      converting my_secret_document.txt.rot13 using rot13
    $ ls
      rot13  my_secret_docuemnt.txt  my_secret_document.txt.rot13
    $ cat my_secret_document.txt
      Too many secrets

## Future ##
I plan on adding the ability to choose how much you rotate by, and maybe even developing a cryptanalyst tool, such that you give it text rotated by some amount, and using `spell`, it keeps shifting until it becomes a word and then prints out the possible word and rotation amounts
