# requete-r-ponse-http
requete &amp; réponse http


1xx - Information
  
100	Continue	Attente de la suite de la requête.

101	Switching Protocols	Acceptation du changement de protocole.

102	Processing	WebDAV RFC 25183,4: Traitement en cours (évite que le client dépasse le temps d’attente limite).

103	Early Hints	RFC 82975 : (Expérimental) Dans l'attente de la réponse définitive, le serveur retourne des liens que le client peut commencer à télécharger.



2xx - Succès

200	OK	Requête traitée avec succès. La réponse dépendra de la méthode de requête utilisée.

201	Created	Requête traitée avec succès et création d’un document.

202	Accepted	Requête traitée, mais sans garantie de résultat.

203	Non-Authoritative Information	Information retournée, mais générée par une source non certifiée.

204	No Content	Requête traitée avec succès mais pas d’information à renvoyer.

205	Reset Content	Requête traitée avec succès, la page courante peut être effacée.

206	Partial Content	Une partie seulement de la ressource a été transmise.

207	Multi-Status	WebDAV : Réponse multiple.

208	Already Reported	WebDAV : Le document a été envoyé précédemment dans cette collection.

210	Content Different	WebDAV : La copie de la ressource côté client diffère de celle du serveur (contenu ou propriétés).

226	IM Used	RFC 32296 : Le serveur a accompli la requête pour la ressource, et la réponse est une représentation du résultat d'une ou plusieurs manipulations d'instances appliquées à l'instance actuelle.



3xx - Redirection

300	Multiple Choices	L’URI demandée se rapporte à plusieurs ressources.

301	Moved Permanently	Document déplacé de façon permanente.

302	Found	Document déplacé de façon temporaire.

303	See Other	La réponse à cette requête est ailleurs.

304	Not Modified	Document non modifié depuis la dernière requête.

305	Use Proxy (depuis HTTP/1.1)	La requête doit être ré-adressée au proxy.

306	Switch Proxy	Code utilisé par une ancienne version de la RFC 26167, à présent réservé. Elle signifiait « Les requêtes suivantes doivent utiliser le proxy spécifié »8.

307	Temporary Redirect	La requête doit être redirigée temporairement vers l’URI spécifiée.

308	Permanent Redirect	La requête doit être redirigée définitivement vers l’URI spécifiée.

310	Too many Redirects	La requête doit être redirigée de trop nombreuses fois, ou est victime d’une boucle de redirection.


4xx - Erreur du client web

400	Bad Request	La syntaxe de la requête est erronée.

401	Unauthorized	Une authentification est nécessaire pour accéder à la ressource.

402	Payment Required	Paiement requis pour accéder à la ressource.

403	Forbidden	Le serveur a compris la requête, mais refuse de l'exécuter. Contrairement à l'erreur 401, s'authentifier ne fera aucune différence. Sur les serveurs où l'authentification est requise, cela signifie généralement que l'authentification a été acceptée mais que les droits d'accès ne permettent pas au client d'accéder à la ressource.

404	Not Found	Ressource non trouvée.

405	Method Not Allowed	Méthode de requête non autorisée.

406	Not Acceptable	La ressource demandée n'est pas disponible dans un format qui respecterait les en-têtes « Accept » de la requête.

407	Proxy Authentication Required	Accès à la ressource autorisé par identification avec le proxy.

408	Request Time-out	Temps d’attente d’une requête du client, écoulé côté serveur. D'après les spécifications HTTP : « Le client n'a pas produit de requête dans le délai que le serveur était prêt à attendre. Le client PEUT répéter la demande sans modifications à tout moment ultérieur »9.

409	Conflict	La requête ne peut être traitée en l’état actuel.

410	Gone	La ressource n'est plus disponible et aucune adresse de redirection n’est connue.

411	Length Required	La longueur de la requête n’a pas été précisée.

412	Precondition Failed	Préconditions envoyées par la requête non vérifiées.

413	Request Entity Too Large	Traitement abandonné dû à une requête trop importante.

414	Request-URI Too Long	URI trop longue.

415	Unsupported Media Type	Format de requête non supporté pour une méthode et une ressource données.

416	Requested range unsatisfiable	Champs d’en-tête de requête « range » incorrect.

417	Expectation failed	Comportement attendu et défini dans l’en-tête de la requête insatisfaisante.

418	I’m a teapot	« Je suis une théière » : Ce code est défini dans la RFC 232410 datée du 1er avril 1998, Hyper Text Coffee Pot Control Protocol.

421	Bad mapping / Misdirected Request	La requête a été envoyée à un serveur qui n'est pas capable de produire une réponse (par exemple, car une connexion a été réutilisée).

422	Unprocessable entity	WebDAV : L’entité fournie avec la requête est incompréhensible ou incomplète.

423	Locked	WebDAV : L’opération ne peut avoir lieu car la ressource est verrouillée.

424	Method failure	WebDAV : Une méthode de la transaction a échoué.

425	Unordered Collection	WebDAV RFC 364811 : Ce code est défini dans le brouillon WebDAV Advanced Collections Protocol, mais est absent de Web Distributed Authoring and Versioning (WebDAV) Ordered Collections Protocol.

426	Upgrade Required	RFC 281712 : Le client devrait changer de protocole, par exemple au profit de TLS/1.0.

428	Precondition Required	RFC 658513 : La requête doit être conditionnelle.

429	Too Many Requests	RFC 658514 : Le client a émis trop de requêtes dans un délai donné.

431	Request Header Fields Too Large	RFC 658514 : Les entêtes HTTP émises dépassent la taille maximale admise par le serveur.

449	Retry With	Code défini par Microsoft. La requête devrait être renvoyée après avoir effectué une action.

450	Blocked by Windows Parental Controls	Code défini par Microsoft. Cette erreur est produite lorsque les outils de contrôle parental de Windows sont activés et bloquent l’accès à la page.

451	Unavailable For Legal Reasons	Ce code d'erreur indique que la ressource demandée est inaccessible pour des raisons d'ordre légal15,16.

456	Unrecoverable Error	WebDAV : Erreur irrécupérable.


xx - Erreur du serveur / du serveur d'application

500	Internal Server Error	Erreur interne du serveur.

501	Not Implemented	Fonctionnalité réclamée non supportée par le serveur.

502	Bad Gateway ou Proxy Error	En agissant en tant que serveur proxy ou passerelle, le serveur a reçu une réponse invalide depuis le serveur distant.

503	Service Unavailable	Service temporairement indisponible ou en maintenance.

504	Gateway Time-out	Temps d’attente d’une réponse d’un serveur à un serveur intermédiaire écoulé.

505	HTTP Version not supported	Version HTTP non gérée par le serveur.

506	Variant Also Negotiates	RFC 229518 : Erreur de négociation. Transparent content negociation.

507	Insufficient storage	WebDAV : Espace insuffisant pour modifier les propriétés ou construire la collection.

508	Loop detected	WebDAV : Boucle dans une mise en relation de ressources (RFC 584219).

509	Bandwidth Limit Exceeded	Utilisé par de nombreux serveurs pour indiquer un dépassement de quota.

510	Not extended	RFC 277420 : La requête ne respecte pas la politique d'accès aux ressources HTTP étendues.

511	Network authentication required	RFC 658514 : Le client doit s'authentifier pour accéder au réseau. Utilisé par les portails captifs pour rediriger les clients vers la page d'authentification.

