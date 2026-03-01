# Analyse-statique-d-un-APK-avec-JADX-GUI-dex2jar-JD-GUI
<img width="1579" height="1033" alt="image" src="https://github.com/user-attachments/assets/b789b61a-0f08-4438-a87d-c2a1df5f8ab8" />
<img width="1900" height="416" alt="image" src="https://github.com/user-attachments/assets/fdcc1320-de87-43a5-b152-2c857569b801" />
Task 3 — Analyse avec JADX GUI
<img width="1414" height="739" alt="image" src="https://github.com/user-attachments/assets/4970a956-21f9-4609-96f3-f99cc232b68c" />
<img width="1405" height="724" alt="image" src="https://github.com/user-attachments/assets/13ff9726-85f3-4988-b9eb-84785431a71b" />
<img width="504" height="727" alt="image" src="https://github.com/user-attachments/assets/56e63766-97f3-4cf4-ab58-006df1f55bb1" />


 Task 4 — Recherche de chaînes sensibles
<img width="1257" height="709" alt="image" src="https://github.com/user-attachments/assets/e085c879-4134-446e-b864-6290f6866590" />
<img width="1257" height="788" alt="image" src="https://github.com/user-attachments/assets/12dfd9f6-a57e-4f05-9505-f40bf754d9d2" />
<img width="1253" height="419" alt="image" src="https://github.com/user-attachments/assets/aa71efcb-c0e0-41bf-81fa-35d12c9512a2" />
Task 5 — Convertir DEX → JAR avec dex2jar
<img width="1261" height="269" alt="image" src="https://github.com/user-attachments/assets/cb858216-4978-4e05-b03b-db9b8af689b0" />
<img width="963" height="247" alt="image" src="https://github.com/user-attachments/assets/a8731f0a-2943-4740-a381-0ab447acc20b" />
<img width="1198" height="476" alt="image" src="https://github.com/user-attachments/assets/64efeaf7-6d2e-440d-9fb1-67d6ca7ad37e" />
convertir dex to jar :
<img width="628" height="86" alt="image" src="https://github.com/user-attachments/assets/0888f119-4164-4438-a768-be0d10deeabe" />

Task 6 — Comparaison JADX vs JD-GUI
<img width="191" height="307" alt="image" src="https://github.com/user-attachments/assets/2536c0a8-7ccd-4b91-85da-d2b61ee15cdd" />
comparaison de class a
<img width="629" height="239" alt="image" src="https://github.com/user-attachments/assets/4c9a26b7-c2aa-432e-b05f-b50642ed1400" />
class b
<img width="628" height="241" alt="image" src="https://github.com/user-attachments/assets/03c31c24-17c7-43a4-a661-15165667e3c7" />
class c
<img width="626" height="287" alt="image" src="https://github.com/user-attachments/assets/fb152fda-ea4a-495c-85ae-f3dde9438d96" />
| **Aspect** | **JADX GUI** | **JD-GUI** | | ------------------------------ | -------------------------------------------------------------------- | ------------------------------------------------- | | **Type de fichiers supportés** | Ouvre directement les fichiers `.apk`, `.dex`, `.aar` | Ouvre uniquement des fichiers `.jar` | | **Structure affichée** | Affiche AndroidManifest, ressources (res/), assets, code Java/Kotlin | Affiche seulement les packages et classes Java | | **Compatibilité Android** | Conçu spécialement pour Android | Conçu pour applications Java classiques | | **Gestion du Kotlin** | Bonne reconstruction du code Kotlin | Difficulté à reconstruire correctement le Kotlin | | **Navigation** | Recherche globale (code + ressources) | Recherche limitée au code Java | | **Obfuscation** | Tente de rendre le code plus lisible | Conserve souvent les noms obfusqués | | **Interface moderne** | Interface plus récente et adaptée au reverse Android | Interface plus ancienne et minimaliste | | **Analyse rapide APK** | Permet analyse directe sans conversion | Nécessite conversion DEX → JAR (ex : via dex2jar) | Task 7 — Rédiger le mini-rapport [Uploading rapor Rapport d’analyse statique – UnCrackable-Level1
Informations générales • Date d’analyse : 01/03/2026 • Analyste : Anas Elmahfoudy & Ghalbane Ziad • APK analysé : UnCrackable-Level1.apk • Version : Version fournie par l’enseignant • Provenance : Fournie par notre enseignant (TP Sécurité Mobile) • Outils utilisés : o JADX 1.5.5 o dex2jar v2.4 o JD-GUI 1.6.6

Résumé exécutif Une analyse statique complète de l’application UnCrackable-Level1.apk a été réalisée à l’aide d’outils de décompilation Android. L’analyse n’a révélé aucune vulnérabilité critique directe, telle que : • clés API en clair • mots de passe codés en dur • composants exportés non protégés • permissions excessives L’application semble volontairement conçue comme un challenge de sécurité (reverse engineering), mais aucune faille de sécurité exploitable évidente n’a été identifiée dans l’analyse statique. Niveau de risque global : Faible à Moyen Actions recommandées :

Continuer l’analyse dynamique pour confirmer l’absence de vulnérabilités
Vérifier l’implémentation des mécanismes anti-debug
Tester l’application sur un environnement rooté pour analyse approfondie
Constats détaillés Constat #1 : Absence de secrets en clair Sévérité : Faible Description : Aucune clé API, mot de passe ou token sensible n’a été trouvé en clair dans le code décompilé. Localisation : Analyse globale du code via JADX GUI. Impact potentiel : Aucun risque immédiat lié à l’exposition de secrets. Remédiation recommandée : Maintenir cette bonne pratique en externalisant les secrets côté serveur.

Constat #2 : Pas de composants Android exposés inutilement Sévérité : Faible Description : L’analyse du fichier AndroidManifest.xml n’a pas révélé de composants (Activity, Service, Receiver) marqués comme exported="true" sans justification. Localisation : AndroidManifest.xml via JADX GUI. Impact potentiel : Risque faible d’attaque inter-application. Remédiation recommandée : Continuer à restreindre les composants exposés.

Constat #3 : Présence de mécanismes anti-debug / protection Sévérité : Moyenne Description : L’application semble contenir des mécanismes visant à empêcher l’analyse ou la modification (challenge pédagogique). Localisation : Code principal analysé avec JADX. Impact potentiel : Comportement intentionnel dans le cadre d’un challenge de sécurité. Remédiation recommandée : Aucune – comportement cohérent avec un exercice pédagogique.

Annexes Permissions demandées • android.permission.INTERNET (Ajuste selon ce que tu as réellement vu dans ton Manifest.) Composants exportés Aucun composant critique exposé sans protection identifié.

Rapport d’analyse statique – UnCrackable-Level1

Informations générales • Date d’analyse : 01/03/2026 • Analyste : Anas Elmahfoudy & Ghalbane Ziad • APK analysé : UnCrackable-Level1.apk • Version : Version fournie par l’enseignant • Provenance : Fournie par notre enseignant (TP Sécurité Mobile) • Outils utilisés : o JADX 1.5.5 o dex2jar v2.4 o JD-GUI 1.6.6

Résumé exécutif Une analyse statique complète de l’application UnCrackable-Level1.apk a été réalisée à l’aide d’outils de décompilation Android. L’analyse n’a révélé aucune vulnérabilité critique directe, telle que : • clés API en clair • mots de passe codés en dur • composants exportés non protégés • permissions excessives L’application semble volontairement conçue comme un challenge de sécurité (reverse engineering), mais aucune faille de sécurité exploitable évidente n’a été identifiée dans l’analyse statique. Niveau de risque global : Faible à Moyen Actions recommandées :

Continuer l’analyse dynamique pour confirmer l’absence de vulnérabilités
Vérifier l’implémentation des mécanismes anti-debug
Tester l’application sur un environnement rooté pour analyse approfondie
Constats détaillés Constat #1 : Absence de secrets en clair Sévérité : Faible Description : Aucune clé API, mot de passe ou token sensible n’a été trouvé en clair dans le code décompilé. Localisation : Analyse globale du code via JADX GUI. Impact potentiel : Aucun risque immédiat lié à l’exposition de secrets. Remédiation recommandée : Maintenir cette bonne pratique en externalisant les secrets côté serveur.

Constat #2 : Pas de composants Android exposés inutilement Sévérité : Faible Description : L’analyse du fichier AndroidManifest.xml n’a pas révélé de composants (Activity, Service, Receiver) marqués comme exported="true" sans justification. Localisation : AndroidManifest.xml via JADX GUI. Impact potentiel : Risque faible d’attaque inter-application. Remédiation recommandée : Continuer à restreindre les composants exposés.

Constat #3 : Présence de mécanismes anti-debug / protection Sévérité : Moyenne Description : L’application semble contenir des mécanismes visant à empêcher l’analyse ou la modification (challenge pédagogique). Localisation : Code principal analysé avec JADX. Impact potentiel : Comportement intentionnel dans le cadre d’un challenge de sécurité. Remédiation recommandée : Aucune – comportement cohérent avec un exercice pédagogique.

Annexes Permissions demandées • android.permission.INTERNET (Ajuste selon ce que tu as réellement vu dans ton Manifest.) Composants exportés Aucun composant critique exposé sans protection identifié. t.md…]()
Task 8 — Nettoyage
<img width="557" height="46" alt="image" src="https://github.com/user-attachments/assets/aa1583ef-2598-41a7-9577-87fd30772ea3" />




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
