### Esperanta-wikimedia-tekstaro
Teksta analizo de Esperanto Wikimedia artikularo, konvertigita al texta dosiero.


### Elsxuti vikimedian esperantan (xmldump) dosieron.

### Forvisxi XML etikedojn

for f in `find . -type f -name 'wiki_*'`; do
	echo "Dosiero: $f"
	sed -i 's/<[^>]*>//g' $f
done


### Kunmeti apartajn dosierojn en unu grandan tekstan dosieron

for f in `find . -type f -name 'wiki_*'`; do
	cat $f >> bigfile



	
