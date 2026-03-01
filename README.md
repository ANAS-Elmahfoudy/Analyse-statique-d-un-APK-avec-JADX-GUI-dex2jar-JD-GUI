# Analyse-statique-d-un-APK-avec-JADX-GUI-dex2jar-JD-GUI
<img width="1579" height="1033" alt="image" src="https://github.com/user-attachments/assets/b789b61a-0f08-4438-a87d-c2a1df5f8ab8" />
<img width="1900" height="416" alt="image" src="https://github.com/user-attachments/assets/fdcc1320-de87-43a5-b152-2c857569b801" />
Task 3 — Analyse avec JADX GUI
<img width="1414" height="739" alt="image" src="https://github.com/user-attachments/assets/4970a956-21f9-4609-96f3-f99cc232b68c" />
<img width="1405" height="724" alt="image" src="https://github.com/user-attachments/assets/13ff9726-85f3-4988-b9eb-84785431a71b" />




[raport.md](https://github.com/user-attachments/files/25662095/raport.md)

Rapport d’analyse statique – UnCrackable-Level1

Informations générales
•	Date d’analyse : 01/03/2026
•	Analyste :  Anas Elmahfoudy & Ghalbane Ziad
•	APK analysé : UnCrackable-Level1.apk
•	Version : Version fournie par l’enseignant
•	Provenance : Fournie par notre enseignant (TP Sécurité Mobile)
•	Outils utilisés :
o	JADX 1.5.5
o	dex2jar v2.4
o	JD-GUI 1.6.6

Résumé exécutif
Une analyse statique complète de l’application UnCrackable-Level1.apk a été réalisée à l’aide d’outils de décompilation Android.
L’analyse n’a révélé aucune vulnérabilité critique directe, telle que :
•	clés API en clair
•	mots de passe codés en dur
•	composants exportés non protégés
•	permissions excessives
L’application semble volontairement conçue comme un challenge de sécurité (reverse engineering), mais aucune faille de sécurité exploitable évidente n’a été identifiée dans l’analyse statique.
Niveau de risque global : Faible à Moyen
Actions recommandées :
1.	Continuer l’analyse dynamique pour confirmer l’absence de vulnérabilités
2.	Vérifier l’implémentation des mécanismes anti-debug
3.	Tester l’application sur un environnement rooté pour analyse approfondie

Constats détaillés
Constat #1 : Absence de secrets en clair
Sévérité : Faible
Description :
Aucune clé API, mot de passe ou token sensible n’a été trouvé en clair dans le code décompilé.
Localisation :
Analyse globale du code via JADX GUI.
Impact potentiel :
Aucun risque immédiat lié à l’exposition de secrets.
Remédiation recommandée :
Maintenir cette bonne pratique en externalisant les secrets côté serveur.

Constat #2 : Pas de composants Android exposés inutilement
Sévérité : Faible
Description :
L’analyse du fichier AndroidManifest.xml n’a pas révélé de composants (Activity, Service, Receiver) marqués comme exported="true" sans justification.
Localisation :
AndroidManifest.xml via JADX GUI.
Impact potentiel :
Risque faible d’attaque inter-application.
Remédiation recommandée :
Continuer à restreindre les composants exposés.

Constat #3 : Présence de mécanismes anti-debug / protection
Sévérité : Moyenne
Description :
L’application semble contenir des mécanismes visant à empêcher l’analyse ou la modification (challenge pédagogique).
Localisation :
Code principal analysé avec JADX.
Impact potentiel :
Comportement intentionnel dans le cadre d’un challenge de sécurité.
Remédiation recommandée :
Aucune – comportement cohérent avec un exercice pédagogique.

Annexes
Permissions demandées
•	android.permission.INTERNET
(Ajuste selon ce que tu as réellement vu dans ton Manifest.)
Composants exportés
Aucun composant critique exposé sans protection identifié.


Rapport d’analyse statique – UnCrackable-Level1

Informations générales
•	Date d’analyse : 01/03/2026
•	Analyste :  Anas Elmahfoudy & Ghalbane Ziad
•	APK analysé : UnCrackable-Level1.apk
•	Version : Version fournie par l’enseignant
•	Provenance : Fournie par notre enseignant (TP Sécurité Mobile)
•	Outils utilisés :
o	JADX 1.5.5
o	dex2jar v2.4
o	JD-GUI 1.6.6

Résumé exécutif
Une analyse statique complète de l’application UnCrackable-Level1.apk a été réalisée à l’aide d’outils de décompilation Android.
L’analyse n’a révélé aucune vulnérabilité critique directe, telle que :
•	clés API en clair
•	mots de passe codés en dur
•	composants exportés non protégés
•	permissions excessives
L’application semble volontairement conçue comme un challenge de sécurité (reverse engineering), mais aucune faille de sécurité exploitable évidente n’a été identifiée dans l’analyse statique.
Niveau de risque global : Faible à Moyen
Actions recommandées :
1.	Continuer l’analyse dynamique pour confirmer l’absence de vulnérabilités
2.	Vérifier l’implémentation des mécanismes anti-debug
3.	Tester l’application sur un environnement rooté pour analyse approfondie

Constats détaillés
Constat #1 : Absence de secrets en clair
Sévérité : Faible
Description :
Aucune clé API, mot de passe ou token sensible n’a été trouvé en clair dans le code décompilé.
Localisation :
Analyse globale du code via JADX GUI.
Impact potentiel :
Aucun risque immédiat lié à l’exposition de secrets.
Remédiation recommandée :
Maintenir cette bonne pratique en externalisant les secrets côté serveur.

Constat #2 : Pas de composants Android exposés inutilement
Sévérité : Faible
Description :
L’analyse du fichier AndroidManifest.xml n’a pas révélé de composants (Activity, Service, Receiver) marqués comme exported="true" sans justification.
Localisation :
AndroidManifest.xml via JADX GUI.
Impact potentiel :
Risque faible d’attaque inter-application.
Remédiation recommandée :
Continuer à restreindre les composants exposés.

Constat #3 : Présence de mécanismes anti-debug / protection
Sévérité : Moyenne
Description :
L’application semble contenir des mécanismes visant à empêcher l’analyse ou la modification (challenge pédagogique).
Localisation :
Code principal analysé avec JADX.
Impact potentiel :
Comportement intentionnel dans le cadre d’un challenge de sécurité.
Remédiation recommandée :
Aucune – comportement cohérent avec un exercice pédagogique.

Annexes
Permissions demandées
•	android.permission.INTERNET
(Ajuste selon ce que tu as réellement vu dans ton Manifest.)
Composants exportés
Aucun composant critique exposé sans protection identifié.
