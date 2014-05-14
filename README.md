Crsstat2
========

Oracle RAC ~ crsstat.sh v2.0 (11g, 12c)

From >> http://southeastdboes.blogspot.ca/2014/05/exa-iting-crsstat-different-perspective.html

 EXA-iting - news - crsstat (11g & 12c) a different perspective


SCRIPT for ORACLE RAC
crsstat (11g, 12c)


Introduction
The crsstat script (Supports both 11g & 12c) is designed to display Oracle RAC Cluster Status formatted for ease of monitoring. 

The script should not be used to change or replace any existing scripts that are provided/available by/in installed software. This script is not supported by Oracle for any issues. It is recommended to test the script before deploying. Always deploy scripts in a DIRECTORY (preferably shared) outside and away from the Software File System.

                            NOTE: The SCRIPT has been tested in bash and ksh Shells only at this time.

ENJOY!
Setup
Keeping it simple below are the set of steps to get going. 

1.        Copy script on a local/shared directory accessible on HOST
NOTE: Script is provided in “APPENDIX (Script)” at the bottom of this document.
           cd <script_directory>
           vi crsstst                                 # copy content from "APPENDIX (Scripts}" at the bottom of this blog.

2.        Update GRID_HOME in this Script under “MODIFY AS NEEDED”
cd <script_directory>
vi ./crsstat
GRID_HOME=<grid_home>

3.        Change execution privileges
chmod 777 ./crsstat

4.        Setup and export PATH to setup ENVIRONMENT
i.e. SCRIPT LOCATION:      /u01/SCRIPTS/crsstat # User Defined Location
export PATH=$PATH:/u01/SCRIPTS
which crsstat         # should display the crsstat location

Commands are limited to FOUR options:

1.        Display SCRIPT HELP.
         crsstat h
2.        List CRS resources.
crsstat res
3.        Display CRS Resource.
crsstat <resource_name>
# NOTE: <resource_name> can be a FULL NAME or a SUBSTRING. i.e. “database” OR “data” OR “base” etc…
4.        Display CRS FULL OUTPUT
crsstat

