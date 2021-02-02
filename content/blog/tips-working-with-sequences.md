+++
title = "Tips for working with sequences"
tags = ["editing sequences", "alignment", "fasta files"]
categories = ["phylogenetics"]
banner = "img/banners/helpful-tips-720.jpg"
twitter_author = "GenomicsJanecka"
+++

### Here are some tips when working with sequences and alignments that will help with some of the most common problems I have seen (and experienced)

- Make sure folders on your computer are set to show extensions. If they are not, you may inadvertently name a file with double extensions such as “myfile.fas.txt”. Then the program you are trying to use may not see it or recognize it. To double check and correct your file name, right click the file and select “Properties” of “Get info”.

- Make sure that your fasta file is saved as a flat text file. Otherwise [MEGA](https://www.megasoftware.net/ "Molecular Evolionary Genetics Analysys") (and other sequence analysis programs) will not be able to import it. If you are not sure what type of text file it is, open it in Word and then do “File” > “Save As” and select “Plain Text (*.txt) and save it. Then change the file extension to “.fas” and retry importing the fasta file.

- Do not have any spaces in file names or sequence names. Many downstream sequence alignment programs do not accept names with spaces, so to avoid any issues, just use either dashes or underscores. 

- The simplest format that is easiest to work with for sequences is the fasta format. Try to stick with that for all your sequence files, unless some specific program you are using needs a different format.

- If for some reason MEGA (or another program) keeps giving you an error, and you are sure you have a flat text file, the sequences are formatted correctly, and the extension is correct, then there are likely hidden characters in your file that you do not see. This sometimes happens when you download text files from the web using certain browsers. To correct this, open the file in a regular Microsoft Office Word editor. Select the “Show all characters tool” and then remove any characters that should not be there, and re-save it as a flat text file, again change the extension back “.fas”, and try re-importing it.

- In most cases alignment programs do not care when it comes to what you are having them align. How dare they??? Oh, they dare, they are cold hearted - just like statistical tests. Does a t-test care if you use a data set that violates the t-test’s assumptions? Nope, it will still give you a test statistic and a p-value, even though they are meaningless. Just like you are the one who needs to decide if it is appropriate to use a t-test, you also need to be the one to decide which sequences should be aligned.  This means you need to have some basic understanding of what you are aligning and why. The main, and most important assumption, is that sequences you are aligning are homologous. Alignment programs will align non-homologus sequences and often even ones that have virtually no sequence similarity. For example, open the HIF1A fasta that I show you how make to in my [alignment video](https://www.youtube.com/watch?v=Pq4Cy76zNew "Making an alignment with MEGA"), paste in a beta globin sequence, and resave it. Now try to align it in MEGA. Muscle will still align it. It will be a meaningless alignment, but it will still be an “alignment”. My point here:  Make sure your fasta file consists of homologs with sufficient sequence similarity to be legitimately aligned, and is free of clearly non-homologous sequences, mislabeled sequences, and sequences with major sequencing errors. 

- You can change the parameters to optimize or improve an alignment. A simple, crude way to do it (that still works pretty well) is to try changing the various settings and then compare your alignments visually. 

- There are more alignment programs that perform better for some kinds of sequences than others. For example, T-Coffee is  arguably considered the best for protein coding sequences because it uses structural models and has other sophisticated ways to iteratively improves the alignment as it builds it. To give different aligners a try you can access them through the [EBI alignment page](https://www.ebi.ac.uk/Tools/msa/ "Multiple Sequence Alignment Tools").

- If you are aligning very divergent sequences, there will be some regions that are poorly aligned and others that will align well. You need to inspect the alignment and make a conscious decision as to whether or not to include the poorly aligned regions in your downstream analysis.
