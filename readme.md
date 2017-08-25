# UBL

UBL is a "format" for ASCII and UTF8 files where control codes are
used to encode hierarchical grouping inside the text.

To start a grouping, the following is written to the stream:

```
0x1D GROUP SEPARATOR
---- Any number of characters that will become the title
0x0A LINE FEED
```

To end a grouping, the following is written to the stream:

```
0x1D GROUP SEPARATOR
0x18 CANCEL
---- Any number of characters that will become the "status code"
0x0A LINE FEED
```


