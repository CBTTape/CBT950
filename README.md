# CBT950
Converted to GitHub via [cbt2git](https://github.com/wizardofzos/cbt2git)

This is still a work in progress. 
Due to amazing work by Alison Zhang and Jake Choi repos are no longer deleted.

```
//***FILE 950 is from Norbert Haas and contains many useful tools,  *   FILE 950
//*           mostly written in REXX.                               *   FILE 950
//*                                                                 *   FILE 950
//*           Most of these tools have REXX'es and panels.          *   FILE 950
//*                                                                 *   FILE 950
//*           There are many more tools here than we describe       *   FILE 950
//*           below.                                                *   FILE 950
//*                                                                 *   FILE 950
//*           Some of these products are commented in German.       *   FILE 950
//*           We tried to translate most of them into English.      *   FILE 950
//*                                                                 *   FILE 950
//*           email:    nh@noadatex.de                              *   FILE 950
//*           website:  www.noadatex.de                             *   FILE 950
//*                                                                 *   FILE 950
//*           email:    sbgolob@cbttape.org                         *   FILE 950
//*                                                                 *   FILE 950
//*       Partial Description:                                      *   FILE 950
//*                                                                 *   FILE 950
//*       AUTOMAT  - A quick method of setting up multiple split    *   FILE 950
//*                  sessions in ISPF, as soon as you get into      *   FILE 950
//*                  ISPF.  (Note: IBM's =XALL command gets rid     *   FILE 950
//*                  of them quickly when you want to close them    *   FILE 950
//*                  down.)                                         *   FILE 950
//*                                                                 *   FILE 950
//*       BACKUP   - Make a quick backup of a dataset from an       *   FILE 950
//*                  ISPF 3.4 list (DSLIST).                        *   FILE 950
//*                                                                 *   FILE 950
//*       CHALL    - Change a string to another string, globally    *   FILE 950
//*                  in a pds.                                      *   FILE 950
//*                                                                 *   FILE 950
//*       CUAATTR  - Summary of color and other attribute codes in  *   FILE 950
//*                  ISPF panels.                                   *   FILE 950
//*                                                                 *   FILE 950
//*       FSCREEN  - Find characters on the screen.                 *   FILE 950
//*                                                                 *   FILE 950
//*       INTER    - Small REXX test interpreter                    *   FILE 950
//*                                                                 *   FILE 950
//*       KONKAT   - A REXX function to concatenate two strings     *   FILE 950
//*                  inside a REXX.                                 *   FILE 950
//*                                                                 *   FILE 950
//*       NOT      - A REXX function like "NOT"                     *   FILE 950
//*                                                                 *   FILE 950
//*       ODER     - A REXX function to "OR"                        *   FILE 950
//*                                                                 *   FILE 950
//*       RULER    - Edit macro to put a ruler into the edit        *   FILE 950
//*                                                                 *   FILE 950
//*       SAVE     - Double a dataset (earlier version of BACKUP)   *   FILE 950
//*                                                                 *   FILE 950
//*       WHOHOLDS - A REXX function to tell you if a dataset       *   FILE 950
//*                  is in use.                                     *   FILE 950
//*                                                                 *   FILE 950
//*       XMAN     - An easy TSO TRANSMIT (XMIT) interface in       *   FILE 950
//*                  ISPF.                                          *   FILE 950
//*                                                                 *   FILE 950
//*       ALL MEMBERS OF THIS DATASET:                              *   FILE 950
//*                                                                 *   FILE 950
//*       NAME       VER.MOD   LAST MODIFIED     SIZE   ID          *   FILE 950
//*       $$$#DATE    04.93   2017/01/06 00:22     12 CBT-493       *   FILE 950
//*       @FILE950    04.93   2017/01/06 00:22    116 CBT-493       *   FILE 950
//*       ADDUP       01.01   2017/01/05 09:23    104 NORBERT       *   FILE 950
//*       AREA        01.01   2017/01/05 09:23     37 NORBERT       *   FILE 950
//*       AUTOMAT     01.40   2017/01/05 09:23    290 NORBERT       *   FILE 950
//*       BACKUP      01.04   2017/01/05 09:23    339 NORBERT       *   FILE 950
//*       BACKUPH0    01.01   2016/12/19 12:37     37 NORBERT       *   FILE 950
//*       BACKUPH1    01.00   2017/01/02 10:07     17 NORBERT       *   FILE 950
//*       BACKUPH2    01.00   2016/12/19 12:35     19 NORBERT       *   FILE 950
//*       BACKUPH3    01.02   2017/01/05 09:10     32 NORBERT       *   FILE 950
//*       BACKUPH4    01.00   2017/01/02 10:07     20 NORBERT       *   FILE 950
//*       BACKUPH5    01.00   2017/01/02 10:07     20 NORBERT       *   FILE 950
//*       BACKUPH6    01.00   2016/12/19 12:37     19 NORBERT       *   FILE 950
//*       BACKUPH7    01.00   2017/01/02 10:07     19 NORBERT       *   FILE 950
//*       BACKUPP     01.04   2010/04/16 07:29     94 NORBERT       *   FILE 950
//*       BIG         01.01   2017/01/05 09:23    177 NORBERT       *   FILE 950
//*       BODY        01.01   2017/01/05 09:23     37 NORBERT       *   FILE 950
//*       BOX         01.01   2017/01/05 09:23    244 NORBERT       *   FILE 950
//*       CATCH       01.02   2017/01/05 09:23     39 NORBERT       *   FILE 950
//*       CFIND       01.01   2017/01/05 09:23     92 NORBERT       *   FILE 950
//*       CHALL       01.04   2017/01/05 09:23    133 NORBERT       *   FILE 950
//*       CHALLM      01.00   2016/10/07 00:31     36 NORBERT       *   FILE 950
//*       CHALLP      01.13   2017/01/05 09:10     67 NORBERT       *   FILE 950
//*       COLA        01.01   2017/01/05 09:23     94 NORBERT       *   FILE 950
//*       CUAATTR     01.04   2017/01/05 09:23    101 NORBERT       *   FILE 950
//*       CUTMEM      01.01   2017/01/05 09:23     26 NORBERT       *   FILE 950
//*       C2B         01.01   2017/01/05 09:23     23 NORBERT       *   FILE 950
//*       DATE        01.08   2017/01/05 09:23     56 NORBERT       *   FILE 950
//*       DISPMSG     01.02   2017/01/05 23:48     21 NORBERT       *   FILE 950
//*       DSINFO      01.01   2017/01/05 09:23    221 NORBERT       *   FILE 950
//*       D2B         01.02   2017/01/05 09:23     31 NORBERT       *   FILE 950
//*       ET          01.01   2017/01/05 09:23    111 NORBERT       *   FILE 950
//*       ET2         01.01   2017/01/05 09:23     81 NORBERT       *   FILE 950
//*       FF          01.02   2017/01/05 09:23     39 NORBERT       *   FILE 950
//*       FLAGCHGS    01.03   2017/01/05 09:23    158 NORBERT       *   FILE 950
//*       FSCREEN     01.00   2016/10/07 00:31     57 NORBERT       *   FILE 950
//*       INCL        01.01   2017/01/05 09:23     23 NORBERT       *   FILE 950
//*       INTER       01.02   2017/01/05 09:23     43 NORBERT       *   FILE 950
//*       KILL        01.01   2017/01/05 09:23    115 NORBERT       *   FILE 950
//*       KONKAT      01.02   2017/01/05 09:23     21 NORBERT       *   FILE 950
//*       LASTWORD    01.01   2017/01/05 09:23     15 NORBERT       *   FILE 950
//*       LCL         01.01   2017/01/05 09:23     50 NORBERT       *   FILE 950
//*       LCLP        01.01   2017/01/05 09:10     76 NORBERT       *   FILE 950
//*       LINFO       01.01   2017/01/05 09:23    170 NORBERT       *   FILE 950
//*       MCANCEL     01.01   2017/01/05 09:23     15 NORBERT       *   FILE 950
//*       MIRACLE     01.00   2017/01/05 09:23      4 NORBERT       *   FILE 950
//*       NOT         01.01   2017/01/05 09:23     23 NORBERT       *   FILE 950
//*       ODER        01.02   2017/01/05 09:23     27 NORBERT       *   FILE 950
//*       ONLY        01.01   2017/01/05 09:23     25 NORBERT       *   FILE 950
//*       PACKCHG     01.14   2017/01/05 09:23    334 NORBERT       *   FILE 950
//*       PACKCHG1    01.19   2017/01/05 09:23    227 NORBERT       *   FILE 950
//*       PACKCHG2    01.13   2017/01/05 09:23     57 NORBERT       *   FILE 950
//*       PACKCHG3    01.12   2017/01/05 09:23     62 NORBERT       *   FILE 950
//*       SAVE        01.03   2017/01/05 09:23    226 NORBERT       *   FILE 950
//*       SAVEP       01.00   2016/10/07 00:31     43 NORBERT       *   FILE 950
//*       SETLAB      01.01   2017/01/05 09:23     96 NORBERT       *   FILE 950
//*       WHOHOLDS    01.03   2017/01/05 09:23     36 NORBERT       *   FILE 950
//*       XDOUBLE     01.03   2017/01/05 09:23    162 NORBERT       *   FILE 950
//*       XMAN        01.04   2017/01/05 09:23    168 NORBERT       *   FILE 950
//*       XMANP       01.02   2017/01/05 09:23     50 NORBERT       *   FILE 950
//*                                                                 *   FILE 950
```
