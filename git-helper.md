# Cloning

  - ~ git clone "copy-repo-link-from-github"
  
# Existing local repository
  
  - ~ git init - unutar odabranog repoa
  
  - ~ git add .
  - ~ git commit -m "poruka1" -m "opis"

  - U slucaju kada modifikujemo postojeci, vec komitovani fajl, moze skracenica koja menja prethodna dva poziva: ~ git commit -am "poruka"
  
  - napravim prazan repo na githubu
  
  - ~ git remote add origin "link-sa-githuba"
  - ~ git remote -v  (proveravam konektovane remote repozitorijume)
  
  - ~ git push -u origin master => -u znaci "upstream" => svaki sledeci put kucam samo "git push" a sve posle -u se podrazumeva
  - ~ git push
  
# Commiting
  
  - ~ git status - shows all files that are updated or created or deleted, but not yet COMMITED
    (MODIFIED - modifikovano, UNTRACKED - novi, git ne zna da postoje)
 
  - ~ git add "file-name"  - stage-uje samo naveden fajl
  - ~ git add .            - stage-uje sve modifikovane i sve nepracene fajlove
  
  - ~ git commit -m "poruka" -m "some description" - lokalni komit
    
# Push
  
  - ~ git push origin master - pushuje komit na "master" granu

# Pull

  - ~ git pull origin master (git pull -u origin master)
  
# Branching
  
  - ~ git branch (shows all branches)
  - ~ git checkout -b "name-of-new-branch"
  - ~ git checkout "name-of-existing-branch"
  - ~ git diff "name-of-branch" (shows all code changes, usually called from parent to compare with child branch)
  - Kada menjamo granu na kojoj moze doci do konflikata sa izmenama na trenutnoj grani, prvo je potrebno te promene komitovati ili stashovati na trenutnoj grani, da bi uspesno izvrsili checkout
  - ~ git merge master - koristimo kada radimo na posebnom branchu, a ekipa promeni sadrzaj na master grani:
      1. pull promene na masteru
      2. ~ git merge master - poziv iz trenutne grane na kojoj radimo, da bi nasa grana bila u toku sa sadrzajem mastera

# Pull Request

  - Request to have your code pulled into another branch (from "new-feature" branch into "master" branch)
  - Na github-u se radi pull request uz komentar o konkretnom PR-u (pull request)
  - Posle pregleda pull request-a, moguce je obaviti akciju MERGE nakon koje je potrebno obrisati mergovanu granu
  - ~ git branch -d "name-of-deleting-branch"

# UNDO Actions

  - undo staging = ~ git reset
  - undo commit = ~ git reset HEAD~1 (HEAD = poslednji komit, 1 = idi u nazad za 1 komit od HEAD komita)
  - undo vise commit-a = ~ git log = pregled svih komita od poslednjeg ka prvom
      1. nadji hash kod zeljenog komita
      2. git reset "hash-code" - unstageuje sve promene do tog komita
      3. git reset --hard "hash-code" - potpuno brise sve promene sve do tog komita

# FORK Action

  - Kada nemas pristup da menjas nesto u nekom repozitorijumu, koristis FORK
  - KOPIRA NECIJI REPO na tvoj github profil, tako da imas sve dozvole modifikacije
  
  
  
# SSH Keys - povezivanje lokalne masine i git naloga
  
  - ~ ssh-keygen -t rsa -b 4096 -C "email.koji.koristis@gitnalog.tvoj"
  
  - Kljuc ce biti sacuvan na "Users/{active-user}/.ssh/id_rsa
  - Unosis ime fajla ako zelis da se zove drugacije od "id_rsa"
  
  - cd u taj direktorijum
  
  - testkey (privatni kljuc koji cuvam na lokalnom racunaru)
  - testkey.pub => 
            otvorim: cat testkey.mb
            uploadujem na git interfejs (public key)
