**Source:**

Oracle RAC - Simplifying Viewing your CRS Stats - crsstat (Sudhakar Kotagiri) \
https://sudhakarkotagiri.blogspot.com/2018/08/oracle-rac-simplifying-viewing-your-crs.html

**Setup:**

Keeping it simple below are the set of steps to get going.

1.       Copy script to a file on a local/shared directory accessible on HOST
           
            NOTE: Script is provided in “APPENDIX” at the bottom of this document.
           
            cd <script_directory>
            vi db12c_env # copy content from "APPENDIX (Environment Setup Script)" at the end of this blog
            vi crsstst # copy content from "APPENDIX (Script}" at the end of this blog.

2.      Update GRID_HOME in this Script under “MODIFY AS NEEDED”
            
             cd <script_directory>
             ./crsstat
            GRID_HOME=<grid_home>

3.      Change execution privileges as needed
             
             chmod  744 ./db_12c_env
             chmod 777 ./crsstat

4.      Setup and export PATH to setup ENVIRONMENT
             
            Set environment using env file "db_12c_env" or in OS profile file.

5.      Commands are limited to FOUR options at this time:
                        a. Display SCRIPT HELP.
                                    crsstat h
                        b. List CRS resources.
                                    crsstat res
                        c. Display CRS Resource.
                                    crsstat <resource_name>
                        # NOTE: <resource_name> can be a FULL NAME or a SUBSTRING. i.e.                                                 “database” OR “data” OR “base” etc…
                        d. Display CRS FULL OUTPUT
                                    crsstat
