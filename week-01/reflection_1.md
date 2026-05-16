[![Screenshot-2026-05-15-163017.png](https://i.postimg.cc/SxKqvTQC/Screenshot-2026-05-15-163017.png)](https://postimg.cc/kBLkVybg)

Git is just a bunch of pointers pointing to each other, creating a chain.
A commit points to a tree, which is basically a directory, then a tree points to one blob or more, which are hashes of files content.

I used `git log` to find previous commits, I chose the most recent one, and using `git cat-file -p [commit]`, I was able to list all the existing objects, as well as the metadata, then i  traversed through all the trees to view their content.

bonus: I used `git cat-file` on the parent hash, and since there is only 2 commits I was able to perform the command 2 times until i got to the first commit which has no parent.