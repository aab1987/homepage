
## Ogó³y 

Git to system kontroli wersji. 
Bêdzie pomocny przy wspo³tworzeniu projektu przez kilka osób np. przy tworzeniu strony internetowej, aplikacji webowej, aplikacji mobinej. 
Ka¿dy wrzuca swój kod do repozytorium (takiej jakby przechowalni kodu) a nastêpnie udostêpnia to repozytorium (jeœli jest publiczne) innym przez stronê np. github.com lub bitbucket.org. Wtedy reszta ma wgl¹d do naszego kodu i mo¿e go edytowaæ.

## Od czego zacz¹æ... 

uruchamiamy gita
i wpisujemy komendy (wa¿ne jest to, ¿eby wpisywaæ dok³adnie, czyli tam gdzie spacja to spacja, gdzie 2 kropki to 2 kropki itd. ;) ka¿d¹ 

komendê koñczymy klikaj¹c enter) :

    git config --global user.name "Twoje imiê"  


    git config --global user.email "Twoj_email"

s³u¿¹ one naszej identyfikacji

mo¿emy sprawdziæ ustawienia wpisuj¹c:

    git config --list

Teraz tworzymy plik z nasz¹ stron¹ internetow¹, np. index.html i zapisujemy na dysku.

Inicjalizujemy nasze pierwsze repozytorium wpisuj¹c

    git init

a nastepnie dodajemy nasz plik index.html

    git add index.html

wykonujemy commit, czyli zatwierdzamy zmiany

    git commit -m "tu piszemy komentarz, np. pierwszy commit"

Je¿eli siê pomylimy i zorientujemy przed wykonaniem komendy "add" i "commit" to mo¿emy porzuciæ zmiany przy pomocy polecenia 

    git checkout index.html - po takim poleceniu zawartoœæ pliku index.html bêdzie taka jak w ostatnim znanym commicie. 

Historiê commitów sprawdzamy:

    git log


## GITHUB.COM : 

Aby móc ³¹czyæ siê z githubem potrzebujemy wygenerowaæ klucz ssh.

Wpisujemy:

    ssh-keygen -t rsa -C "Twoj_email@email.com"

Pojawia nam siê info gdzie mamy ten wygenerowany klucz.

Wchodzimy teraz na stornê github.com, tworzymy sobie konto.

W menu Account Settings (prawy górny róg-ikonka klucza p³askiego) wybieramy SSH KEYS --> ADD SSH KEY --> wklejamy tekst z id_rsa.pub 

(wa¿ne- ten z rozszerzeniem .pub ). Nadajemy jakiœ tytu³ i zapisujemy.

Wracamy do naszego terminala i wpisujemy:
   
    ssh -T git@github.com

Ponownie wchodzimy na g³ówn¹ stronê github.com ( przyciskiem home jest tu oœmiornicokotek - lewy górny róg) i klikamy New 

repository,tworzymy jakieœ.

Teraz wpisujemy w terminalu: 

    git remote add origin git@github.com:twojlogin/nazwa_repozytorium.git

And the last one:

    git push -u origin master




Mo¿emy klonowaæ repezytoria kole¿anek i kolegów. A robimy to tak:

klikamy nazwê u¿ytkownika, np. szemek. Wchodzimy w zak³adkê Repositories, nastêpnie klikamy jakiekolwiek repozytorium i wtedy po prawej 

stronie mamy : You can clone with... zaznaczamy SSH i klonujemy.



Przydatne:
http://blog.piotrnalepa.pl/2013/05/19/git-podreczny-zestaw-niezbednych-komend-dla-kazdego-webdevelopera-i-nie-tylko/
 