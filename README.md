# Poietic Examples

Example models for the Poietic Flows toolkit.

To play with the demos, you need the
[Poietic Flows](https://github.com/OpenPoiesis/PoieticFlows) installed.


## Contents

- **Thinking In Systems** – flows and stocks models from the [book](https://www.goodreads.com/book/show/3828902-thinking-in-systems)
  *Thinking in Systems: A Primer* by Donella Meadows


## Running the demos

Make sure you have the `poietic` command-line tool from the
[Poietic Flows](https://github.com/OpenPoiesis/PoieticFlows) package installed.
Follow the installation instructions contained in the package.


There are two ways to run and explore the demos: use a convenience
`run` script or do it manually. Here are the methods described in more detail.

### Convenience script

To run the demos you can use the included convenience `run` script.
It requires the `poietic` tool executable to exist somewhere.
Can be specified explicitly using the `POIETIC` environment variable.

Use the the `run` command type, for example:

```bash
./run ThinkingInSystems/Capital.poieticframe
```

The command will create output in the `./out` directory with a CSV file
containing the simulation result. 

Extras:

- If you have [Gnuplot](http://gnuplot.info) installed, then
  chart images will be generated.
- If you have [Graphviz](https://graphviz.org) installed, then the model
  diagram image will be created.

### Manual Method

1. Create a new database: `poietic new`
2. Importing the demo package: `poietic import Basic/Interest.poieticframe`
3. To make sure all parameter connections are correct, for some packages you might need to run `poietic edit auto-parameters`.
4. Run the simulation: `poietic run` and see the simulation results in the
   standard output.

Explore the included `run` shell script or explore `poietic --help` and `--help`
of its subcommands to learn more what can be done with the example models.


## Development Notes

The included demos are in early stage of development. The file format of
the demos is not yet stable and might change. If you create your own
derivatives, please be aware, that they might or might not work in the future.


## Author

- [Stefan Urbanek](mailto:stefan.urbanek@gmail.com)



