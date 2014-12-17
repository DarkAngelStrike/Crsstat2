From: https://www.linkedin.com/pulse/20140722201045-18529757-exa-iting-news-crsstat-11g-12c-a-different-perspective

Keeping it simple below are the set of steps to get going.

1. Copy script on a local/shared directory accessible on HOST
NOTE: Script is provided in “APPENDIX (Script)” at the bottom of this document.
cd <script_directory>
vi crsstst # copy content from "APPENDIX (Scripts}" at the bottom of this blog.

2. Update GRID_HOME in this Script under “MODIFY AS NEEDED”
cd <script_directory>
vi ./crsstat
GRID_HOME=<grid_home>

3. Change execution privileges
chmod 777 ./crsstat

4. Setup and export PATH to setup ENVIRONMENT
i.e. SCRIPT LOCATION: /u01/SCRIPTS/crsstat # User Defined Location
export PATH=$PATH:/u01/SCRIPTS
which crsstat # should display the crsstat location

Commands are limited to FOUR options:

1. Display SCRIPT HELP.
crsstat h
2. List CRS resources.
crsstat res
3. Display CRS Resource.
crsstat <resource_name>
# NOTE: <resource_name> can be a FULL NAME or a SUBSTRING. i.e. “database” OR “data” OR “base” etc…
4. Display CRS FULL OUTPUT
crsstat
