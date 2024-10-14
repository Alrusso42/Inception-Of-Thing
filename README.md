# 42_inception_of_things

# Explication :

**K3s**

- K3s est une version allégée de Kubernetes, conçue pour être facile à installer et à gérer, particulièrement sur des environnements à ressources limitées comme les IoT ou les environnements de développement. Il simplifie l’utilisation de Kubernetes tout en offrant les fonctionnalités essentielles pour orchestrer des conteneurs.

**Vagrant**

Vagrant est un outil de gestion de machines virtuelles qui permet de créer et de configurer des environnements de développement reproductibles. Il utilise des "fichiers de configuration" pour automatiser la mise en place d'environnements, facilitant ainsi le travail en équipe et l’intégration de nouvelles technologies.

**K3d**

K3d est un outil qui permet de faire fonctionner K3s dans des conteneurs Docker. Il simplifie le déploiement de clusters K3s pour le développement et les tests, en permettant aux développeurs de créer rapidement des environnements Kubernetes légers sans avoir à gérer des installations complexes.

**Intégration continue (CI) et Argo CD**

L'intégration continue est une pratique de développement où les modifications du code sont fréquemment intégrées dans un dépôt partagé. Cela permet de détecter rapidement les problèmes. Argo CD est un outil d’optimisation pour la gestion de déploiements Kubernetes. Il utilise la méthode GitOps, permettant de déployer automatiquement des applications en synchronisant l’état des déploiements avec la configuration stockée dans un dépôt Git.

**Kubernetes**

Kubernetes est un système open-source qui permet de gérer des conteneurs d’applications (des petits environnements d’exécution qui regroupent tout le nécessaire pour faire tourner une application). Il automatise plusieurs tâches, comme le déploiement, la mise à l’échelle et la gestion des conteneurs. En gros, Kubernetes aide à orchestrer (ou gérer) des applications composées de nombreux conteneurs, ce qui facilite leur déploiement sur des serveurs, tout en assurant leur disponibilité et leur performance.

**IoT (Internet Of Thing)**
# ==> Reseau d'appareil leur permettant de communiquer entre eux pour ameliorer l efficacite des services



## Part 1 : 
Order :
- vagrant up
- vagrant SSH
- ifconfig eth1
- Verification du nom des VM
- k3s --version
- kubectl get nodes -o wide"

## Part 2 :
Order :
- Ouverture des ports pour les app1, 2 et 3
- vagrant up
- vagrant SSH
- ifconfig eth1
- ip addr show eth1
- Verification du nom des VM
- k3s --version
- kubectl get nodes -o wide"
- kubectl get all -n kube-system
- curl -H "Host:app2.com" 192.168.56.110
- Acces a l application depuis un navigateur

## Part 3 :
Order :
- Vagrant up
- Vagrant SSH
- Verification de la presence des fichiers de configuration
- ./install.sh
- kubectl get ns
- kubectl get pods -n dev
- Expliquer la difference entre namespace et un pod
# ==> Un namespace c'est un espace pour organiser les ressources (gestion de droit etc.. par exemple), tandis que le pod c'est une unite pour executer  des applications. Donc un namespace peut contenir plusieurs pod, mais l'inverse n est pas vrai
- kubectl get services -A
- Verifier que le login de quelqu un du groupe q ete inclus dans le nom du depot github
- Vérifiez qu'une image Docker est utilisée dans le dépôt Github. L'image peut être celle de Wil ou une image personnalisée. Dans ce dernier cas, vérifiez que le login d'un membre du groupe a été inclus dans le nom du dépôt Dockerhub. Assurez-vous également qu'il y a les deux tags requis dans le dépôt Dockerhub.
- Allez sur : http://192.168.56.110:8080" (Port a verifier)
- Se connecter : login = admin password = le password afficher apres l execution du script
- Parcours de l application dans argocd
-  curl http://localhost:8888/
- >sed -i 's/wil42\/playground\:v1/wil42\/playground\:v2/g' deploy.yaml
$>g up "v2" # git add+commit+push
[..]
a773f39..999b9fe master -> master
- cat deployment.yaml | grep v2










