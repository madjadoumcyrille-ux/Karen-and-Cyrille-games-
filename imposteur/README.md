# IMPOSTEUR — by M. Cyrille

Jeu mobile-first de bluff et déduction, en français, pour 2 à 8 joueurs. Créateur affiché dans le jeu : **M. Cyrille · CST de Sarh**.

## Lien GitHub Pages
Une fois GitHub Pages actif, le jeu est ici :
https://madjadoumcyrille-ux.github.io/Karen-and-Cyrille-games-/imposteur/

## Jouer
1. Ouvre le lien sur Android, iPhone ou ordinateur.
2. L'hôte choisit un pseudo et crée une salle privée.
3. Il partage le code de 5 caractères ou le lien d'invitation.
4. Les autres entrent leur pseudo et le code, ou ouvrent le lien.
5. L'hôte lance la manche. Chacun découvre son rôle en privé.
6. Discutez, donnez des indices sans dire le mot, puis l'hôte ouvre le vote.
7. Le résultat révèle le mot, l'imposteur et les votes. L'hôte peut relancer une manche.

## Déploiement
Le workflow GitHub Pages déjà présent déploie le dépôt entier, sous-dossiers compris. Après le commit, vérifie l'onglet Actions et le réglage Settings → Pages → Source: GitHub Actions.

## Architecture réseau
Le prototype utilise PeerJS/WebRTC pour connecter les navigateurs directement, avec l'hôte comme arbitre de partie. PeerServer Cloud sert à la signalisation; les données de jeu transitent par les connexions de données WebRTC. C'est une vraie synchronisation entre navigateurs lorsqu'une connexion P2P s'établit, mais la disponibilité dépend des réseaux mobiles, des restrictions NAT/firewall et du service de signalisation partagé. Les salles disparaissent quand l'hôte ferme la page. Ce prototype n'est pas un service compétitif à haute disponibilité : pour une version commerciale, remplace l'hôte-P2P par un backend persistant (par ex. Supabase Realtime ou un serveur WebSocket), ajoute validation serveur des rôles/votes, reconnexion, modération et tests multi-appareils.

## Installation sur téléphone
- Android/Chrome : ouvre le lien, menu ⋮ → Installer l'application / Ajouter à l'écran d'accueil.
- iPhone/Safari : Partager → Sur l'écran d'accueil.
- Une connexion Internet est requise pour le multijoueur. Le cache PWA ne rend pas les salles hors ligne.
