# Text-Classification
This project will describe about the Binary Text Classification of Email data with the help of NLP 
And Noun Phrase Extraction from a sentence.
# 1. Noune_Phrase.ipynb: 
This file contailns the python code for the Noun phrase extraction.
# 1.1 Tokenization:
Tokenize the sentence using 'nltk.word_tokenize(x)' and give is POS(part of speech) tagging using 'nltk.pos_tag(nltk.word_tokenize(x))'
# 1.2 Writting Grammar:
Grammar for the selecting the words from the tokenized sentence that give the nuon phrase.\
grammar = r'''\
    NP: {<DT>?<JJ|JJS>*<NN|NNS>}
        
    '''
# 1.3 Chunk parser:
Create the chunk parser using the above grammar and the make a tree.\\
cp=nltk.RegexpParser(grammar)\
tree = cp.parse(tokens)

# 1.4 Selecting the Subtree:
Finally select the subtree of the generated tree.
