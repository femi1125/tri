Algorithme trierTabNombres
Variable
    tab: tableau
      n, i, j, temp, max, min: entier
Début

  Écrire("Vous souhaitez entrer combien de nombres ?")
    Lire(n)

  Pour i de 1 à n faire
        Écrire("Entrez le nombre ", i, " : ")
        Lire(tab[i])
    FinPour

   max <- tab[1]
   min <- tab[1]

  Pour i de 2 à n faire
        Si tab[i] > max alors
            max <- tab[i]
        FinSi
        Si tab[i] < min alors
            min <- tab[i]
        FinSi
    FinPour

   Pour i de 1 à n-1 faire
        Pour j de 1 à n-i faire
            Si tab[j] > tab[j+1] alors
                temp <- tab[j]
                tab[j] <- tab[j+1]
                tab[j+1] <- temp
            FinSi
        FinPour
    FinPour

  Écrire("Le maximum est : ", max)
    Écrire("Le minimum est : ", min)
    Écrire("Tableau trié par ordre croissant : ")
    Pour i de 1 à n faire
        Écrire(tab[i])
    FinPour

Fin
