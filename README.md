Analyses to recreate the results in the manuscript **"Rumen bacterial community structure impacts feed efficiency in beef cattle"** by Paz by Paz et al. 2017 in ISME J. The analyses are separated into several R Markdown files.

Follow the instructions below to setup the same environment used to analyze the data and render the R Markdown files. Adhere to the delineated order as succeeding R Markdown files depend on previous results.

    1. data_curation.Rmd
	2. generate_OTU_table.Rmd
	3. qc_bacterial.Rmd
	4. feed_efficiency_phenotype.Rmd
	5. alpha_diversity.Rmd
	6. beta_diversity.Rmd
	7. differential_OTUs.Rmd
    8. forward_stepwise_regression.Rmd

Due to licensing constraints, USEARCH could not be included in the setup. The current dataset requires more than the 4Gb RAM allowed in the no-charge 32-bit version, thus the paid license [USEARCH 64-bit version](http://drive5.com/usearch/buy64bit.html) was used. USEARCH outputs required in the analyses are provided in the usearch_outputs directory.

Clone the github repository and run the setup.sh script

git clone https://github.com/enriquepaz/RumenMicrobiome_Beef.git
cd RumenMicrobiome_Beef
./setup.sh

Anaconda is downloaded and prompts you during installataion of the packages. The prompts are roughly as follows:

Press enter to view the license agreement
Press enter to read the license and q to exit
Accept the terms
Prompts you where to install anaconda. Simply type anaconda to create a directory within the current directory. Should be: [/Users/user/anaconda] >>> anaconda
No to prepend anaconda to your path. Choosing yes should not impact the installation though.
Will be asked a few times if you wish to proceed with installing the packages...agree to it.
After installation, enter 'source anaconda/bin/activate rumenVirome' on the command line to activate the virtual enviornment

To render one of the RMarkdown files: R CMD BATCH --no-restore --no-save '--args file1.Rmd' render.R




