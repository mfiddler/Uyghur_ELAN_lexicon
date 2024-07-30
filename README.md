# Uyghur_ELAN_lexicon
A lexicon that can be imported into ELAN for semi-automated morphological parsing of transcribed Uyghur language data. 

# Import
If you're looking to use this lexicon, you'll probably have an .eaf file with transcription of Uyghur speech (this lexicon uses Uyghur Latin script). Open your .eaf file, then choose Options..Interlineariation Mode. In the Lexicon Actions drop-down menu, choose Import Lexicon, then select this .lift file. 

# Setup
Your transcript needs to be set up with appropriate Tier Types. Each speaker's Intonation Units (phrases/sentences) should be set up as the primary tier type. You can then add empty tiers for Words, Morphemes and Glosses. For the Word and Morphs tiers, choose Symbolic Subdivision for the "Stereotype" in the Tier Type attributes box. For Gloss, choose Symbolic Association. 

In Interlinearization Mode, go to the Configure Analyzer Settings box. Set up a Whitespace Text Analyzer that takes your Intonation Unit tiers as its source and Word tiers as its target. This will split the intonation units into individual words. Then set up a Lexicon Analyzer with Word tier as its source and Morph and Gloss tiers as its two targets. 

# Use
Once the analyzers are set up, tick the "Recursive" box at the top of the screen in Interlinearization Mode, then click "Analyze/Interlinearize". The Whitespace Analyzer will pass over the entire transcript and populate the Word tiers. Then it will go back to the first line and the Lexicon Analyzer will start parsing the words in each Intonation Unit. When it hits strings of text with more than one possible parsing, a small window will pop up and you'll need to tell it which parsing is correct. When it finishes parsing one word or Intonation Unit, you'll need to manually initiate the parsing of the next one. Right-click (or two-finger click, on a Mac) on an intonation unit in the transcript and select Analyze/Interlinearize from the menu that pops up.

If you don't finish parsing the entire transcript in one shot, save your work and come back to it later. When you come back, make sure "Recursive" is checked at the top of the screen. Then resume working through the intonation units one by one. Don't click "Analyze/Interlinearize" at the top of the screen again: this will re-do the Whitespace Analyzer over the whole transcript and start you all over.
