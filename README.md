Consignes :

- Creer une classe , Créer au moins deux traits dans des fichiers séparés, incluez le tout.
- Faire en sorte que votre classe utilise les traits que vous avez créé
- Experimentez, testez ...



Théorie :

En PHP orienté Objet, les traits permettent de définir des méthodes communes à plusieurs classes.

Les traits sont surtout utiles pour outrepasser les limites de l'héritage ( une classe ne peut hériter que d'une seule classe )

Grâce aux traits, une classe peut utiliser des méthodes de plusieurs traits différents.

La syntaxe est la suivante :

// Definir un trait
trait monTrait
{
    public function doStuff()
    {
    echo"Doing stuff";
    }

    public function doStuff2()
    {
    echo"Doing stuff2";
    }


}

class maClasse
{
use monTrait;
}

$test = new maClasse();
$test->doStuff();
// Affichera Doing Stuff


Utiliser plusieurs traits différent dans la même classe

trait monTrait1
{
    public function doSomething()
    {
    echo"Doing something";
    }
}

trait monTrait2
{
    public function doSomething2()
    {
    echo"Doing something 2";
    }
}

class maClasse
{
use monTrait1, monTrait2;
}

$test = new maClasse();
$test->doSomething();
// Affichera Doing something

$test->doSomething2();
// Affichera Doing something 2


Documentation sur php.net ( Lecture vivement recommandée ) :

http://php.net/manual/fr/language.oop5.traits.php