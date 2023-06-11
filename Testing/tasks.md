# Tasks for testing

>__*This is subject to update, as with every group I would think of new tasks.*__

>__*If anyone would have offers of their own: eima.blaz@gmail.com or fork enter them in and pull request them in.*__


1. **Create a program for Groceries list.**
- I should be able to create Item.
- Each item should have a name, origin
- I should be able to add Items to the Groceries list.
- When registering item to the list I want to be able
    to provide the amount of this item that I need.
- There should be an option to delete item
from the Groceries list.
- There should be options to show all crated products
and current shopping list.

2. **Create a program for Cataloguing Movies.**

- I should be able to create a movie record.
- Each movie should have a title, imdb rating, release year.
- I should be able to add Movies to MoviesIHaveSeen list.
- When registering movie to the list I want to be able
    to provide my personal rating 0-10.
- There should be an option to delete last movie
from the MoviesIHaveSeen. OR 
- if the id of the movie is provided remove a that movie.
- There should be options to show all created movies list
and MoviesIHaveSeen list.
- After the program terminates both MoviesIHaveSeen  list 
and all created movies should be saved into separate files.
- At the start of the program the program should read the files to catch up on what was done before.
~~~
Example of testing file operations:
def writetoafile(fname):
    with open(fname, 'w') as fp:
        fp.write('Hello\n')

def test_writetofile(tmpdir):
    file = tmpdir.join('output.txt')
    writetoafile(file.strpath)  # or use str(file)
    assert file.read() == 'Hello\n'
~~~
>Basically do the same but pass the test file a tmpdir fixture, 
that does not need to be defined as it is built-in to pytest
