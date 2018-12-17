HelloWorld-html5 : 
Prendre le .war présent dans le target
Renommer le fichier en hibernate.war
Mettre le fichier dans le dossier Docker.
Faire : sudo docker build --tag=hibernate .
Puis : sudo docker run -it --rm -p 8080:8080 hibernate

Les URL fonctionnants : 
localhost:8080/hibernate/connexion.html (page html)
localhost:8080/hibernate/inscription.html (page html)

Les URL ne fonctionnants pas totalement (manque la connexion aux fichiers externes)
localhost:8080/hibernate/hello/json/connexion/{pseudo}/{mot de passe}
localhost:8080/hibernate/hello/json/inscription/{pseudo}/{mot de passe}/{confirmation mdp}/{email}
localhost:8080/hibernate/hello/json/merguez/{id_user}/{text}//SET tweet
localhost:8080/hibernate/hello/json/merguez/{id_user}//GET tweet
localhost:8080/hibernate/hello/json/home/{id_user}
localhost:8080/hibernate/hello/json/home

Les URL Non Testés à voir
localhost:8080/hibernate/hello/json/comment/{id_tweet}/{id_user}/{text}   //SET comment
localhost:8080/hibernate/hello/json/comment/{id_tweet}    //GET comment
localhost:8080/hibernate/hello/json/like/{id_tweet}/{id_user}/{text}   //SET comment
localhost:8080/hibernate/hello/json/like/{id_tweet}    //GET comment
localhost:8080/hibernate/hello/json/follow/{id_user}/{id_user_follow}  //SET follow
localhost:8080/hibernate/hello/json/follow/{id_user}    //GET follow