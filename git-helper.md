# Cloning

  >> git clone <copy-repo-link-from-github>
  
# Commiting
  
  >> git status - shows all files that are updated or created or deleted, but not yet COMMITED
    (MODIFIED - modifikovano, UNTRACKED - novi -> git ne zna da postoje)
 
  >> git add <file-name>  - stage-uje samo naveden fajl
  >> git add .            - stage-uje sve modifikovane i sve nepracene fajlove
  
  >> git commit -m "poruka" -m "some description" - lokalni komit
  
  >> git push - pushuje komit na remote repository
  
# SSH Keys - povezivanje lokalne masine i git naloga
  
  >> ssh-keygen -t rsa -b 4096 -C "email.koji.koristis@gitnalog.tvoj"
  
  - Kljuc ce biti sacuvan na "Users/{active-user}/.ssh/id_rsa
  - Unosis ime fajla ako zelis da se zove drugacije od "id_rsa"
  
  - cd u taj direktorijum
  
  - testkey (privatni kljuc koji cuvam na lokalnom racunaru)
  - testkey.pub => uploadujem na git interfejs (public key)