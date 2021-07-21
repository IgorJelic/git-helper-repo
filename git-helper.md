# Cloning

  - ~ git clone "copy-repo-link-from-github"
  
# Existing local repository
  
  - >> git init - unutar odabranog repoa
  
  - >> git add .
  - >> git commit -m "poruka1" -m "opis"
  
  - napravim prazan repo na githubu
  
  - >> git remote add origin <link-sa-githuba>
  - >> git remote -v => proveravam konektovane remote repozitorijume
  
  - >> git push -u origin master => -u znaci "upstream" => svaki sledeci put kucam samo "git push" a sve posle -u se podrazumeva
  - >> git push
  
# Commiting
  
  - >> git status - shows all files that are updated or created or deleted, but not yet COMMITED
    (MODIFIED - modifikovano, UNTRACKED - novi -> git ne zna da postoje)
 
  - >> git add <file-name>  - stage-uje samo naveden fajl
  - >> git add .            - stage-uje sve modifikovane i sve nepracene fajlove
  
  - >> git commit -m "poruka" -m "some description" - lokalni komit
    
# Push
  
  - >> git push origin master - pushuje komit na "master" granu
  
# Branching
  
  
  
# SSH Keys - povezivanje lokalne masine i git naloga
  
  - >> ssh-keygen -t rsa -b 4096 -C "email.koji.koristis@gitnalog.tvoj"
  
  - Kljuc ce biti sacuvan na "Users/{active-user}/.ssh/id_rsa
  - Unosis ime fajla ako zelis da se zove drugacije od "id_rsa"
  
  - cd u taj direktorijum
  
  - testkey (privatni kljuc koji cuvam na lokalnom racunaru)
  - testkey.pub => 
            otvorim: cat testkey.mb
            uploadujem na git interfejs (public key)
