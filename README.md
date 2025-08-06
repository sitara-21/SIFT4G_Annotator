# Annotating a VCF file

To run the SIFT 4G Annotator on Linux or Mac via command line, type the following command into the terminal:
`java -jar <Path to SIFT4G_Annotator .jar file> -c -i <Path to input vcf file> -d <Path to SIFT4G database directory> -r <Path to your results folder> -t`

*Example:* 
```
java -jar /n/data1/hms/dbmi/gulhan/lab/ankit/scripts/SIFT4G_Annotator/SIFT4G_Annotator.jar -c -i /n/scratch/users/a/ans4371/merged_bams/Haplotypecaller_output/Plt/.HaplotypeCaller/platelet_positive_merged_RG/platelet_positive_RG.g.vcf.gz.final.vcf -d /n/data1/hms/dbmi/gulhan/lab/ankit/misc_files/HybridCTC/SIFT_db/GRCm38.74 -r /n/data1/hms/dbmi/gulhan/lab/ankit/misc_files/HybridCTC/SIFT_output -t
```

## Options
Option | 	Description
--- | --- 
-c 	| To run on command line
-i 	| Path to your input variants file in VCF format
-d 	| Path to SIFT database directory
-r 	| Path to your output results folder
-t 	| To extract annotations for multiple transcripts (Optional)

## Troubleshooting

If you've built a database following https://github.com/pauline-ng/SIFT4G_Create_Genomic_DB, make sure there are non-empty <chrom>.gz and <chrom>regions files
Find list of supported databases here: https://sift.bii.a-star.edu.sg/sift4g/public/

If your database files start with a 'chr', you must rename them without the 'chr' for the annotator to work.

*Example:* 
`mv chr19.gz -> 19.gz; mv chr19.regions 19.regions; mv chr19_SIFTDB_stats.txt 19_SIFTDB_stats.txt`
