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
"33"
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
"33"
"Marseille"
"1984"
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
"32"
"MATHIEUX CODABEE ET J'AI 33 ANS" 
"mathieux codabee et j'ai 33 ans" 
"Le gras c'est la vie"
  """Salut
  ça va ?""" 
````

