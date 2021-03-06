# irma-scripts
Stand-alone scripts deployed to Irma

These scripts are deployed to `/proj/ngi2016001/private/scripts` by the irma-provision process.

The scripts should contain instructions for usage unless it's obvious how to use them. Preferably, invoking a script 
without arguments should be safe to run without any side effects and only display usage instructions on stdout

__NEVER__ put any passwords, usernames, tokens, user data or other sensitive information in the scripts. If such
information is required by the script, rely on reading it from an environment variable instead. 

When adding a new script to this repository, be sure to add a brief description of its purpose below:

* __concordance_check.sh__ - bash script to perform concordance check between a vcf file with genotypes and a vcf file 
with variant calls
* __find_unorganized_flowcells.sh__ - bash script that verifies that the organized project folder under the DATA 
directory contains all runfolders in incoming having data from the project in them
* __link_project_sisyphus_reports.sh__ - bash script that links sisyphus runfolder reports from the incoming folder to
the corresponding project folder under ANALYSIS
* __set_charon_genotyping_status.sh__ - bash script to set the genotyping status field in charon to a specified value 
for samples present in a supplied vcf file
* __statdump_to_json.pl__ - perl script that can parse a statdump zipfile created by sisyphus and output the statistics
as json
