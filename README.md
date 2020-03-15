# monpremierflutter

Mon premier project avec Flutter

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://flutter.dev/docs/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://flutter.dev/docs/cookbook)

For help getting started with Flutter, view our
[online documentation](https://flutter.dev/docs), which offers tutorials,
samples, guidance on mobile development, and a full API reference.
"# flutter"


# Section 4 : Les bases de DART

## Les variables

````dart
void main() {
  var prenom = "Mathieu";
  print(prenom);
  prenom = "Georges";
  print(prenom);
  
  String nom = "Codabee";
  print(nom);
  
  int age = 33;
  print(age);
}

//Console
"Mathieu"
"Geoges"
"Codabee"
33
````

## Constantes et Final

````dart
void main() {
  var prenom = "Mathieu";
  print(prenom);
  prenom = "Georges";
  print(prenom);
  
  String nom = "Codabee";
  print(nom);
  
  int age = 33;
  print(age);
  
  const lieuDeNaissance = "Marseille";
  const int annee = 1984;
  print(lieuDeNaissance);
  print(annee);
  
  final passion = "développer des applications";
  final String sport = "AquaPoney";
  print(passion);
  print(sport);
}

//Console
"Mathieu"
"Geoges"
"Codabee"
33
"Marseille"
1984
"développer des applications"
"AquaPoney"
````
## String ou chaînes de caractères

````dart
void main() {
  String prenom = "Mathieu";
  prenom += "x";
  var nom = "Codabee";
  var age = 33;
  var nomcomplet = prenom + ' ' + nom + " et j'ai " + age.toString() + " ans";
  print(nomcomplet);

  var nomComplet = "$prenom $nom et j'ai $age ans ";
  print(nomComplet);

  print(nomComplet.length);
  print(nomComplet.toUpperCase());
  print(nomComplet.toLowerCase());

  String citation = 'Steve Jobs a dis : "Stay hungry , stay foolish"';
  String phrase = "C'est la vie";
  phrase = "Le gras c'est la vie";
  print(phrase);

  String triple = """
  Salut
  ça va ? 
  """;
  print(triple);
}

//Console
"Mathieux Codabee et j'ai 33 ans"
"Mathieux Codabee et j'ai 33 ans"
32
"MATHIEUX CODABEE ET J'AI 33 ANS" 
"mathieux codabee et j'ai 33 ans" 
"Le gras c'est la vie"
  """Salut
  ça va ?""" 
````

## Les nombres

````dart
void main() {
  //int -> Nombre entier
  //double -> nombre avec décimale

  int entier = 8;
  int operation = 3;
  double decimal = 33.3;
  print(entier);
  print(decimal);

  var sansType = 5;
  print(sansType);

  var addition = entier + operation;
  print(addition);
  var multiplication = entier * operation;
  print(multiplication);
  var soustraction = entier - operation;
  print(soustraction);
  var division = (entier / operation).floor();
  var remain = entier % operation;
  print(division);
  print(remain);
}

//Console
8
33.3
5
11
24
5
2
2
````

## Les Booléens

````dart
void main() {
  bool jaimeDart = true;
  print(jaimeDart);

  bool enTrainDeTelecharger = true;
  enTrainDeTelecharger = false;
}

//Console
true
````

## Les listes

````dart
void main() {
  List maListe = ["Pierre", "Paul", "Jacques"];
  print(maListe);
  print(maListe.length);
  print(maListe[0]);
  maListe.add("Georges");
  print(maListe);
  maListe.remove("Pierre");
  maListe.removeAt(0);
  print(maListe);
}

//Console
[Pierre, Paul, Jacques]
3
Pierre
[Pierre, Paul, Jacques, Georges]
[Paul, Jacques, Georges]
````

## Les Maps

````dartvoid main() {
  Map maMap = {"Pierre": 21, "Paul": 17, "Jacques": 56};
  print(maMap.length);

  maMap["Georges"] = 34;
  print(maMap);

  maMap.remove("Pierre");
  maMap.clear();
  print(maMap);
}

//Console
3
{Pierre: 21, Paul: 17, Jacques: 56, Georges: 34}
{}
````

## Les conditions

````dart
void main() {
  //Egalité ==
  //Difference !=
  //Sup >
  //Inf <
  //SupEgal >=
  //InfEgal <=

  var age = 6;
  var ilPleut = true;

  if (age == 18) {
    print("Oui");
  } else {
    print("Non");
  }

  print(age == 18 ? "Oui" : "Non");

  if (age >= 18) {
    print("En voiture");
  } else if (age >= 12) {
    print("Dans le bus");
  } else {
    print("Dans la pousette");
  }

  if (!ilPleut) {
    print("Prend ton kway");
  } else {
    print("Prend ton maillot");
  }
}

//Console
"Non"
"Non"
"Dans la pousette"
"Prend ton maillot"
````

## Les boucles For

````dart
void main() {
  print("Hello 1");
  print("Hello 2");

  for (var x = 0; x < 10; x++) {
    print("Salut les codeurs ${x + 1} fois");
  }

  List<String> maListe = ["Pierre", "Paul", "Jacques"];
  for (var x = 0; x < maListe.length; x++) {
    print(maListe[x]);
  }

  maListe.forEach((prenom) {
    print(prenom);
  });

  maListe.forEach((prenom) => print(prenom));

  Map map = {1: "Je", 2: "Tuco", 3: "Blondin", 4: "Sentenza"};

  map.forEach((key, value) {
    print("Numéro de key :  $key ===> nom : $value ");
  });

  map.forEach(
      (key, value) => print("Numéro de key :  $key ===> nom : $value "));
}

//Console
"Hello 1"
"Hello 2"
"Salut les codeurs 1 fois"
"Salut les codeurs 2 fois"
"Salut les codeurs 3 fois"
"Salut les codeurs 4 fois"
"Salut les codeurs 5 fois"
"Salut les codeurs 6 fois"
"Salut les codeurs 7 fois"
"Salut les codeurs 8 fois"
"Salut les codeurs 9 fois"
"Salut les codeurs 10 fois"
"Pierre"
"Paul"
"Jacques"
"Pierre"
"Paul"
"Jacques"
"Pierre"
"Paul"
"Jacques"
"Numéro de key :  1 ===> nom : Je" 
"Numéro de key :  2 ===> nom : Tuco" 
"Numéro de key :  3 ===> nom : Blondin" 
"Numéro de key :  4 ===> nom : Sentenza" 
"Numéro de key :  1 ===> nom : Je" 
"Numéro de key :  2 ===> nom : Tuco" 
"Numéro de key :  3 ===> nom : Blondin" 
"Numéro de key :  4 ===> nom : Sentenza" 
````

## Les boucles While

````dart
void main() {
  var nombreDeBut = 3;
  /*while(nombreDeBut < 3) {
    print ("ouf on n'a pris que $nombreDeBut buts");
    nombreDeBut++;
  }*/
  do {
    print("ouf on n'a pris que $nombreDeBut buts");
    nombreDeBut++;
  } while (nombreDeBut < 3);
}

//Console
"ouf on n'a pris que 3 buts"
````

## Les Switch

````dart
void main() {
  var ville = "Marseille";

  switch (ville) {
    case "Paris":
      print("ici c'est Paris");
      break;
    case "Marseille":
      print("A jamais les premiers");
      break;
    case "Nice":
      print("Issa Nissa");
      break;
    default:
      break;
  }
}

//Console
"A jamais les premiers"
````

## Les fonctions de base

````dart
void main() {
   void maPremiereFonction() {
    //Code de la fonction
   print("Super ma première fonction en Dart");
  }
  
  maPremiereFonction();
}

//Console 
"Super ma première fonction en Dart"
````

## Les fonctions avec paramètres

````dart
void main() {
  void maPremiereFonction() {
    //Code de la fonction
    print("Salut");
    print("Super ma première fonction en Dart");
  }

  maPremiereFonction();

  void saluer(String prenom) {
    print("Salutation $prenom");
  }

  saluer("Mathieu");
}

//Console
"Salut"
"Super ma première fonction en Dart"
"Salutation Mathieu"
````

## Les fonctions avec retour

````dart
void main() {
  String saluer2(String prenom) {
    return "Salut $prenom";
  }

  var salutation = saluer2("Claude");
  print(salutation);

  int aireDuChamps(int longueur, int largeur) {
    return longueur * largeur;
  }

  print(aireDuChamps(4, 2));

  int aireModifie(int longueur, int largeur) => longueur * largeur;
  print(aireModifie(5, 2));
}

//Console
"Salut Claude"
8
10
````

## Exercices

````dart
//Faire une boucle de 0 à 100 et imprimer uniquement les nombres impairs
void main(){
for(var x = 0; x<100; x++){
    if (x%2 != 0){
      print(x);
    }
  }
}
````

````dart
//Créer une fonction pour convertir les degrés celsius en Farheneight
void main() {
  void convertir(int temp){
      print("En celsius, la température est $temp °C");
      var temp2 = (temp * 9/5) + 32;
      print("En Fahrenheit, la température devient $temp2 F");
  }
  convertir(24);
}
````

````dart
void main() {
  var age = 24;
    if (age >= 0 && age <12) {
      print("Eau");
    }else if(age >= 12 && age < 18){
      print("Soda");
    }else{
      print("Bière");
    }
}
````

````dart
//Créer une Map String, bool avec une liste de garçons et filles, faire un print uniquement pour les filles
void main(){
  Map liste = {"Pierre": false, "Paul": false, "Jacques": false, "Paula": true, "Marie": true};
  liste.forEach((key, value) {
    if (value == true){
      print ("$key est une fille");
    }else {
      print("$key est un garçon");
    }
  });
}
````

# Section 5 : La programmation orienté objet


## L'Objet

Classe

````dart
void main() {
  var punto = new Voiture("Fiat", "Punto", 66000, 2011, "Vert");
  print(punto.marque);
  print(punto.kilometrage);
  punto.rouler();
  print(punto.kilometrage);

  var clio = new Voiture("Renault", "Clio", 210000, 2007, "Blanc");
  print(clio.modele);
}

class Voiture {
  String marque;
  String modele;
  int kilometrage;
  int annee;
  String couleur;

  void rouler() {
    kilometrage++;
    print("Broom Broom");
  }

  Voiture(String marque, String modele, int kilometrage, int annee,
      String couleur) {
    this.marque = marque;
    this.modele = modele;
    this.kilometrage = kilometrage;
    this.annee = annee;
    this.couleur = couleur;
  }
}

//Console
"Fiat"
66000
"Broom Broom"
66001
"Clio"
````

## L'héritage

````dart
void main() {
  var punto = new Voiture("Fiat", "Punto", 66000, 2011, "Vert");
  print(punto.marque);
  print(punto.kilometrage);
  punto.rouler();
  print(punto.kilometrage);

  var clio = new Voiture("Renault", "Clio", 210000, 2007, "Blanc");
  print(clio.modele);

  var cc = new Cabriolet("Peugeot", "202cc", 20000, 2006, "Gris clair");
  print(cc.couleur);
  cc.cheveuxAuxVents();
  cc.rouler();

  var trac = new Tracteur(
      "???", "Le rouge avec les grosses roues", 3000, 1970, "rouge", 25);
  trac.rouler();
  print(trac.kilometrage);
  trac.pasPresse();
}

class Voiture {
  String marque;
  String modele;
  int kilometrage;
  int annee;
  String couleur;

  void freiner() {}

  void rouler() {
    kilometrage++;
    print("Broom Broom");
  }

  Voiture(String marque, String modele, int kilometrage, int annee,
      String couleur) {
    this.marque = marque;
    this.modele = modele;
    this.kilometrage = kilometrage;
    this.annee = annee;
    this.couleur = couleur;
  }
}

class Tracteur extends Voiture {
  int vitesseMax;

  void pasPresse() {
    print(
        "Vous qui etes derrière moi, prenez patience. Je ne vais qu'à $vitesseMax maximum");
  }

  Tracteur(String marque, String modele, int kilometrage, int annee,
      String couleur, int vitesseMax)
      : super(marque, modele, kilometrage, annee, couleur) {
    this.vitesseMax = vitesseMax;
  }
}

class Cabriolet extends Voiture {
  int tempsDeDecapotage = 3;

  void cheveuxAuxVents() {
    print("Je fais le cake sur le promenade des anglais ");
  }

  Cabriolet(
      String marque, String modele, int kilometrage, int annee, String couleur)
      : super(marque, modele, kilometrage, annee, couleur);
}

//Console 
"Fiat"
66000
"Broom Broom"
66001
"Clio"
"Gris clair"
"Je fais le cake sur le promenade des anglais" 
"Broom Broom"
"Broom Broom"
3001
"Vous qui etes derrière moi, prenez patience. Je ne vais qu'à 25 maximum"
````

## Le Polymorphisme

````dart
void main() {
  var tri = new Triangle(4,2);
  tri.calculerAire();
  
  var car = new Carre(4,2);
  car.calculerAire();
}

class Triangle extends Forme {
  
  // largeur * longueur / 2 
  @override
  void calculerAire(){
    super.calculerAire();
    var aire = largeur * longueur / 2;
    print("L'aire est $aire ");
  }
  
  Triangle(int largeur, int longueur) : super(largeur, longueur);
}

class Carre extends Forme {
  
  //largeur * longueur
  @override
  void calculerAire(){
    super.calculerAire();
    var aire = longueur * largeur;
    print("L'aire est $aire");
  }
  Carre(int largeur, int longueur) : super(largeur, longueur);
}

class Forme {
  int largeur;
  int longueur;

  void calculerAire() {
    print("Calcul de l'aire en cours ....");
  }

  Forme(int largeur, int longueur) {
    this.largeur = largeur;
    this.longueur = longueur;
  }
}

//Console
"Calcul de l'aire en cours ...."
"L'aire est 4"
"Calcul de l'aire en cours ...."
"L'aire est 8"
````