### Esperanta-wikimedia-tekstaro
Teksta analizo de Esperanto Wikimedia artikularo, konvertigita al texta dosiero.


### Elsxuti krudan vikimedian esperantan (xmldump) dosieron.
De gxenerala retejo https://dumps.wikimedia.org/ kaj elsxulti https://dumps.wikimedia.org/eowiki/latest/eowiki-latest-pages-articles.xml.bz2  

#### Malkompaktigi la dosieron xml
`bunzip2 eowiki-latest-pages-articles.xml.bz2`

#### Eltiri apartajn artikolojn el la dosieron xml.
Mi uzis la ilon https://github.com/attardi/wikiextractor

`git clone https://github.com/attardi/wikiextractor  `
`mkdir text`  
`./wikiextractor/WikiExtractor.py  eowiki-latest-pages-articles.xml text`  

### Forvisxi XML etikedojn
`for f in `find . -type f -name 'wiki_*'`; do`  
`	echo "Dosiero: $f"`  
`	sed -i 's/<[^>]*>//g' $f`  
`done`  

### Kunmeti apartajn dosierojn en unu grandan tekstan dosieron
`for f in `find . -type f -name 'wiki_*'`; do`  
`	cat $f >> bigfile`  



	
