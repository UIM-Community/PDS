# PDS
Nimsoft (CA UIM) Portable Data Stream

Nimsoft uses the proprietary Portable Data Stream (PDS) format as a way to represent data across the network. In general, a PDS formatted message contains a stream of data, tagged by descriptive labels. You may extract the data in a sequential manner, or get the data using the tags. The Nimsoft API offers several functions to read from or write to a PDS. The general idea is to store name, type and value information into the data stream on one end, and to extract the data on the other end of a network communication channel. The Nimsoft API will automatically translate the data in the stream to the correct format for that platform.

The Portable Data Stream (PDS) library contains a set of functions meant to manipulate machine independent
data represented by the PDS object. This object may in turn be used, for instance, to send network independent
information from client to server. The data stream built by PDS is an ASCII stream containing elements built
using the following format:

| KEY_NAME | PDS_TYPE | DATA_SIZE | DATA |
| --- | --- | --- | --- |

## Available PDS Types

| TYPE | CODE | DESCRIPTION |
| --- | --- | --- |
| PDS_I | 1 | Integer |
| PDS_PI | 2 | Integer pointer |
| PDS_PPI | 3 | Pointer to an integer pointer, commonly used for intergers array |
| PDS_RGI | 4 | Pointer to an existing integer |
| PDS_RGPI | 5 | Pointer to an integer array |
| PDS_CH | 6 | Character |
| PDS_PCH | 7 | NUL terminated string (C String) |
| PDS_PPCH | 8 | Pointer to a NUL terminated string (C String) |
| PDS_RGCH | 9 | Pointer to a character buffer |
| PDS_RGPCH | 10 | Pointer to a character array buffer |
| PDS_F | 11 | Floating point number |
| PDS_PF | 12 | Pointer to a floating point number |
| PDS_PPF | 13 | Pointer to a floating point number pointer |
| PDS_RGF | 14 | Pointer to a floating point number |
| PDS_RGPF | 15 | Pointer to a floating point number array |
| PDS_PDS | 16 | PDS |
| PDS_VOID | 17 | Raw byte data |
| PDS_SEP | 18 | No data |
| PDS_PPDS | 19 | Pointer to a PDS |
| PDS_CPCH | 20 | N/A |
| PDS_CPDS | 21 | N/A |
| PDS_INT64 | 22 | Integer on 64 bit (BigINT) |

## PDS Errors
