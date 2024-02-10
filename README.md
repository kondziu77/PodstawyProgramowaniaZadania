Zadanie 1
mkdir repo1
cd repo1
echo "pierwszy" > 1.txt
echo "drugi" > 2.txt
git init
git status
git add .
git status
git commit -m "initial commit"
git status

Zadanie 2
echo "zmieniony tekst" > 1.txt
git status
echo "zmieniony tekst" > 2.txt
git diff 2.txt
git add .
git commit -am "zmieniono zawartosc plikow"
git log

Zadanie 3
cd..
git clone repo1 repo2

Zadanie 4
cd repo2
git rm 1.txt
git mv 2.txt changed.txt
git status
git commit -am "usunieto 1 i zmieniono nazwe 2"
git log --stat

Zadanie 5
cd..
git pull repo2

Zadanie 6
echo "zmiana w repo1" > changed.txt
cd ../repo2
echo "zmiana w repo2" > changed.txt
git commit -am "zmiana w repo2"
cd ../repo1
git commit -am "zmiana w repo1"
git pull ../repo2
git add . 
git commit -m "rozwiazano konflikt"
git status
git log
cd ../repo2
git pull ../repo1

Zadanie 7
git reset --hard HEAD
git status
more changed.txt
git pull origin master
git status

Zadanie 8
git show HEAD~1:changed.txt

Zadanie 9
git diff HEAD~1 changed.txt

Zadanie 10
git branch test
git checkout test
echo "Nowa zawartość w branchu test" > plik1.txt
git commit -am "Zmiany w branchu test"
git branch
git checkout master
more plik1.txt
git status

Zadanie 11
git pull origin test
git status
git branch
git log --oneline -n 2
