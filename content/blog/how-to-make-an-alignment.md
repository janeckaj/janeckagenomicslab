+++
title = "Making an alignment"
tags = ["tree buildin"]
categories = ["phylogenetics"]
banner = "img/banners/thumbnail-building-msa-mega-720.PNG"
twitter_author = "GenomicsJanecka"
+++

### How to build a basic sequence alignment in MEGA

The program MEGA is one of the most user friendly phylogenetics tools to work with sequences. It has a suite of tools with which you can do everything from building alignments to reconstructing trees to running some basic selection tests. In this article, I am going outline the steps for importing a file with sequences and making an alignment. MEGA provides two free algorithms, Clustal and Muscle, of these Muscle is considered a better aligner, but in most cases both of them produce comparable alignments. You can download both of these program for free and use them stand-alone, however, what is nice about MEGA is that it integrates them into a comprehensive genetics analysis package.

I made a YouTube video on my channel where I go through these steps, in case you prefer to watch a tutorial or need more clarification.

Making a basic sequence alignment using MEGA

1. Find your favorite gene in NCBI’s HomoloGene database record of curated homologs and put together your sequence file.
- Go to the main NCBI website, select the “HomoloGene” in the dropdown menu, and search for your gene using its official gene symbol (for example HIF1A). 
- Go to the HomoloGene record for your gene. To get the mRNA nucleotide sequences for the species you want, click on the “Download” button in the upper right of the page. 
- In the dropdown menu, select “mRNA”. 
- Check the boxes of the species you want. To follow along with my YouTube video select human (H. sapiens), chimp (P. troglodytes), dog (C. lupus), rat (R. norvegicus), and chicken (G. gallus). 
- Then click download. This will download a flat text file with the sequences in fasta format. 

2. Open the file in a text editor (I recommend the text editor in MEGA but you can also use something like Notepad). Change the name of the sequences in the file after the “>” to just the species, gene symbol, and accession number, all separated by dashes. For example, “human-hif1a-NM_001530.3”. Save the file under a informative name such as “genename-mrna-v2.fas” For example, “hif1a-mrna-v2.fas”. As a tip, do not overwrite sequence files (or any data files for that matter) once you make major changes to them, just save them under a different version. This way you can always go back to the earlier file.


3. Import the fasta file in to MEGA by opening MEGAX, selecting the “Align” tool, then “Edit/Build Alignment” and “Retrieve sequences from a file” and click “OK”. In the open file window that pops up, navigate to the folder with your downloaded file, at the bottom right, make sure that the format is “FASTA” so that your file shows up, select it, and click “Open”. This will open an “Alignment Explorer” window with your sequences. Make sure that each sequence name is correct, and that all your sequences are there. If your file does not open correctly, go back and double check that all your sequences are in fasta format, that there are no unnecessary characters, and it is a plain text file. 


4. To build a multiple sequence alignment, in the “Alignment Explorer” window, select the “Align using the MUSCLE algorithm” tool, then “Align DNA”. In the confirmation window with “Nothing selected for alignment. Select All?” click “OK”. A window with the MUSCLE options will open. Leave the parameters as default and then click “OK”. A window may open asking if you want to remove gaps before aligning, if you get that check “Yes”. The MUSCLE program will run with a window showing the progress. After a few seconds to minutes (depending on how many sequences you have and how long they are) the alignment will be completed and appear in MEGA’s alignment explorer window. Using the scroll bar at the bottom look over your alignment to make sure it looks reasonable. Finally, save the alignment in two formats. First, in the alignment explorer, click on “Data”, select “Save Session”, and save it with name “yourlastname-genesymbol-aligned.mas” (for example: “janecka-hifqa-mrna-aligned.mas”). Second, click “Data” and select “Export Alignment” then “Fasta Format”, and save it with the name “yourlastname-genesymbol-aligned.fas”.


Now you are ready to do some sequence analysis! To see how you can build the best phylogenetic tree with bootstrap values in MEGA see my [YouTube video](https://www.youtube.com/watch?v=xKS5qZwl1GY&t=28s "Making tree with BS values in Mega").
