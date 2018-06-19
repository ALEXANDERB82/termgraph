# termgraph.py

A python command-line tool which draws basic graphs in the terminal.

Graph types supported:

- Bar Graphs
- Color charts
- Multi-variable
- Stacked charts
- Horizontal or Vertical
- Emoji!


### Examples

```
termgraph.py data/ex1.dat
```

<img src="docs/img/example.png" width="665" alt="Single variable bar chart"/>

```
termgraph.py data/ex4.dat --color {blue,red} --no-title
```

<img src="docs/img/example2.png" width="655" alt="Multi variable bar chart with colors" />

```
termgraph.py data/ex7.dat --color {yellow,magenta} --stacked --title "Stacked Data"
```

<img src="docs/img/example3.png" width="686" alt="Multi variable stacked bar chart with colors" />

```
termgraph.py data/ex1.dat --custom-tick "🏃" --width 20
```

<img src="docs/img/example4.png" width="556" alt="Emoji!" />


### Install

* Works best with python3
* pip3 install colorama
* Download script, set executable and put in path

### Usage

* Create data file with two columns either comma or space separated.
  The first column is your labels, the second column is a numeric data

* termgraph.py [datafile]

* Help: termgraph -h

```
usage: termgraph.py [-h] [--title TITLE] [--no-title] [--width WIDTH]
                    [--format FORMAT] [--suffix SUFFIX] [--no-labels]
                    [--color [{red,blue,green,magenta,yellow,black,cyan} [{red,blue,green,magenta,yellow,black,cyan} ...]]]
                    [--vertical] [--stacked] [--different-scale]
                    [--custom-tick CUSTOM_TICK]
                    [filename]

draw basic graphs on terminal

positional arguments:
  filename              data file name (comma or space separated). Defaults to
                        stdin.

optional arguments:
  -h, --help            show this help message and exit
  --title TITLE         Title of graph
  --no-title            Does not print title. Overrides --title.
  --width WIDTH         width of graph in characters default:50
  --format FORMAT       format specifier to use.
  --suffix SUFFIX       string to add as a suffix to all data points.
  --no-labels           Do not print the label column
  --color [{red,blue,green,magenta,yellow,black,cyan} [{red,blue,green,magenta,yellow,black,cyan} ...]]
                        Graph bar color( s )
  --vertical            Vertical graph
  --stacked             Stacked bar graph
  --different-scale     Categories have different scales.
  --custom-tick CUSTOM_TICK
                        Custom tick mark, emoji approved
```


### Background

I wanted a quick way to visualize data stored in a simple text file. I initially created some scripts in R that generated graphs but this was a two step process of creating the graph and then opening the generated graph.

After seeing [command-line sparklines](https://github.com/holman/spark) I figured I could do the same thing using block characters for bar charts.

### Contribute

For feature requests or bug reports, use [Github
Issues](https://github.com/mkaz/termgraph/issues).

Thanks to all the additional
[Contributors](https://github.com/mkaz/termgraph/graphs/contributors).


### License

Copyright 2012-2018 Marcus Kazmierczak

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

