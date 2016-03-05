=== Data Source ===

There are a lot of files in: `https://dumps.wikimedia.org/eswiki/latest/`. They are described in `https://en.wikipedia.org/wiki/Wikipedia:Database_download`. Some of them are xml and some sql. Need to consider the most appropriate for me.

The corresponding dictionary page is `https://dumps.wikimedia.org/eswiktionary/`.

There is a wikipedia Python package: `https://pypi.python.org/pypi/wikipedia`. It may give me all the functionality I need.

=== Processing Flow ===

In pseudocode:

1) Get wikipedia content
   * Format? Source?
   
2) Format each page's introduction into an anki note
   * Format of Anki notes? need intermediate representation?
   
3) Package the notes into a deck

=== General notes ===

Most page synopses start with the name of the page. That would make them useless as flashcard texts, so I need to remove that.
    * It seems that in all cases the text to remove is bolded. Convenient!

There are way too many pages even in the Spanish Wikipedia. Need to find a reasonable way to filter them. Options:
    * Internal ranking: if it exists, that'd be awesome.
    * Length of text: very rough, a little stupid, but maybe good enough.
    * PageRank: I guess this would highlight clearly the indispensale knowledge of the world. Expensive to calculate, probably. Not sure how it would behave at the margins (ie long tail), but that probably doesn't matter if I filter.