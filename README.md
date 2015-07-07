# TheHokeApplication 
-or- 
#cine[] 

##text-to-image interpolation

###brief: 

The software takes as an input a text from a given author. The script evaluates the text for it's essential elements, starting with a measure of the most basic elements (words, sentences, line-breaks). Based on the measure of the author's writing the script will create a score which will be used to place the elements of content in sequence. These elements will be evaluated by a search engine, using the parsed metadata gathered from the content of the writing. The search engine will provide us with relative images for the sequence. These images will be output into a piece with a given duration according to the score.

###elements/processes:

1. Text parser

    Paragraphs, words per paragraph, eliminate white space, quotations, proper nouns

2.  Evaluate count (ratio of parsed elements to the whole)

    paragraph-to-whole
    quotations-to-whole - quotations are specialized paragraphs and receive added value

3. Metadata per paragraph

    Propername acts (does something)
    Quotations gain speaker and listener attributes
    All articles removed
    Duplicated terms removed but attribute value to that term; terms with highest value ordered first in metadata

4. Search

    Search engine customized to default to images
    Metadata evaluated by search engine

5. Evaluation

    If null result, metadata is minimized by reducing terms starting with the least valuable. If there are multiple terms of similar least values, terms are eliminated either randomly or through a function whereby the unique terms are given precedent over those occurring in prior paragraphs
    If given a set of results, we determine which image can be chosen either randomly or based on top result not already used

6. Output

    Images are placed on a timeline/sequence
    Time line plays images for a period based on their relative values (see item 2)
    Audio (TBD)
