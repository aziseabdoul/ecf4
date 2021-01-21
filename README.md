**FRONT**
https://ecf4550631279.wordpress.com/

**BACK**
*En tant qu'user authentifié avec toutes les permissions et après avoir récupéré le JWT*
POST http://localhost:1337/sujets-de-discussions

{
    "titre": "Qu'est ce que strapi ?",
    "id_user": 3,
    "date_creation": "2021-01-20"
}

POST http://localhost:1337/messages

{
    "corps": "Strapi est un CMS",
    "id_user": 3,
    "id_sujet": 3,
    "date_creation": "2021-01-20"
}

*En tant qu'un autre user authentifié avec toutes les permissions + JWT*
GET http://localhost:1337/sujets-de-discussions/3
GET http://localhost:1337/messages/1
