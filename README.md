# JAVA_IHMS2
Une autre version d'IHMs en Java.
- ConsoleIhmImpl et JPanelIhmImpl;


- des classes spécialisées dans les menus;

![Menu Screen 1](./hcmenu01.png?raw=true "Menu en  mode console")
![Menu Screen 2](./hcmenu02.png?raw=true "Menu en  mode Jpanel")


- des classes spécialisées dans l'affichage des tableaux;
 
 ![Tableau Screen 1](./hc01.png?raw=true "Tableau en  mode console")
 ![Tableau Screen 2](./hc02.png?raw=true "Tableau en  mode Jpanel")


#Exemples d'utilisation:
<code lang='java'>
 
 // Donnera un tableau dans une vue JPanel:
 
        String titreTableau="Les élèves";

        String[] tabEntetes={"Nom","Prénom","age","NIA"};

        String[][] tabDonnees= {
                {"MENVUSSA", "Gérard", "45","1234567"},
                {"TERIEUR", "Alexandre"},
                {"TERIEUR", "Alain", "26","F252525"},
                {"OCHON", "Paul", "19"}
        };

        TypeAlignement[] tabTa={TypeAlignement.LEFT,TypeAlignement.CENTER,TypeAlignement.CENTER,TypeAlignement.LEFT};

        //Affichage du contenu du tableau
        Ihm vue = FabriqueIhm.creerIhm(TypeIhm.JPANEL);

        try {
            //Affichage avec colonne NO
            vue.afficherTableau(titreTableau, tabEntetes, tabDonnees, tabTa, true);

            //ou Affichage sans colonne NO
            vue.afficherTableau(titreTableau,tabEntetes,tabDonnees,tabTa,false);
        }catch(Exception ex){
            ex.printStackTrace();
        }
 
 
 //pour obtenir un affichage dans la console, il suffira la ligne Ihm vue=...  par Ihm vue = FabriqueIhm.creerIhm(TypeIhm.CONSOLE);

 </code>

Exemple de création d'un menu mode console:

![Menu console Screen 1](./hcmenu_console01.PNG?raw=true "Menu en  mode console")

