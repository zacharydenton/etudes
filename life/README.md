The Game of LIFE or: Cellular Automata and Computer Graphics
============================================================

LIFE is a multicellular communal organism that inhabits the deserts of
Flatland. The desert is organized in a square array with each square
capable of holding one LIFE cell. LIFE generations mark the passage of
time, each generation bringing births and deaths to the LIFE community.

To follow the history of such a community, place LIFE cells into their
initial positions in the desert. Count the passing generations by
observing these rules.

1.  The *immediate neighbors* of a cell are those cells occupying the
    eight horizontally, vertically, and diagonally adjacent cells.
2.  If a LIFE cell has fewer than two immediate neighbors, it dies of
    *loneliness*. If a LIFE cell has more than three immediate
    neighbors, it dies of *overcrowding*.
3.  If an empty square has exactly three LIFE cells as immediate
    neighbors, a new cell is born in the square.
4.  Births and deaths all take place exactly at the change of
    generations. Thus a dying cell may help birth a new one, but a
    newborn cell may not resurrect a dying cell, nor may one dying cell
    stave off death for another by lowering the local population
    density.

For instance, the community ⋯ becomes ⋮ in one generation, and the
community ⸬ must live near Palm Springs because it never changes at all.

Statement of the Theme
----------------------

Write a program that simulates a LIFE community. The input should be the
initial positions of the community's cells, and the output an aerial
view of the community at each generation. An ordinary line printer can
be used to plot the community's history, but such output is unaesthetic.
If you have access to hardcopy graphic output devices or to an
interactive graphics terminal, use the facilities provided to present a
more appealing visual display.

Performance Practice
--------------------

Although the examples do not show it, some communities grow enormously
from extremely meager beginnings. Others transport themselves slowly
across the desert, continually moving from old territory into new. Your
program should be able to handle large communities without a terrific
cost in space or time. A naive approach will repeatedly scan a large
array to build the generations; the programming problem is to find data
structures and algorithms that are more economical. You may want to try
some method that only keeps track of the occupied squares. Since a
growing or moving community can move out of the view of any fixed method
for displaying the output, you will probably want a method that shifts
its point of view as the community changes.

Orchestration
-------------

APL may be suitable because of its vector and matrix operations. Almost
any higher-level language with arrays can be used. This is a good
problem for studying the cost of assembly language on programming time
and the payoff in inner loop efficiency. Finally, for those with access
to the hardware, a micro-coded version would be an interesting
experiment; the computer becomes a LIFE community.

Playing Time
------------

This problem should take one person 3 weeks.

Variations on the Theme
-----------------------

A community may go on growing forever, continually changing its
position, shape, or membership. But it is more common for a community to
become stable, repeating a few patterns in a cycle for all eternity, the
length of the cycle being the community's period. (The period of a dead
and empty desert is one under this definition.) Modify your program so
that it attempts to recognize and report such stable communities. Can
you think of any algorithm, short of saving all previous generations,
that would infallibly identify stable communities?

The history of a LIFE community is fascinating if viewed as a movie (one
of the reasons that we suggested an interactive graphics terminal). It
is even more attractive when color is added. Each cell can be assigned a
color at birth, perhaps by virtue of its generation or because of the
genetic background of its parents. Cyclic but moving communities (of
which there are quite a number) are beautiful when they march by in a
coat of many sparkling colors.

Every community has a successor, but some have no predecessors. These
isolated communities are called Gardens of Eden. The only way that they
can be seen is by placing them on the desert as an initial
configuration. Think of the ways to use your program to find a Garden of
Eden.
