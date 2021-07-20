# Indoor_Localization

This is a project done as a part of the course Smart Sensing for IoT
which deals with Trilateration of a Node in a 100x100 grid given the range measurements from
3 access points (APs).

Both Brute force methods as well as Least Squares Optimization methods using LMFIT are used
to trilaterate and analyse error performance and time.

The detailed report on Dataset Generation, Localization, Observations, Impact of Anchor Points
and Geometric Dilution of Precision can be found [here]().

## Dependencies
* LMFIT
* Numpy
* Matplotlib
* AST
* argparse
* linecache, math, os
* bash commands - ls, grep, xargs, rm

## generate_dataset.py
Generates the following dataset:

>Running this file deletes old dataset files if present. Hence backup if necessary. It also
asks for conformation while running.

To run: `python3 generate_dataset.py`

## brute_force_localization.py
This displays a random heatmap of rms cost function each time you run it.
To run: `python3 brute_force_localization.py`

## trilaterization.py
Generates the following trilaterization data depending on the brute-step given:

>Running this file deletes corresponding old trilaterization files if present. Hence backup if
necessary. It also asks for conformation while running.

To run: `python3 trilaterization.py [--brute_step {int}]`

If no brute_step if given it defaults to using 50,50 as starting point.
Brute Step 10 and 5 take atleast 30mins to complete.

## trilaterization_errors_per_range_error.py
Generates 3 plots and prints some useful information in the terminal as given in the report.
Use q to navigate from one plot to the next.
Shows CDF, PDF and Violin Plot.

To run: `python3 trilaterization_errors_per_range_error.py [--file_id {brute_step}]`

`file_id` is the prefix of the files to be used which happens to be the `brute_step`. If nothing is given it defaults to
using files which have prefix "_" which corresponds to starting point 50,50.

## trilateration_errors_per_anchor_triplet.py
Generates a bar graph plot of median errors per anchor configuration.
To run: `python3 trilaterization_errors_per_anchor_triplet.py [--file_id {brute_step}] [--show_before_after]`

`file_id` is same as the previous script.
The `show_before_after` flag displays the scatter plot for each anchor triplet. Since, 400 plots have to be seen to
end the script, Ctrl+C can be used to end the script.
Each time the script is run a random range error order is used so that you don't have to see all 100 before going to
the next one.
Both the flags can be used in combination to read different brute_step files.
Use q to navigate from one plot to the next.
