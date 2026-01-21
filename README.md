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


## Evaluacija rezultata

Projekt je uspješno demonstrirao end-to-end NLP pipeline na malom, ali tematski konzistentnom korpusu od 15 TED Talkova. Ključni pokazatelji uspješnosti:

- **ASR kvaliteta (WER)**  
  Prosječni Word Error Rate (WER) iznosi **5,7%** (raspon 2,0%–13,6%).  
  Najbolji rezultati postignuti su na govorima s jasnim, sporijim govorom (npr. Robert Waldinger: 2,04%, Rhaina Cohen: 2,68%).  
  Najveći WER zabilježen je kod govora s brzim tempom i emocionalnim izražavanjem (npr. Stephanie Yates-Anyabwile: 13,64%).  
  Najčešće greške: supstitucije ("ok" → "okay"), insertions/deletions malih riječi i propuštanje markera ([laughter], [applause]).

- **Stabilnost viših razina obrade**  
  Unatoč prisutnosti ASR grešaka, metode **word embeddings** i **topic modeling** ostale su robusne:  
  - Semantičke sličnosti (GloVe finetuning) pokazale su očekivane veze (npr. "love" ↔ "life", "dream", "feel"; "relationship" ↔ "friendship", "marriage").  
  - LDA (5 tema) jasno je izdvojio glavne motive korpusa: romantična ljubav, depresija i ranjivost, stres i povezanost, moć tijela, smisao života.

- **Ograničenja evaluacije**  
  - Nije provedena usporedba ASR vs. službenih transkripata na razini sažetaka (ROUGE score) ili embeddingsa (cosine similarity).  
  - Korpus je mali (15 govora), što ograničava generalizaciju rezultata.

**Zaključak evaluacije**  
Unatoč tipičnim ASR greškama (prosječno ~6%), više razine analize (embeddings i teme) ostale su semantički stabilne i interpretabilne. Ovo potvrđuje da **moderne NLP metode mogu uspješno obraditi govoreni sadržaj čak i s nesavršenim transkriptima**.

**Sljedeći koraci za evaluaciju**  
- Izračun ROUGE scorea za TextRank sažetke (ASR vs. official).  
- Usporedba embeddingsa i tema između ASR i službenih transkripata.  
- Proširenje korpusa na 50+ govora za robusnije rezultate.


## Struktura repozitorija
- `official_transcripts_not_cleaned/` – službeni transkripti izvučeni sa TED stranice, potrebno ih je u jednom trenu ubaciti u Google Collab ako planiramo izvoditi kod
- `End_to_End_NLP_analiza_TED_Talkova.ipynb` – Jupyter bilježnica
- `ted_urls.txt` - popis linkova na odabrane TED Talkove
- `README.md` – opis projekta

Projekt je implementiran u jednoj Jupyter bilježnici koja sadrži cjelokupan kod popraćen komentarima i opisima.
