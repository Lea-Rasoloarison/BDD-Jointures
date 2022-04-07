# BDD-Jointures
BDD Jointures


1 - Retourne les noms, prénoms, rôle et équipe de tous les joueurs, classés dans l’ordre alphabétique par équipe, puis par rôle dans l’équipe, puis par nom de famille, puis par prénom.


SELECT firstname, lastname, role, team_id
FROM wizard
INNER JOIN player ON wizard.id=player.wizard_id ORDER BY team_id ASC, role ASC, lastname ASC, firstname ASC ;

https://zupimages.net/up/22/14/2ap5.png

2 - Retourne uniquement les prénoms et noms des joueurs ayant le rôle de seeker (attrapeur), classés par ordre alphabétique de nom puis prénom

SELECT firstname, lastname, role 
FROM wizard
INNER JOIN player ON wizard.id=player.wizard_id WHERE role='seeker' ORDER BY lastname ASC, firstname ASC ;

https://zupimages.net/up/22/14/mnpt.png

3 - Retourne la liste de tous les sorciers qui ne pratiquent pas le quidditch.

SELECT firstname, lastname, role 
FROM wizard
INNER JOIN player ON wizard.id=player.wizard_id WHERE role='NULL' ORDER BY lastname ASC, firstname ASC ;
