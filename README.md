# edu-git

## Skapa gitlek i github (Ta bort gammal om det finns)

> gitlek ska ha README.md, inget annat.

```bash
git clone https://github.com/[ANVÄNDARE]/gitlek.git gitlek1
git clone https://github.com/[ANVÄNDARE]/gitlek.git gitlek2
```
## Ändra README.md i github

```bash
cd gitlek1
echo -e "\n## Ändrat i gitlek 1" >> README.md
git add .
git commit -m "Ändrat i gitlek1"
cd ..


cd gitlek2
echo -e "\ntext" >> README.md
git add .
git commit -m "Ändrat i gitlek2"
cd ..

cd gitlek1
git fetch
git merge
echo -e "\n## Ändrat i gitlek 2" >> README.md
git add .
git commit -m "Merged"
cd ..

cd gitlek2
git fetch
git rebase
vi README.md #Ta bort konflikter
git add .
git rebase --continue
git push
cd ..

cd gitlek1
git fetch
git merge

git push
```
