# Giradischi – lettore audio per Android

Kotlin + Media3 (ExoPlayer). Funzioni: elenco brani con cartelle e ricerca, volume,
casuale/sequenziale/ripeti, riproduzione automatica, equalizzatore bassi/medi/alti,
riproduzione in background con notifica e controlli da schermo bloccato.

## Compilare con Android Studio
1. File → Open → seleziona la cartella `Giradischi`. Accetta la sincronizzazione Gradle
   (Android Studio crea da solo il Gradle wrapper).
2. Collega il telefono (debug USB) o usa un emulatore → Run per installarla.
3. Per ottenere l’APK: Build → Build Bundle(s) / APK(s) → Build APK(s).
   Il file è in `app/build/outputs/apk/debug/app-debug.apk`.

## Compilare senza Android Studio (GitHub)
1. Crea un repository su GitHub e carica tutto il contenuto di questa cartella
   (compresa la cartella nascosta `.github`).
2. Scheda Actions → "Build APK" → Run workflow.
3. A fine esecuzione scarica `Giradischi-apk` dagli Artifacts: dentro c’è `app-debug.apk`.
4. Copia l’APK sul telefono e installalo (consenti l’installazione da origini sconosciute).

## Note
- Formati: MP3, WAV, MP4/M4A, AAC, OGG, FLAC. WMA non è supportato da Android/ExoPlayer
  di serie: serve l’estensione FFmpeg di Media3 (da compilare a parte).
- Il volume regola il volume multimediale del telefono.
- I file aggiunti con "Aggiungi file" valgono per la sessione; i brani trovati nella memoria
  del telefono vengono ricaricati a ogni avvio.
