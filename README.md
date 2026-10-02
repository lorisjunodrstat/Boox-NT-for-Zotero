<img width="465" height="169" alt="boox_nt_for_zotero" src="https://github.com/user-attachments/assets/73f00249-d6cb-41e0-a9b8-84dcc198f5ab" />

# Boox NT for Zotero 📚🖋️

**Boox-NT-for-Zotero** est une version optimisée et personnalisée de l'application open source [*Zoo for Zotero*](https://github.com/mickstar/Zoo-For-Zotero). 

Elle est spécialement conçue pour les utilisateurs de liseuses Android à écran E-Ink (notamment les gammes **Onyx Boox** comme la Boox Air C, Note, Nova, etc.) utilisant un hébergement **Nextcloud / WebDAV** pour leur bibliothèque Zotero.

---

## 🌟 Fonctionnalités clés et Améliorations

### 1. 🚀 Upload résilient par morceaux (*Nextcloud Chunking API v2*)
* **Découpage en paquets (Chunks)** : Les fichiers volumineux (PDFs annotés, livres numérisés) sont découpés en petits paquets (2 à 5 Mo) lors du transfert vers Nextcloud.
* **Reprise automatique en cas de coupure Wi-Fi** : Si la connexion réseau s'interrompt lors de la mise en veille de la liseuse, la synchronisation reprend exactement là où elle s'était arrêtée sans renvoyer l'intégralité du fichier.
* **Traitement en arrière-plan via WorkManager** : Exécution sous forme de service prioritaire (*Foreground Service*) pour empêcher Android de couper le Wi-Fi pendant les transferts lourds.

### 2. 🔄 Bouton « Upload Forcé » & Gestion des copies Boox
* **Résolution des conflits de lecture** : Corrige le problème fréquent sur Onyx Boox où les applications de lecture (comme *NeoReader*) enregistrent leurs annotations sur une copie locale temporaire du fichier.
* **Bouton d'action dédié** : Permet de forcer la détection du fichier annoté le plus récent, de remplacer l'original local et de pousser immédiatement la version annotée vers votre serveur Zotero / Nextcloud.

### 3. 📝 Ajout direct de notes manuscrites
* **Export direct depuis les Notes Boox** : Importez et rattachez facilement des fichiers PDF exportés depuis l'application de notes manuscrites d'Onyx Boox vers une référence Zotero existante.
* **Prise en charge du menu « Partager » Android** : Exportez directement vos croquis et notes manuscrites vers **Boox-NT-for-Zotero** via le menu de partage Android.

---

## 🚀 Installation

1. Téléchargez le dernier fichier **`app-release.apk`** depuis la section [Releases](../../releases).
2. Transférez le fichier sur votre tablette Onyx Boox (via USB, BooxDrop ou Google Drive).
3. Activez l'installation depuis des sources inconnues dans les paramètres de votre appareil et installez l'APK.
4. Configurez vos identifiants Zotero et les paramètres d'accès à votre serveur WebDAV Nextcloud.

---

## 🛠️ Compilation à partir du code source

Si vous souhaitez compiler l'application vous-même avec **Android Studio** :

1. Clonez ce dépôt :
   ```bash
   git clone [https://github.com/lorisjunodrstat/Boox-NT-for-Zotero.git]([https://github.com/votre-nom-utilisateur/Boox-NT-for-Zotero](https://github.com/lorisjunodrstat/Boox-NT-for-Zotero.git)
