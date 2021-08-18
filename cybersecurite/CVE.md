# CVE 

## Définition
Common Vulnerabilities and Exposures ou CVE est un dictionnaire publiques relatives aux vulnérabilités de sécurité. Les CVE aident les professionnels à coordonner leurs efforts visant à hiérarchiser et résoudre les vulnérabilités, et ainsi renforcer la sécurité des systèmes informatiques.

Les identifiants CVE sont des références de la forme CVE-AAAA-NNNN (AAAA est l'année de publication et NNNN un numéro d'identifiant). 
Par exemple, la faille FREAK a pour identifiant CVE-2015-0204. 

## Critères d'attribution d'un identifiant CVE


Les identifiants CVE sont attribués aux failles qui répondent à un ensemble de critères spécifiques :

   **1. Possibilité de correction indépendante**
    
    Chaque faille doit pouvoir être corrigée indépendamment de tout autre bogue.

   **2. Reconnaissance par le fournisseur concerné OU documentation**
    
    L'éditeur de logiciel ou le fabricant de matériel doit reconnaître le bogue et son effet négatif sur la sécurité. 
    Ou, la personne qui a signalé le bogue doit partager un rapport de vulnérabilité qui permet de démontrer que le bogue 
    a un effet négatif ET qu'il enfreint la politique de sécurité du système touché.

   **3. Impact sur un code base**
    
    Les failles qui touchent plus d'un produit doivent recevoir différents identifiants CVE. 
    Dans le cas de bibliothèques, protocoles ou normes partagés, la faille reçoit un seul identifiant CVE uniquement s'il
    n'existe aucun moyen d'utiliser le code partagé sans être affecté par la vulnérabilité. Dans le cas contraire, 
    chaque code base ou produit affecté obtient un identifiant CVE unique.


## Présentation d'un CVE 

Dans le cadre de mon alternance, en entreprise, j'ai dû faire face à une vulnérabilité sur un CMS que nous utilisions : Magento. Le CVE CERTFR-2021-AVI-609 mettait en lumière les risques de sécurités
sur une version de Magento que nous utilisions. Ces risques sont:

*  Exécution de code arbitraire à distance
*  Déni de service à distance
*  Contournement de la politique de sécurité
*  Élévation de privilèges

## Source

SOURCE DEFINITION : 

https://fr.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures

https://www.redhat.com/fr/topics/security/what-is-cve

SOURCE CVE:

https://www.cert.ssi.gouv.fr/avis/CERTFR-2021-AVI-609/


