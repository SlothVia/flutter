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