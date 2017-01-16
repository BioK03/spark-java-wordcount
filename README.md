<img src="http://spark.apache.org/images/spark-logo-trademark.png" alt="Spark Logo" height="200"/>

# spark-java-wordcount

This repo is an example of Spark pairing keys over a text file.

The goal of this is to count words from a poem using a Map - Pair - Reduce operation.

## Input file

The poeme.txt is a 2978 line-long file separated into sections. It represents a foreign poem translated into French.

## Execute the project
With spark and hadoop installed, you must put the file on the hadoop disk :

`hadoop fs -put poeme.txt /test`

Next, after having compiled the project (with Maven for example : `mvn clean package`), you will execute the project :

`hadoop jar NameOfYourJar.jar WordCount /test/poeme.txt /results`

You can see the results using <img src="http://gethue.com/wp-content/uploads/2014/03/hue_logo_300dpi_huge.png" height="15"/> (Hue) for example.

## Raw results

Here is a sample of the results :
```
(sentinelles,1)
(souvent,8)
(Elles,1)
(prairies;,1)
(Soulevait,1)
(soupir,3)
(épais,5)
(filet,2)
(derniers,3)
(Bassin,2)
(collines;,1)
(ridé,1)
(Pauvre,1)
(lumière,5)
(nom,6)
(Viennent,2)
(saisie,1)
(guider,2)
(fuir,4)
(L'homme,1)
(tranquilles,1)
(distrait,1)
(demeure;,1)
(gentille:,1)
(s'endormir,1)
(Prétendait,1)
```
It details, for each word, the number of occurence in the poem.
