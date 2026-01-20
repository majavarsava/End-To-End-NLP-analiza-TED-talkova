# End-to-End NLP analiza TED Talkova

## Opis projekta
Cilj projekta je izgradnja i analiza end-to-end sustava za obradu govorenog sadržaja primjenom metoda NLP-a, pri čemu se polazi od audio zapisa TED Talkova te se postupno provodi automatska transkripcija govora i višeslojna analiza dobivenog teksta. Projekt se fokusira na TED Talkove iz područja psihologije i međuljudskih odnosa (npr. ljubav, privrženost, emocionalne veze), koji predstavljaju semantički bogat i tematski konzistentan skup govornog materijala.
Analiza obuhvaća pretvorbu govora u tekst, normalizaciju i lingvističku obradu transkripata, automatsko sažimanje sadržaja te otkrivanje tematske strukture govora. Poseban naglasak stavlja se na usporedbu rezultata dobivenih na temelju automatski generiranih transkripata i službenih TED transkripata, kako bi se analizirao utjecaj pogrešaka automatskog prepoznavanja govora na daljnje NLP zadatke.  


## Skup podataka (15 ted talkova):
- TED službena web stranica – odabrani audio zapisi
- Službeni TED transkripti s TED stranice
- Whisper ASR transkripti


## Korištene tehnike
1. Automatic Speech Recognition (Whisper)
2. Osnovna obrada teksta i POS tagging
3. Named Entity Recognition
4. Ekstraktivno sažimanje teksta (TextRank)
5. Topic modelling i word embeddings

## Ulazi i izlazi
**Ulaz:** audio zapisi (.mp3/.wav)  
**Izlaz:** transkripti, sažeci, tematske distribucije, vizualizacije


## Očekivani rezultati:
Očekuje se da će projekt pokazati kako je moguće izgraditi end-to-end NLP sustav za analizu govorenog sadržaja te kako kvaliteta automatske transkripcije utječe na rezultate sažimanja i tematske analize. Rezultati će pružiti uvid u dominantne teme i jezične obrasce u TED Talkovima iz područja psihologije i međuljudskih odnosa, kao i u ograničenja i prednosti primjene NLP metoda na automatski generirane transkripte govora.


## Evaluacija
Usporedba ASR i službenih transkripata te analiza utjecaja ASR pogrešaka
na daljnje NLP zadatke.


## Struktura repozitorija
- `official_transcripts_not_cleaned/` – službeni transkripti izvučeni sa TED stranice, potrebno ih je u jednom trenu ubaciti u Google Collab ako planiramo izvoditi kod
- `End_to_End_NLP_analiza_TED_Talkova.ipynb` – Jupyter bilježnica
- `ted_urls.txt` - popis linkova na odabrane TED Talkove
- `README.md` – opis projekta

Projekt je implementiran u jednoj Jupyter bilježnici koja sadrži cjelokupan kod popraćen komentarima i opisima.
