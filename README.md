# TP 3 - Les Formulaires en Symfony

## Description

Page produit (Premium Wireless Headphones) avec formulaire d'ajout au panier utilisant Symfony Form Component et personnalisation Twig.

## Ce que j'ai fait

**1. Form Type (ProductType.php)**
- Créé un formulaire avec 2 champs : quantité (IntegerType) et couleur (ChoiceType)
- Utilisé la syntaxe PHP avec paramètres nommés (`child:`, `type:`, `options:`)
- Ajouté `declare(strict_types=1);` pour le typage strict

**2. Controller (ProductController.php)**
- Route `/` avec attribut PHP 8 : `#[Route(name: 'app_product', path: '/')]`
- Création et passage du formulaire à la vue

**3. Template (product/index.html.twig)**
- Affichage des informations produit et du formulaire
- Application du thème personnalisé avec `{% form_theme form with [...] %}`

**4. Form Theme (custom_product_theme.html.twig)**
- Personnalisé l'affichage des champs avec blocks Twig spécifiques
- Appliqué les classes Bootstrap (form-control, form-select)
- Utilisé les fonctions `form_label()`, `form_widget()`, `form_errors()`

