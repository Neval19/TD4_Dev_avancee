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
