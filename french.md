# Setup son

## 1. Télécharger les cables virtuels et Voicemeeter

- **CABLE** > https://vb-audio.com/Cable/index.htm
- **CABLE A** et le **CABLE B** > https://vb-audio.com/Cable/index.htm#DownloadCable
- **Voicemeeter Banana** > https://vb-audio.com/Voicemeeter/banana.htm

## 2. Installer les cables un par un et redémarrer après chaque installation

Note: Exécuter en tant qu'administrateur chaque `.exe`

## 3. Ouvrir l'interface de réglage des sons de windows

`Win` + `R` puis `mmsys.cpl sound` (ou dans un fichier raccourci)

> Onglet **Playback**
- Mettre `VoiceMeeter Input` en **Default Device**

> Onglet **Recording**

- Mettre `VoiceMeeter Output` en **Default Device**
- `CABLE Output` > **Properties** > onglet **Listen** 
  - cocher la case *Listen to this device* et sélectionner `VoiceMeeter Input` dans la liste déroulante en dessous

## 4. Configurer VoiceMeeter

> En haut à gauche

- Cliquer sur **Hardware Input 1** et sélectionner *WDM: CABLE-A Output (...)*
- Dessous, n'avoir que le bouton **A1** d'activé
- Cliquer sur **Hardware Input 2** et sélectionner *WDM: CABLE-B Output (...)*
- Dessous, n'avoir que le bouton **A1** d'activé

> Au milieu

- Dans la colonne **Virtual Inputs** Désactiver toutes les sorties sauf **A1**

> En haut à droite

- Cliquer sur **A1** et sélectionner *WDM: Speakers (...)* ou le périphérique de sortie souhaité (casque, HP, etc.)

Sauvegarder la configuration **Menu** > *Save Settings*

## 5. Configurer l'audio de StreamlabsOBS / OBS Studio

Ouvrir les **Settings**, puis afficher la page **Audio**

- **Desktop Audio Device 1** > *CABLE Input (...)*
- **Desktop Audio Device 2** > *VoiceMeeter Input (...)*
- **Mic/Auxiliary Device 1** > *CABLE-A Output (...)*
- **Mic/Auxiliary Device 2** > *CABLE-B Output (...)*
- **Mic/Auxiliary Device 3** > *Microphone (...)*

Dans la page **Advanced**
- *Audio* > *Audio Monitoring Device* > VoiceMeeter Input


## 6. Configurer le mixeur audio de Windows

`Win` + `R` puis `ms-settings:apps-volume` (ou dans un fichier raccourci)

- Master Output > *VoiceMeeter Input (...)*
- obs64.exe > *VoiceMeeter Aux Input (...)*
- Game > *CABLE-A Input (...)*
- Music app > *CABLE-B Input (...)*
- Discord > *CABLE Input (...)*

## 7. Désactiver certaines sources audio pour les VODs

- Télécharger et installer Twitch Soundtrack > https://www.twitch.tv/broadcast/soundtrack
- fermer slobs
- installer soundtrack
- activer l'installation du plugin pour slobs
- lancer slobs
- ajouter la source **Soundtrack Source** à toutes les scènes
- dans **Advanced Audio Settings** désactiver la piste 6 pour les sources non désirées sur les VODs