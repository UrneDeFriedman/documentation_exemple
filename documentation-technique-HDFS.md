## A propos
Auteur: Yanis  
Version: 1.0  
Licence: DE3 - Notre groupe  

## Technologies
- Hadoop: Hortonworks HDP Sandbox 2.6.5  
Un tutoriel est disponible à cette adresse: https://www.cloudera.com/tutorials/learning-the-ropes-of-the-hdp-sandbox.html#login-credentials  

- Python:  
&nbsp;&nbsp;&nbsp;&nbsp; 3.10 sur la machine locale  
&nbsp;&nbsp;&nbsp;&nbsp; 2.7 sur la VM Hadoop  

## Version des modules python sur la machine locale
asgiref==3.5.2  
bcrypt==3.2.2  
cffi==1.15.0  
cryptography==37.0.2  
Django==3.2.5  
paramiko==2.11.0  
pycparser==2.21  
PyNaCl==1.5.0  
pytz==2022.1  
scp==0.14.4  
six==1.16.0  
sqlparse==0.4.2  

Certains de ces modules sont des dépendances. Pour obtenir tous ces modules, voici la liste des modules à installer:  
pip install django==3.2.5  
pip install paramiko  
pip install scp  

## Commandes utiles  
- Connection en ssh:  
ssh username@localhost -p 2222  
- Envoi d'un document avec le protocole SCP de la machine locale vers la vm HDP:  
scp -P 2222 path/to/file/on/local/machine.py username@localhost:/path/to/put/file  
- Exécuter un fichier .py sur la vm:
  1) Se connecter en ssh avec la commande précédente
  2) Exécuter la commande suivante: python path/to/file.py 

- Envoyer manuellement un fichier de la vm hadoop vers hdfs (avec suppression du fichier):  
     hdfs dfs -moveFromLocal /path/to/file.csv /path/in/HDFS/to/put/file.csv

## Monitoring de la VM  
Ambari: http://localhost:8080  

## Scripts  
1) Machine locale
- 

2) VM HDP
- createAborescence.py : permet de generer l'arborescence sur la vm HDP   
![image de la ligne modifiable](/img/arborescence_modifiable.PNG)  
Cette ligne est modifiable dans la fonction <creation_sous_dossier>.  


3) Scripts communs:
- 