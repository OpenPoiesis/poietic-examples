# Poietic Demos

Demo designs for the Poietic toolkit.

To play with the demos, you need the
[Poietic Toolkit](https://github.com/OpenPoiesis/Poietic-swift).


## Contents

- **Thinking In Systems** – flows and stocks models from the [book](https://www.goodreads.com/book/show/3828902-thinking-in-systems)
  *Thinking in Systems: A Primer* by Donella Meadows


## Running the demos

To run a demo, you need the [Poietic Toolkit](https://github.com/OpenPoiesis/PoieticCore).

Please refer to a README file included with each folder for more details.

To run the demos you can use the included `run` command. It requires the `poietic` tool
executable to exist somewhere. Can be specified explicitly using the `POIETIC` environment
variable.

To use the `run` command type, for example:

```bash
./run ThinkingInSystems/Capital.poieticframe
```

If this demo project directory share the same parent directory as the Poietic Core,
then make sure that the tool has been built and then use the command like this::

```bash
export POIETIC=../PoieticCore/.build/debug/poietic
./run ThinkingInSystems/Capital.poieticframe
```

### Manual Method

1. Chose a location of your database and store the path in `POIETIC_DESIGN` environment
   variable with: `export POIETIC_DESIGN="demo.poietic"`
2. Creating a new database: `poietic new`
3. Importing the demo package: `poietic import PATH_TO_MODEL_FOLDER`
4. Running the model: `poietic run`

### Example

Requires [Gnuplot](http://gnuplot.info), on Mac can be installed using `brew install gnuplot`.

Make sure that you have the `poietic` tool compiled, add it to your PATH or add it to the
alias in the script below.

This demo runs the `ThinkingInSystems/Capital` example and generates output in the `./out`
directory where you can find `output.csv` with all the simulation states, `*.gnuplot` files
containing instructions for plotting and `*.png` files with charts. The charts
are defined within the model as `Chart` objects.

```sh
# Alias the poietic tool, if we do not have it in PATH
alias poietic="swift run poietic"

# Path to the database.
export POIETIC_DESIGN="demo.poietic"

# Create a new empty database.
#
# This will create a new database by importing a frame and automatically
# connecting parameters.
#
poietic new --import ThinkingInSystems/Capital.poieticframe --auto-parameters

# Run the model and generate output into the ./out directory.
poietic run --steps 150 -f gnuplot -o ./out

# Create charts using gnuplot.
cd ./out
gnuplot *.gnuplot

```


## Development Notes

The included demos are in early stage of development. The file format of
the demos is not yet stable and might change. If you create your own
derivatives, please be aware, that they might or might not work in the future.


## Author

- [Stefan Urbanek](mailto:stefan.urbanek@gmail.com)



