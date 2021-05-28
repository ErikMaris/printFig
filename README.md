# printFig

printFig is a MATLAB tool for exporting figures via the command line and in scripts.

## Requirements
Please check 'requirements.txt' for the software's dependencies.

## Installation
1. Download the software by clicking the dropdown menu 'Code' and click 'Download ZIP'.
2. Unpack the zip file and move the folder to your desired location.
3. Go to 'requirements.txt' and move the dependencies to the folder LifetimeAnalysis/bin/external
4. Open MATLAB and add the folder ("Add with subfolders") to your MATLAB path.

![image](https://user-images.githubusercontent.com/77492856/119955717-99be7300-bfa0-11eb-8c8a-0a6765b572dc.png)

The software is now ready to use.

5. Open the demo script in LifetimeAnalysis/src/scripts/demo/demo_script.mlx and run the code.

## Usage

Initialize a printFig object
```
p = printFig();
```
or directly with arguments setting the path to a specific save folder.
```
p = printFig('savepath','path to save folder, e.g. ../results/figures/current_project');
```
Let's set the units in the plotExt variable to png only, which has the flag '-dpng'
```
p.plotExt = {'-dpng'};
```
all options are given here: https://nl.mathworks.com/help/matlab/ref/saveas.html and 'fig' to save the figure as MATLAB Figure file.

Now plot a figure with the print command and save it directly to the save folder. In this example, we name the file 'result'
```
p.print('result');
```
and the figure 'result.png' is written to the save folder.

Alternatively, the GUI is launched via the command
```
ExportFigures_App(parent)
```
where the parent is an object with field parent.printFig with contains a 'printFig' object. This is solely meant for integration with GUI's and is not (yet) available as stand-alone.

## Documentation

Type
```
doc printFig
```
for the documentation or
```
help printFig.print
```
for the documentation of a specific function, which is the 'print' function in this example. 

## Project organization
- PG = project-generated
- HW = human-writable
- RO = read only
```
.
├── .gitignore
├── CITATION.md
├── LICENSE.md
├── README.md
├── requirements.txt
├── bin                <- Compiled and external code, ignored by git (PG)
│   └── external       <- Any external source code, ignored by git (RO)
├── config             <- Configuration files (HW)
├── data               <- All project data, ignored by git
│   ├── processed      <- The final, canonical data sets for modeling. (PG)
│   ├── raw            <- The original, immutable data dump. (RO)
│   └── temp           <- Intermediate data that has been transformed. (PG)
├── docs               <- Documentation notebook for users (HW)
│   ├── manuscript     <- Manuscript source, e.g., LaTeX, Markdown, etc. (HW)
│   └── reports        <- Other project reports and notebooks (e.g. Jupyter, .Rmd) (HW)
├── results
│   ├── figures        <- Figures for the manuscript or reports (PG)
│   └── output         <- Other output for the manuscript or reports (PG)
└── src                <- Source code for this project (HW)

```

## License

This project is licensed under the terms of the [MIT License](/LICENSE.md)
