# flutter

#### Voici quelques-unes des commandes Flutter couramment utilisées avec leurs explications :

1. **Créer un nouveau projet Flutter :**
   ```bash
   flutter create nom_du_projet
   ```
   - Cette commande génère un nouveau projet Flutter avec la structure de base.

2. **Exécuter l'application sur un émulateur ou un appareil connecté :**
   ```bash
   flutter run
   ```
   - Compile et exécute l'application sur l'émulateur ou l'appareil connecté.

3. **Mettre à jour les dépendances du projet :**
   ```bash
   flutter pub get
   ```
   - Télécharge les dépendances spécifiées dans le fichier pubspec.yaml.

4. **Vérifier la santé de l'installation Flutter :**
   ```bash
   flutter doctor
   ```
   - Vérifie si Flutter est correctement installé sur votre machine et donne des conseils pour résoudre d'éventuels problèmes.

5. **Vérifier les mises à jour disponibles :**
   ```bash
   flutter upgrade
   ```
   - Met à jour Flutter et ses dépendances.

6. **Vérifier la liste des émulateurs disponibles :**
   ```bash
   flutter emulators
   ```
   - Affiche la liste des émulateurs configurés sur votre machine.

7. **Lancer une application sur un émulateur spécifique :**
   ```bash
   flutter run -d nom_emulateur
   ```
   - Exécute l'application sur un émulateur spécifique.

8. **Créer une nouvelle classe ou un nouveau widget :**
   ```bash
   flutter create nom_du_widget.dart
   ```
   - Génère un nouveau fichier Dart pour une classe ou un widget.

9. **Lancer un test unitaire :**
   ```bash
   flutter test
   ```
   - Exécute les tests unitaires dans le répertoire "test".

10. **Activer le mode "Hot Reload" :**
    ```bash
    r
    ```
    - Dans la console où l'application est en cours d'exécution, appuyez sur "r" pour effectuer un rechargement à chaud (Hot Reload). Cela applique instantanément les modifications sans redémarrer l'application.

11. **Build APK (Android) :**
    ```bash
    flutter build apk
    ```
    - Génère un fichier APK pour le déploiement sur des appareils Android.

12. **Build IPA (iOS) :**
    ```bash
    flutter build ios
    ```
    - Génère un fichier IPA pour le déploiement sur des appareils iOS.

13. **Créer un lanceur d'icône d'application :**
    ```bash
    flutter pub run flutter_launcher_icons:main
    ```
    - Met à jour l'icône de l'application en fonction de la configuration spécifiée dans le fichier pubspec.yaml.

Ces commandes devraient vous aider à démarrer avec Flutter et à gérer votre projet efficacement. N'oubliez pas de consulter la documentation officielle de Flutter pour des informations plus détaillées sur chaque commande : https://flutter.dev/docs/development/tools/flutter-cli

#### Expliaction pour chaque fichier dans le projet
### Fichier pubspec.yaml:

1. **`name: cnn_classification`**: Nom du projet Flutter.

2. **`description: "A new Flutter project."`**: Description du projet.

3. **`publish_to: 'none'`**: Empêche la publication accidentelle sur pub.dev.

4. **`version: 1.0.0+1`**: Numéro de version de l'application.

5. **`environment: sdk: '>=3.2.0 <4.0.0'`**: Version minimale du SDK Flutter requise.

6. **`dependencies`**: Les dépendances du projet :
   - `flutter`: SDK Flutter.
   - `cupertino_icons`: Icônes Cupertino.
   - `tflite_v2`: TensorFlow Lite pour Flutter.
   - `image_picker`: Plugin pour sélectionner des images.
   - `image`: Manipulation d'images.

7. **`dev_dependencies`**: Dépendances de développement :
   - `flutter_test`: Dépendance de test.
   - `flutter_lints`: Ensemble de linters pour encourager de bonnes pratiques de codage.

8. **`flutter`**:
   - `uses-material-design`: Utilise le design matériel.
   - `assets`: Liste des fichiers d'assets (images, modèles TensorFlow Lite, etc.).

#### Explication :

### Dépendances du Projet (dans `dependencies`):

1. **`flutter: SDK Flutter`**
   - **Rôle :** C'est la dépendance principale qui spécifie la version du SDK Flutter utilisée pour développer l'application.

2. **`cupertino_icons: Icônes Cupertino`**
   - **Rôle :** Ajoute les icônes spécifiques à iOS (Cupertino) pour être utilisées dans l'application Flutter.

3. **`tflite_v2: TensorFlow Lite pour Flutter`**
   - **Rôle :** Intègre TensorFlow Lite dans l'application Flutter, permettant ainsi l'utilisation de modèles TensorFlow Lite pour l'inférence sur des appareils mobiles.
  
    ```markdown
    TensorFlow Lite est une bibliothèque mobile conçue pour déployer des modèles sur des appareils mobiles, des microcontrôleurs et d'autres appareils de périphérie.
    ```

4. **`image_picker: Plugin pour sélectionner des images`**
   - **Rôle :** Fournit une interface pour permettre à l'utilisateur de sélectionner des images à partir de la galerie ou de l'appareil photo de l'appareil.

5. **`image: Manipulation d'images`**
   - **Rôle :** Offre des fonctionnalités de manipulation d'images, telles que le décodage, la modification de la taille et d'autres opérations.

### Dépendances de Développement (dans `dev_dependencies`):

1. **`flutter_test: Dépendance de test`**
   - **Rôle :** Inclut les outils et bibliothèques nécessaires pour écrire et exécuter des tests unitaires et d'intégration dans l'application Flutter.

2. **`flutter_lints: Ensemble de linters pour encourager de bonnes pratiques de codage`**
   - **Rôle :** Intègre un ensemble de linters (règles statiques d'analyse du code) pour encourager des pratiques de codage cohérentes et de haute qualité.

### Configuration Flutter (dans `flutter`):

1. **`uses-material-design: Utilise le design matériel`**
   - **Rôle :** Indique que l'application utilise le design matériel, assurant ainsi une apparence et une expérience utilisateur cohérentes avec les directives de conception de Google.

2. **`assets: Liste des fichiers d'assets`**
   - **Rôle :** Déclare les fichiers d'actifs tels que des images, des modèles TensorFlow Lite, etc., qui seront inclus dans le package de l'application. Ces fichiers peuvent être utilisés par l'application pendant son exécution (par exemple, affichage d'images, chargement de modèles).

### Dossier assets:

- **ai.jpg**: Image utilisée comme arrière-plan du Drawer.
- **model.tflite et model2.tflite**: Modèles TensorFlow Lite utilisés dans l'application.
- **labels.txt et labels2.txt**: Fichiers texte contenant les labels/classes pour les modèles.

### Fichier main.dart:

- Point d'entrée de l'application.
- Configuration de l'apparence de l'application et initialisation du widget principal.

### Fichier MenuBarre.dart:

- Widget de tiroir (Drawer) contenant des liens vers différentes parties de l'application.
- Utilise des dépendances de l'application telles que `loadimage.dart`, `loadimage2.dart`, `main.dart`, et `myhomepage.dart`.

### Fichier myhomepage.dart:

- Widget principal de la page d'accueil de l'application.
- Contient une app bar, un menu latéral et un corps avec un message d'accueil.
- Aucune dépendance externe.

### Fichier loadimage.dart:

- Page permettant à l'utilisateur de sélectionner une image et de faire des prédictions avec un modèle TensorFlow Lite.
- Utilise le plugin `image_picker` pour sélectionner une image depuis la galerie.
- Utilise le modèle TensorFlow Lite `model.tflite` et les labels `labels.txt`.

### Fichier loadimage2.dart:

- Page similaire à `loadimage.dart`, mais utilise un autre modèle TensorFlow Lite (`model2.tflite`) et des labels différents (`labels2.txt`).
- Utilise également le plugin `image_picker` pour sélectionner une image depuis la galerie.

Ces fichiers semblent constituer une application Flutter d'apprentissage profond qui utilise TensorFlow Lite pour la classification d'images. Les dépendances clés sont TensorFlow Lite (`tflite_v2`), le plugin `image_picker` pour la sélection d'images, et le plugin `image` pour la manipulation d'images.

#### Explication:

### main.dart:

```dart
import 'package:cnn_classification/myhomepage.dart';
import 'package:flutter/material.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Flutter Demo',
      theme: ThemeData(
        colorScheme: ColorScheme.fromSeed(seedColor: Colors.blue),
        useMaterial3: true,
      ),
      home: const MyHomePage(title: 'Deep learning application'),
    );
  }
}
```

1. **`import 'package:cnn_classification/myhomepage.dart';`**: Importe la classe `MyHomePage` depuis le fichier `myhomepage.dart`.

2. **`import 'package:flutter/material.dart';`**: Importe le package `flutter/material.dart` qui contient les widgets pour la conception des interfaces utilisateur.

3. **`void main() { runApp(const MyApp()); }`**: Point d'entrée de l'application. La fonction `main` appelle la fonction `runApp` avec une instance de `MyApp`.

4. **`class MyApp extends StatelessWidget {`**: Définit la classe `MyApp` qui est un widget sans état.

5. **`const MyApp({super.key});`**: Constructeur de `MyApp`.

6. **`@override Widget build(BuildContext context) {`**: Implémentation de la méthode `build` qui retourne la structure de l'interface utilisateur de l'application.

7. **`return MaterialApp(`**: Crée une instance de `MaterialApp` qui est la structure de base pour une application Flutter.

8. **`title: 'Flutter Demo',`**: Titre de l'application.

9. **`theme: ThemeData(`**: Configuration du thème de l'application.

10. **`colorScheme: ColorScheme.fromSeed(seedColor: Colors.blue),`**: Définit la couleur principale du thème.

11. **`useMaterial3: true,`**: Active le thème Material 3 (expérimental).

12. **`),`**: Fermeture du thème.

13. **`home: const MyHomePage(title: 'Deep learning application'),`**: Définit la page d'accueil de l'application comme une instance de `MyHomePage` avec un titre spécifique.

14. **`);`**: Fermeture de `MaterialApp`.

### myhomepage.dart:

```dart
import 'package:flutter/material.dart';
import 'package:cnn_classification/MenuBarre.dart';

class MyHomePage extends StatefulWidget {
  const MyHomePage({super.key, required this.title});

  final String title;

  @override
  State<MyHomePage> createState() => _MyHomePageState();
}

class _MyHomePageState extends State<MyHomePage> {
  void _incrementCounter() {
    // Fonction appelée lors de l'incrémentation du compteur (non implémentée dans cet exemple).
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        backgroundColor: Theme.of(context).colorScheme.inversePrimary,
        title: Text(widget.title),
      ),
      drawer: const MenuBarre(),
      body: const Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: <Widget>[
            Text(
              'Bienvenue sur notre application de deep learning. Choisissez le modèle que vous voulez utiliser depuis le menu.',
            ),
          ],
        ),
      ),
      floatingActionButton: FloatingActionButton(
        onPressed: _incrementCounter,
        tooltip: 'Increment',
        child: const Icon(Icons.add),
      ),
    );
  }
}
```

1. **`import 'package:flutter/material.dart';`**: Importe le package `flutter/material.dart`.

2. **`import 'package:cnn_classification/MenuBarre.dart';`**: Importe la classe `MenuBarre` depuis le fichier `MenuBarre.dart`.

3. **`class MyHomePage extends StatefulWidget {`**: Définit la classe `MyHomePage` qui est un widget avec état.

4. **`const MyHomePage({super.key, required this.title});`**: Constructeur de `MyHomePage` avec un titre requis.

5. **`final String title;`**: Titre de la page d'accueil.

6. **`@override State<MyHomePage> createState() => _MyHomePageState();`**: Crée l'état associé à `MyHomePage`.

7. **`class _MyHomePageState extends State<MyHomePage> {`**: Définit la classe d'état pour `MyHomePage`.

8. **`void _incrementCounter() {`**: Fonction qui serait appelée lors de l'incrémentation du compteur (non implémentée dans cet exemple).

9. **`@override Widget build(BuildContext context) {`**: Implémentation de la méthode `build` qui retourne la structure de l'interface utilisateur de la page d'accueil.

10. **`return Scaffold(`**: Crée un Scaffold, la structure de base pour les pages.
    
### `return Scaffold` :

10.1. **Contexte :**
   - Utilisé pour créer la structure globale d'une page ou d'une interface utilisateur.

10.2. **Emplacement :**
   - `Scaffold` englobe généralement tout l'écran et contient des éléments tels que la barre d'applications, le corps de la page, le tiroir (drawer), etc.

12. **`appBar: AppBar(`**: Définit la barre d'applications.

13. **`backgroundColor: Theme.of(context).colorScheme.inversePrimary,`**: Définit la couleur de fond de la barre d'applications.

14. **`title: Text(widget.title),`**: Affiche le titre de la page d'accueil dans la barre d'applications.

15. **`),`**: Fermeture de la barre d'applications.

16. **`drawer: const MenuBarre(),`**: Ajoute un tiroir de navigation (drawer) avec le widget `MenuBarre`.

17. **`body: const Center(`**: Définit le corps de la page.

18. **`child: Column(`**: Crée une colonne d'éléments centrés.

19. **`Text(`**: Affiche un message de bienvenue.

20. **`),`**: Fermeture de la colonne.

21. **`),`**: Fermeture du Centre.

22. **`floatingActionButton: FloatingActionButton(`**: Ajoute un bouton d'action.

23. **`onPressed: _incrementCounter,`**: Associe la fonction `_incrementCounter` à l'appui du bouton.

24. **`tooltip: 'Increment',`**: Tooltip du bouton.

25. **`child: const Icon(Icons.add),`**: Icône du bouton.

26. **`),`**: Fermeture du FloatingActionButton.

27. **`);`**: Fermeture du Scaffold.

### MenuBarre.dart:

```dart
import 'package:cnn_classification/loadimage.dart';
import 'package:cnn_classification/loadimage2.dart';
import 'package:cnn_classification/main.dart';
import 'package:cnn_classification/myhomepage.dart';
import 'package:flutter/material.dart';

class MenuBarre extends StatelessWidget {
  const MenuBarre({Key? key});

  @override
  Widget build(BuildContext context) {
    return Drawer(
      backgroundColor: Colors.grey,
      child: ListView(
        children: [
          const DrawerHeader(
            decoration: BoxDecoration(
              gradient: LinearGradient(colors: [Colors.black, Colors.grey]),
            ),
            child: CircleAvatar(background

Image: AssetImage('assets/ai.jpg')),
          ),
          Column(
            children: [
              ListTile(
                title: Text('Home'),
                leading: Icon(Icons.home),
                onTap: () {
                  Navigator.push(
                    context,
                    MaterialPageRoute(builder: (context) => const MyApp()),
                  );
                },
              ),
              ExpansionTile(
                title: const Text('Chose algorithme'),
                leading: const Icon(Icons.settings),
                children: [
                  ListTile(
                    title: Text('Fashion Mnist'),
                    onTap: () {
                      Navigator.push(
                        context,
                        MaterialPageRoute(builder: (context) => const LoadImage2()),
                      );
                    },
                  ),
                  ListTile(
                    title: Text('Waste Classification'),
                    onTap: () {
                      Navigator.push(
                        context,
                        MaterialPageRoute(builder: (context) => const LoadImage()),
                      );
                    },
                  )
                ],
              )
            ],
          )
        ],
      ),
    );
  }
}
```

1. **`import 'package:cnn_classification/loadimage.dart';`...**: Importe les classes nécessaires depuis d'autres fichiers.

2. **`class MenuBarre extends StatelessWidget {`**: Définit la classe `MenuBarre`, un widget sans état.

3. **`const MenuBarre({Key? key});`**: Constructeur de `MenuBarre`.

4. **`@override Widget build(BuildContext context) {`**: Implémentation de la méthode `build` qui retourne la structure du widget.

5. **`return Drawer(`**: Crée un widget Drawer.

### `return Drawer` :

5.1. **Contexte :**
   - Utilisé pour créer un volet latéral (tiroir) qui s'ouvre depuis le bord gauche de l'écran.

5.2. **Emplacement :**
   - Souvent utilisé comme contenu du paramètre `drawer` dans un widget `Scaffold`.


7. **`backgroundColor: Colors.grey,`**: Définit la couleur de fond du tiroir.

8. **`child: ListView(`**: Crée une liste d'éléments dans le tiroir.

9. **`const DrawerHeader(`**: En-tête du tiroir avec une image.

10. **`CircleAvatar(backgroundImage: AssetImage('assets/ai.jpg')),`**: Affiche une image dans l'en-tête.

11. **`),`**: Fermeture de l'en-tête.

12. **`Column(`**: Crée une colonne d'éléments dans le tiroir.

13. **`ListTile(`**: Élément du tiroir pour la page d'accueil.

14. **`ExpansionTile(`**: Élément du tiroir pour choisir un algorithme.

15. **`ListTile(`**: Sous-élément pour Fashion Mnist.

16. **`ListTile(`**: Sous-élément pour Waste Classification.

17. **`),`**: Fermeture du tiroir.

### loadimage.dart et loadimage2.dart:

Ces fichiers contiennent des classes qui permettent à l'utilisateur de sélectionner une image à partir de la galerie, de charger un modèle TensorFlow Lite, d'effectuer des prédictions et d'afficher les résultats.

Ces classes sont assez similaires, mais `loadimage2.dart` utilise un autre modèle TensorFlow Lite et des labels différents pour la classification.

Chaque fichier a une structure similaire :

1. Importations nécessaires.
2. Définition de la classe d'état (qui étend `StatefulWidget`).
3. Méthodes d'initialisation (`initState`), de chargement du modèle (`loadmodel`), de sélection d'image (`_pickImage`), de détection d'image (`detectimage`), et de libération des ressources (`dispose`).
4. Méthode `build` pour définir l'interface utilisateur.
5. L'utilisation du package `tflite_v2` pour charger le modèle et effectuer des prédictions sur une image.

Les commentaires dans le code fournissent des informations supplémentaires sur les différentes parties du code. Notez que la fonction `_pickImage` utilise le plugin `image_picker` pour sélectionner une image à partir de la galerie.

### Classe `LoadImage` (loadimage.dart) :

```dart
class LoadImage extends StatefulWidget {
  const LoadImage({Key? key}) : super(key: key);

  @override
  State<LoadImage> createState() => _LoadImageState();
}
```

- **Ligne 1-7 :** Définition de la classe `LoadImage` qui étend `StatefulWidget`.

```dart
class _LoadImageState extends State<LoadImage> {
  final ImagePicker _picker = ImagePicker();
  File? file;
  var outputs;
  var v = "";
  bool imageSelected = false;
```

- **Ligne 9-16 :** Déclaration de la classe `_LoadImageState` qui étend `State` de `LoadImage`. Initialisation de variables pour le plugin `image_picker`, l'image sélectionnée, les résultats de la prédiction, une chaîne pour la visualisation, et un indicateur d'image sélectionnée.

```dart
  @override
  void initState(){
    super.initState();
    loadmodel().then((value){
      setState(() {
        
      });
    });
  }
```

- **Ligne 18-25 :** La méthode `initState` est appelée lors de la création du widget. Elle initialise le modèle TensorFlow Lite en appelant la méthode `loadmodel`.

```dart
  Future<void> loadmodel() async{
      String res;
      res = (await Tflite.loadModel(
        model: "assets/model.tflite",
        labels: "assets/labels.txt",
      ))!;
      print("Model loading status : ${res}");
  }
```

- **Ligne 27-38 :** La méthode `loadmodel` utilise le plugin `tflite_v2` pour charger le modèle TensorFlow Lite à partir du fichier `.tflite` et les fichiers de labels à partir de `labels.txt`.

```dart
  Future<void> _pickImage() async{
    try{
      final XFile? image = await _picker.pickImage(source: ImageSource.gallery);
      if(image == null) return;
      setState(() {
        file = File(image.path);
        imageSelected = true;
      });
      await detectimage(file!);
      print('Image picked');
    }catch(e){
      print('Error picking image : $e');
    }
  }
```

- **Ligne 40-68 :** La méthode `_pickImage` utilise le plugin `image_picker` pour permettre à l'utilisateur de sélectionner une image depuis la galerie. Une fois l'image sélectionnée, la méthode `detectimage` est appelée pour effectuer des prédictions.

```dart
  Future<void> detectimage(File image) async {
    int startTime = DateTime.now().millisecondsSinceEpoch;
    var predictions = await Tflite.runModelOnImage(
      path: image.path,
      numResults: 1,
      threshold: 0.05,
      imageMean: 127.5,
      imageStd: 127.5,
    );
    setState(() {
      outputs = predictions;
      v = predictions.toString();
    });
    print("Output Shape: ${predictions![0]['shape']}"); 
    print("//////////////////////////////////////////////////");
    print(predictions);
    // print(dataList);
    print("//////////////////////////////////////////////////");
    int endTime = DateTime.now().millisecondsSinceEpoch;
    print("Inference took ${endTime - startTime}ms");

  }
```

- **Ligne 70-96 :** La méthode `detectimage` prend le chemin de l'image sélectionnée, utilise TensorFlow Lite pour effectuer des prédictions, et met à jour l'état du widget avec les résultats de la prédiction.
- Cette partie du code utilise le plugin `tflite_v2` dans Flutter pour effectuer une prédiction à l'aide d'un modèle TensorFlow Lite sur une image donnée. Voici une explication détaillée des paramètres utilisés dans la méthode `Tflite.runModelOnImage` :

```dart
var predictions = await Tflite.runModelOnImage(
  path: image.path,    // Chemin vers le fichier de l'image sur lequel effectuer la prédiction.
  numResults: 1,        // Nombre de résultats à retourner. Dans cet exemple, on veut la meilleure prédiction.
  threshold: 0.05,      // Seuil de confiance pour filtrer les prédictions dont la probabilité est inférieure à 0.05.
  imageMean: 127.5,     // Moyenne des valeurs des pixels pour normaliser l'image avant la prédiction.
  imageStd: 127.5,      // Écart type des valeurs des pixels pour normaliser l'image avant la prédiction.
);
```

Explication détaillée :

1. **`path: image.path` :**
   - `path` est le chemin vers le fichier image sur lequel vous souhaitez effectuer la prédiction.
   - `image.path` est utilisé pour obtenir le chemin du fichier de l'image sélectionnée précédemment.

2. **`numResults: 1` :**
   - `numResults` spécifie le nombre de résultats que vous souhaitez obtenir. Dans cet exemple, on demande une seule prédiction, c'est-à-dire la classe avec la probabilité la plus élevée.

3. **`threshold: 0.05` :**
   - `threshold` est un seuil de confiance. Les prédictions dont la probabilité est inférieure à ce seuil seront filtrées. Dans cet exemple, seules les prédictions avec une probabilité supérieure à 0.05 seront considérées.

4. **`imageMean: 127.5` et `imageStd: 127.5` :**
   - Ces paramètres sont utilisés pour normaliser les valeurs des pixels de l'image avant de les fournir au modèle pour la prédiction. La normalisation est souvent nécessaire pour que les données d'entrée soient dans la plage attendue par le modèle.

En résumé, cette ligne de code effectue une prédiction sur l'image spécifiée en utilisant un modèle TensorFlow Lite. Les résultats de la prédiction, c'est-à-dire les classes prédites et leurs probabilités associées, sont stockés dans la variable `predictions`. Les paramètres tels que le seuil de confiance, la normalisation des pixels, etc., sont utilisés pour configurer le processus de prédiction.

```dart
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        backgroundColor: Theme.of(context).colorScheme.inversePrimary,
        title: const Text('Waste Image Clasification'),
      ),
      drawer: const MenuBarre(),
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: <Widget>[
            file != null 
            ? Image.file(
            file!,
            height: 200,
            width: 200,
            ) : const Text('No image selected'),
            const SizedBox(height: 20),
            outputs != null && outputs!.isNotEmpty ?
            Text(outputs![0]['label'].toString().substring(2),style: const TextStyle(color: Colors.red),) : const Text(''),
          ],
        ),
      ),
      floatingActionButton: FloatingActionButton(
        onPressed: () {
          _pickImage();
        },
        tooltip: 'Pick Image from Gallery',
        child: const Icon(Icons.image),
      ),
    );
  }

  @override
  void dispose() {
    // Unload the model when the state is disposed
    Tflite.close();
    super.dispose();
  }
}
```

- **Ligne 98-127 :** La méthode `build` crée l'interface utilisateur de la page. Elle comprend un `Scaffold` avec une barre d'applications, un corps qui affiche l'image sélectionnée et le résultat de la prédiction, et un bouton flottant pour sélectionner une nouvelle image.

### Classe `LoadImage2` (loadimage2.dart) :

Les explications pour `LoadImage2` sont très similaires à `LoadImage`, avec des différences mineures liées à l'utilisation d'une méthode différente pour effectuer la prédiction, notamment la manipulation d'images pour redimensionner l'image à 28x28 pixels.

Je vais résumer ces différences :

- La méthode `detectimage` dans `LoadImage2` utilise la manipulation d'images pour redimensionner l'image à 28x28 pixels avant d'effectuer la prédiction avec TensorFlow Lite.

- La classe `LoadImage2` utilise un modèle TensorFlow Lite différent (`model2.tflite`) avec un fichier de labels différent (`labels2.txt`).

Le reste de la structure et des fonctionnalités est similaire à `LoadImage`.

En résumé, ces classes permettent d'interagir avec des modèles TensorFlow Lite pour la classification d'images à partir de sélections d'images. Le fichier `loadimage.dart` utilise un modèle et des labels spécifiques, tandis que `loadimage2.dart` utilise une configuration différente.
