# Europarl-Speaker-Information
Europarl parallel corpora with per sentence speaker annotations for 22 language pairs.

The need for more personalized Machine Translation (MT) is highlighted in Mirkin et al. (2015). Nevertheless, research on personalized NMT remains scarce. One of the main challenges for more personalized MT systems is finding large enough annotated parallel datasets. Rabinovich et al. (2017) published an annotated parallel dataset for EN-FR and EN-DE, however, for many other language pairs no sufficiently large annotated datasets are available.

To address the aforementioned problem, we compiled a collection of parallel corpora for 20 language pairs. We annotated parallel sentences from Europarl (Koehn, 2005) with speaker information (name, gender, age, date of birth, euroID and date of the session) based on monolingual Europarl source files which contain speaker names on the paragraph level. We used meta-information of the members of the European Parliament (MEPs) released by Rabinovich et al. (2017) (which includes a.o. name, country, date of birth and gender predictions per MEP) to retrieve the demographic annotations. An example of the annotations used:

An overview of the language pairs as well as the number of annotated parallel sentences we retrieved per language pair is given in table below:

    EN-BG:		306.380
    EN-CS:		491.848
    EN-DA:	        1.421.197
    EN-DE:  	1.296.843
    EN-EL:		921.540
    EN-ES:		1.419.507
    EN-ET:		494.645
    EN-FI: 	        1.393.572
    EN-FR:		1.440.620
    EN-HU:		251.833
    EN-IT:		1.297.635
    EN-LT:		477.358 
    EN-LV:		487.287	
    EN-NL:		1.419.359  
    EN-PL:		478.008  
    EN-PT:		1.426.043	  
    EN-RO:		303.396	
    EN-SK:		488.351  
    EN-SL:		479.313	
    EN-SV:		1.349.472	
    EN-LT:		477.358	
    EN-LV:		487.287	

The data is provided in zip files per language. Every zip file contains 3 files:
 
  [1] SOURCE.source-target.txt: 
  Tokenized source data 
      
      Example:
        Is the Commission taking the initiative going to be a question of weeks or a question of months ?
        I fully support this report and welcome its adoption by this Parliament .

  [2] TARGET.source-target.txt: 
  Tokenized parallel target data
      
      Example:
        Est-ce une question de semaines ou de mois ?
        Je soutiens pleinement ce rapport et je me réjouis de son adoption par ce Parlement .

  [3] Tags.source-target.txt:
  Tags corresponding to the SOURCE and TARGET sentences providing information about the speaker, i.e. name, date of birth, date of the session, age of the speaker.
      
      Example:
        <LINECOUNT="5" EUROID="28257" NAME="ivo belet" LANGUAGE="UNK" GENDER="MALE" DATE_OF_BIRTH="1959-6-7" SESSION_DATE="11-02-15" AGE="52"/>
        <LINECOUNT="6" EUROID="1289" NAME="proinsias de rossa" LANGUAGE="UNK" GENDER="MALE" DATE_OF_BIRTH="1940-5-15" SESSION_DATE="04-03-11" AGE="64"/>

If you use our dataset, please cite:
        
    Eva Vanmassenhove and Christian Hardmeier, 2018. Europarl Datasets with Demographic Speaker Information. European      Association for Machine Translation (EAMT), May 28-30, Alicante, Spain [accepted].

References:
        
        Ella Rabinovich, Shachar Mirkin, Raj Nath Patel, Lucia Specia and Shuly Wintner, 2017. Personalized Machine Translation: Preserving Original Author Traits. Proceedings of the 15th Conference of the European Chapter of the Association for Computational Linguistics (EACL 2017), April 3-7, Valencia, Spain, 1074--1084.

        Philipp Koehn, 2005. Europarl: A parallel corpus for statistical machine translation. Proceedings of the In MT Summit, Phuket, September 12-16, Thailand, 79--86. 

        Shachar Mirkin, Scott Nowson, Caroline Brun and Julien Perez, 2015. Motivating personality-aware machine translation. In Proceedings of the 2015 Conference on Empirical Methods in Natural Language Processing, September 17-21, Lisbon, Portugal, 1102--1108.


