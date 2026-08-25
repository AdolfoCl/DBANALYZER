# DBANALYZER

## STANDARD DATA SET ANALYSIS REPORT

It generates a printed report showing the active and deleted records and the use of disk space for all standard data sets in a DMSII database of the UNISYS MCP Operating System.
 
## How to compile

From CANDE: 
```
C SYMBOL/DBANALYZER AS DBANALYZER WITH COBOL85
```

## How to run

From CANDE:
```
RUN DBANALYZER;FILE DASDL(TITLE = <DESCRIPTION FILE TITLE>)
```

## Results
The following is the generated report format. The database below is made up:
SAMPLEDB, with figures consistent with each other, to show the layout.
```
SDSANAL                                            * STANDARD DATASET ANALYSIS *                                 14/03/2025 09:22:41 
DATA BASE:  SAMPLEDB             UPDATE LEVEL   7                                                                          PAGE   1 
                 STR                      FILE SIZE   .....A R E A S......   ......RECORD SPACES.......      ACTIVE       DASDL    % 
DATA SET NAME    NUM   FAMILY NAME        (SECTORS)   ALLOWED  IN USE   %    ALLOCATED    DELETED    %      RECORDS       POPUL.   SAT
-------------    ---   -----------        ---------   --------------------   --------------------------     -------     --------  ---
GLOBALS            1   DBPACK01                180       2        1  50.0           1          0    0.0            1            1 100.0
CUSTOMER           5   DBPACK01             24,120     340       24   7.1      41,880      1,204    2.9       40,676      500,000   8.1
ADDRESS            7   DBPACK01             10,080     210       10   4.8      17,332        288    1.7       17,044      400,000   4.3
CONTACT            9   DBPACK01              5,040     156        5   3.2       8,104          0    0.0        8,104      250,000   3.2
PRODUCT           12   DBPACK01              3,528      88        4   4.5       6,215         41    0.7        6,174      120,000   5.1
PRICE-LIST        14   DBPACK01              1,008      40        1   2.5         940          0    0.0          940       60,000   1.6
STOCK             16   DBPACK01              7,056     175        7   4.0      12,480        615    4.9       11,865      300,000   4.0
ORDER-HEAD        20   DBPACK01             50,400     720       50   6.9      88,104      2,310    2.6       85,794    1,500,000   5.7
ORDER-LINE        22   DBPACK01            151,200     980      151  15.4     402,556     10,877    2.7      391,679    5,000,000   7.8
SHIPMENT          25   DBPACK01             20,160     480       20   4.2      33,012        704    2.1       32,308      800,000   4.0
INVOICE           28   DBPACK01             35,280     615       35   5.7      61,230      1,508    2.5       59,722    1,200,000   5.0
INVOICE-LINE      30   DBPACK01            100,800     900      100  11.1     268,401      6,122    2.3      262,279    4,000,000   6.6
PAYMENT           33   DBPACK01             15,120     402       15   3.7      25,744        390    1.5       25,354      700,000   3.6
SUPPLIER          36   DBPACK01              1,008      36        1   2.8         612          0    0.0          612       20,000   3.1
EMPLOYEE          40   DBPACK01              2,016      64        2   3.1       1,877         22    1.2        1,855       50,000   3.7
AUDIT-EVENT       45   DBPACK01             60,480     850       60   7.1     155,203          0    0.0      155,203    3,000,000   5.2
```

## Credits
Adapted from **GREGORY'S A-SERIES TECHNICAL JOURNAL**
VOLUME 2, NUMBER 7      AUGUST, 1988
PAGE 261  **"EXPLORING DMSII WITH COBOL"**
