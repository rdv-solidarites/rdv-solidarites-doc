# Notifications

  
Questions sur la fonctionnalité de notification à l'agent lorsque le RDV est posé dans un court délai :  


* C'est lorsque le RDV a lieu dans les 24h ou 48h ?
* Y a-t-il notification en cas d'annulation dans ce délais?
* Y a-t-il notification en cas de modification de la date d'un RDV initialement plus lointain?



  
un coup d'œil au code me donne l'impression qu'on notifie l'agent  


* en cas de suppression par l'agent \(apparemment pas par l'usager, mais peut-être ne peut-il pas annuler de lui même ?\)
* Changement dans les 48h

  
mais pas dans le cas d'une modification lointaine  
\(je trouve que c'est pas forcement très clair dans le code, Adrien Di Pasquale qui a fait quelque incursion dans cette partie de l'appli saura peut-être mieux dire que moi :-/\)  


-&gt;  


1. ce n'est ni dans les 24h ni dans les 48h mais si le RDV a lieu "aujourd'hui ou demain" ce qui est subtilement différent de 48h
2.  si tu parles de notifications pour l'agent dans le cas ou c'est l'usager qui annule \(ou un autre agent\) Camille Garrigue il n'y en a jamais, ca n'existe pas \(sauf oubli de ma part\).
3. bonne question, non le fait de repousser un RDV du passé à maintenant + 1h par exemple ne declenchera pas de notif. ca me parait un peu tordu quand meme non ?







Dans le cas 1. c'est à 9h le matin qu'on analyse les rdv dans cette situation c'est bien ça ?

  
 

