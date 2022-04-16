---
title: "Supported Encodings"
---
This lists the currently supported encodings of [liblcf](https://github.com/EasyRPG/liblcf/blob/master/src/reader_util.cpp).

| Human readable name | Mapping table (ICU)        | Codepage (iconv) |
|---------------------|----------------------------|------------------|
| Japanese            | ibm-943_P15A-2003          | 932              |
| Korean              | windows-949-2000           | 949              |
| :::                 | (needs ibm-1363_P11B-1998) |                  |
| Central Europe      | ibm-5346_P100-1998         | 1250             |
| Cyrillic [^1]       | ibm-5347_P100-1998         | 1251             |
| Occidental [^1]     | ibm-5348_P100-1997         | 1252             |
| Greek [^1]          | ibm-5349_P100-1998         | 1253             |
| Hebrew [^1]         | ibm-9447_P100-2002         | 1255             |
| Arabic [^1] [^2]    | ibm-9448_X100-2005         | 1256             |
| Thai [^1]           | windows-874-2000           | 874              |
| Chinese simplified  | windows-936-2000           | 936              |
| :::                 | (needs ibm-1386_P100-2001) |                  |
| Chinese traditional | windows-950-2000           | 950              |
| :::                 | (needs ibm-1373_P100-2002) |                  |
| Turkish             | ibm-5350_P100-1998         | 1254             |
| Baltic              | ibm-9449_P100-2002         | 1257             |

[^1]: with Euro

[^2]: \+ 8 chars
