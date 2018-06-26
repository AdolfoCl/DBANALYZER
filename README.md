# DBANALYZER

## STANDARD DATA SET ANALYSIS REPORT

It generates a printed report showing the active and deleted records and the use of disk space for all standard data sets in a DMSII database of the UNISYS MCP Operating System.
 
## How to compile

From CANDE: 
```
C SYMBOL/DBANALYZER AS DBANALYZER WITH DMALGOL
```

## How to run

From CANDE:
```
RUN DBANALYZER;FILE DASDL(TITLE = <DESCRIPTION FILE TITLE>)
```

## Results
The following is the generated report format
```
SDSANAL                                            * STANDARD DATASET ANALYSIS *                                 22/06/2018 18:41:02 
DATA BASE:  TVPRGDRB             UPDATE LEVEL   3                                                                           PAGE   1 
                 STR                      FILE SIZE   .....A R E A S......   ......RECORD SPACES.......      ACTIVE       DASDL    % 
DATA SET NAME    NUM   FAMILY NAME        (SECTORS)   ALLOWED  IN USE   %    ALLOCATED    DELETED    %      RECORDS       POPUL.  SAT
-------------    ---   -----------        ---------   --------------------   --------------------------     -------     --------  ---
ABOCO             27                            520       2        1  50.0           0          0                 0        3,000  0.0
ACTA              28                          1,003      16        1   6.2           0          0                 0        5,000  0.0
AFDEC             30                          1,005     502        1   0.1           0          0                 0    1,000,000  0.0
AGINS             31                          1,007     127        1   0.7           0          0                 0      300,000  0.0
...
```

## Credits
Adapted from **GREGORY'S A-SERIES TECHNICAL JOURNAL**
VOLUME 2, NUMBER 7      AUGUST, 1988
PAGE 261  **"EXPLORING DMSII WITH COBOL"**
