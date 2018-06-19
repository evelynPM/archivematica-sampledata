## Variously configured files to test handling of file format extensions

The files in these folders are designed to test various different format
identification tools' (and the format policy register's) ability to look at
files with only a file-format-extension as its primary signature. Files
should have an extension known to PRONOM, e.g. `.jpg`, `.bin`, `.class` but
should not contain characteristics that would identify the file via any
signature-based method available to the tool. Two folders are set-up with a
limited number of samples.

### empty_files_with_extensions

To test extension-only identification and not risk identification via a format
identification tool's binary matching techniques, these files are devoid of
any content. Their file-sizes should be zero. They will also be free from
various byte-order-markings used in Unicode-like formats such as UTF-8.

### text_files_with_extensions

To test extension-only identification and not risk files being treated
differently for being zero-bytes in size, these objects all contain text. The
text used will mostly be encoded using the ASCII character-encoding and will
simply be the format's extension. As an example, if the sample file is a
`.pyc` file, the text inside the file will be `pyc`.
