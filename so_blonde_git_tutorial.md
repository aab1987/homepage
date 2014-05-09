
## Og�y 

Git to system kontroli wersji. 
B�dzie pomocny przy wspo�tworzeniu projektu przez kilka os�b np. przy tworzeniu strony internetowej, aplikacji webowej, aplikacji mobinej. 
Ka�dy wrzuca sw�j kod do repozytorium (takiej jakby przechowalni kodu) a nast�pnie udost�pnia to repozytorium (je�li jest publiczne) innym przez stron� np. github.com lub bitbucket.org. Wtedy reszta ma wgl�d do naszego kodu i mo�e go edytowa�.

## Od czego zacz��... 

uruchamiamy gita
i wpisujemy komendy (wa�ne jest to, �eby wpisywa� dok�adnie, czyli tam gdzie spacja to spacja, gdzie 2 kropki to 2 kropki itd. ;) ka�d� 

komend� ko�czymy klikaj�c enter) :

    git config --global user.name "Twoje imi�"  


    git config --global user.email "Twoj_email"

s�u�� one naszej identyfikacji

mo�emy sprawdzi� ustawienia wpisuj�c:

    git config --list

Teraz tworzymy plik z nasz� stron� internetow�, np. index.html i zapisujemy na dysku.

Inicjalizujemy nasze pierwsze repozytorium wpisuj�c

    git init

a nastepnie dodajemy nasz plik index.html

    git add index.html

wykonujemy commit, czyli zatwierdzamy zmiany

    git commit -m "tu piszemy komentarz, np. pierwszy commit"

Je�eli si� pomylimy i zorientujemy przed wykonaniem komendy "add" i "commit" to mo�emy porzuci� zmiany przy pomocy polecenia 

    git checkout index.html - po takim poleceniu zawarto�� pliku index.html b�dzie taka jak w ostatnim znanym commicie. 

Histori� commit�w sprawdzamy:

    git log


## GITHUB.COM : 

Aby m�c ��czy� si� z githubem potrzebujemy wygenerowa� klucz ssh.

Wpisujemy:

    ssh-keygen -t rsa -C "Twoj_email@email.com"

Pojawia nam si� info gdzie mamy ten wygenerowany klucz.

Wchodzimy teraz na storn� github.com, tworzymy sobie konto.

W menu Account Settings (prawy g�rny r�g-ikonka klucza p�askiego) wybieramy SSH KEYS --> ADD SSH KEY --> wklejamy tekst z id_rsa.pub 

(wa�ne- ten z rozszerzeniem .pub ). Nadajemy jaki� tytu� i zapisujemy.

Wracamy do naszego terminala i wpisujemy:
   
    ssh -T git@github.com

Ponownie wchodzimy na g��wn� stron� github.com ( przyciskiem home jest tu o�miornicokotek - lewy g�rny r�g) i klikamy New 

repository,tworzymy jakie�.

Teraz wpisujemy w terminalu: 

    git remote add origin git@github.com:twojlogin/nazwa_repozytorium.git

And the last one:

    git push -u origin master




Mo�emy klonowa� repezytoria kole�anek i koleg�w. A robimy to tak:

klikamy nazw� u�ytkownika, np. szemek. Wchodzimy w zak�adk� Repositories, nast�pnie klikamy jakiekolwiek repozytorium i wtedy po prawej 

stronie mamy : You can clone with... zaznaczamy SSH i kopiujemy i potem klonujemy przy pomocy komendy: 

    git clone "i tutaj wklejamy lub przepisujemy(na windowsie;)) adres repozytorium"



Przydatne:
http://blog.piotrnalepa.pl/2013/05/19/git-podreczny-zestaw-niezbednych-komend-dla-kazdego-webdevelopera-i-nie-tylko/
 