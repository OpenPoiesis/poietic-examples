# Poietic Examples

Example models for the Poietic Flows toolkit.

To play with the examples, you need the
[Poietic Tool](https://github.com/OpenPoiesis/PoieticTool) installed.


## Contents

- **Thinking In Systems** – flows and stocks models from the [book](https://www.goodreads.com/book/show/3828902-thinking-in-systems)
  *Thinking in Systems: A Primer* by Donella Meadows


## Running the demos

Make sure you have the `poietic` command-line tool from the
[Poietic Tool](https://github.com/OpenPoiesis/PoieticTool) package installed.
Follow the installation instructions contained in the package.


There are two ways to run and explore the demos: use the included convenience
`run` script or do it manually. Here are the methods described in more detail.

### Convenience Script

To run the demos you can use the included convenience `run` script in the
same directory as this README file.

For example:

```bash
./run ThinkingInSystems/Capital.poieticframe
```

The command will create output in the `./out` directory with a CSV file
containing the simulation result. If you have the optional tools installed
(see below), more content, including charts and diagrams, is generated.

**Recommended**

Install the following tools to have additional visual content generated.

- [Gnuplot](http://gnuplot.info) – generate charts as PNG images.
- [Graphviz](https://graphviz.org) – generate model diagram image.

On MacOS with Homebrew use:

```bash
brew install gnuplot graphviz
```

### Manual Method

1. Create a new database: `poietic new`
2. Importing the demo package: `poietic import Basic/Interest.poieticframe`
3. To make sure all parameter connections are correct, for some packages you might need to run `poietic edit auto-parameters`.
4. Run the simulation: `poietic run` and see the simulation results in the
   standard output.

Explore the included `run` shell script or explore `poietic --help` and `--help`
of its subcommands to learn more what can be done with the example models.

Experiment with the model by editing it. See the
[poietic tool documentation](https://github.com/OpenPoiesis/PoieticTool/blob/main/Docs/Tool.md)
for more details.


## Development Notes

The included demos are in early stage of development. The file format of
the demos is not yet stable and might change. If you create your own
derivatives, please be aware, that they might or might not work in the future.


## Author

- [Stefan Urbanek](mailto:stefan.urbanek@gmail.com)
