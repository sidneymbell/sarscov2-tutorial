# Template repository for SARS-CoV-2 analyses    

This repository is a template and tutorial for running a basic phylogenetic analysis on SARS-CoV-2 data.
We've created these resources with the goal of enabling Departments of Public Health to start using Nextstrain to understand their SARS-CoV-2 genomic data within 1-2 hours.

_If you're looking for the SARS-CoV-2 analyses used for the main Nextstrain builds, please see [this repository instead](https://github.com/nextstrain/ncov)._

## Overview: complete walkthrough
### Getting started with analysis  
_The starting point for this section is a FASTA file with sequence data + a TSV file with metadata. You can also just use our example data to start._

[1. Preparing your data](docs/data-prep.md)  
[2. Set up and installation](docs/setup.md)  
[3. Orientation: analysis workflow](docs/orientation-workflow.md)  
[4. Orientation: which files should I touch?](docs/orientation-files.md)  
[5. Running & troubleshooting](docs/running.md)   
[6. Customizing your analysis](docs/customizing-analysis.md)  
[7. Customizing your visualization](docs/customizing-visualization.md)

### Getting started with visualization & interpretation  
_The starting point for this section is a JSON file. You can also just use our examples to start._

[8. Options for visualizing and sharing results](docs/sharing.md)  
[9. Interpreting your results](docs/interpretation.md)  
[10. Writing a narrative to highlight key findings](docs/narratives.md)  
_11. Case studies: interpreting your data (coming soon!)_  

## Quickstart    

If you'd prefer, you can also start by running a basic analysis on the provided example data and/or visualizing the output with the [auspice.us](auspice.us) drag-and-drop viewer. If you get stuck at any point, you can find more detailed instructions in the full tutorial outlined above.

We also recommend [this 1-hour video overview](https://youtu.be/m4_F2tG58Pc) by Heather Blankenship on how to deploy Nextstrain for a Public Health lab.

#### 1. Clone this repository  
```
git clone https://github.com/nextstrain/sarscov2-tutorial.git
```

#### 2. Install augur for bioinformatics
```
python3 -m pip install nextstrain-augur
```

MacOS:
```
brew install mafft iqtree raxml fasttree vcftools
```

Ubuntu/Debian:  
```
sudo apt install mafft iqtree raxml fasttree vcftools
```

#### 3. Run basic analysis on example data  
```
sarscov-tutorial$ snakemake --profile ./my-analyses/example
```


#### 4. Visualize your results (or our example output)  
Go to `https://auspice.us` in your browser.
Drag and drop `./auspice/sarscov2.json` (or any other JSON in this directory) anywhere on the screen.

Voila!


## Help  

If something in this tutorial is broken or unclear, please [open an issue](XXX) so we can improve it for everyone.  

If you have a specific question, post a note over at the [discussion board](XXX) -- we're happy to help!
