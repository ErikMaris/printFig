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
```matlab
p = printFig();
```
or directly with arguments setting the path to a specific save folder.
```
p = printFig('savepath','path to save folder, e.g. ../results/figures/current_project')
```
Now plot a figure and save it directly to 




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
