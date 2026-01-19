# End-to-End NLP analiza TED Talkova

## Opis projekta
Projekt demonstrira izgradnju end-to-end NLP sustava za analizu govorenog sadržaja
na primjeru TED Talkova iz područja psihologije i međuljudskih odnosa.

## Skup podataka
- TED Talks (audio zapisi)
- Službeni TED transkripti
- Whisper ASR transkripti

## Korištene tehnike
- Automatic Speech Recognition (Whisper)
- Normalizacija i POS tagging
- Named Entity Recognition
- Ekstraktivno sažimanje (TextRank)
- Topic modeling (LDA)

## Ulazi i izlazi
**Ulaz:** audio zapisi (.mp3/.wav)  
**Izlaz:** transkripti, sažeci, tematske distribucije, vizualizacije

## Evaluacija
Usporedba ASR i službenih transkripata te analiza utjecaja ASR pogrešaka
na daljnje NLP zadatke.
