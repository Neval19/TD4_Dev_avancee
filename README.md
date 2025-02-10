Question 1.1 La taille par défaut d'une clé RSA est de 2048 bits 
Pour créer une clé de 4096 bits il faut utiliser la commande :
openssl genrsa -out server.key 4096
Question 1.2 
Pour extraire la clé publique il faut utiliser la commande : 
openssl rsa -in server.key -pubout -out server.pub
Question 2.1
Pour obtenir une nouvelle paire de clés RSA protégée avec l'algorithme DES3
openssl genrsa -des3 -out protected.key 4096
Avec pour mot de passe "123456"
Question 2.2
openssl rsa -in protected.key -pubout -out protected.pub
Il n'y a pas de différence car c'est seulement la clé privé qui est protégée.
Question 3.1 
openssl dgst -sha256 exemple.txt
SHA2-256(exemple.txt)= dfd6d03c745a8db93ae7b723b425d15b538851fd94289e7214c0efbf2e55bc51
openssl dgst -md5 exemple.txt
MD5(exemple.txt)= aee6fa45a4432fe6fb3f934bc9286eec
openssl dgst -sha1 exemple.txt
SHA1(exemple.txt)= 8617f6ad0c75bcae63c09cc88018f3d2f80ea3ca

La taille de MD5 est de 128 bits et SHA-1 de 160 bits.

Kevin Jiang 302

