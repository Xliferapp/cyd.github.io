================================================================================
  CYD GitHub Pages — avtomatski prehod na tunel
================================================================================

1) Firebase (enkrat)
   - console.firebase.google.com → nov projekt
   - Build → Realtime Database → Create (Europe)
   - Rules:

     {
       "rules": {
         "cyd": {
           "live": {
             ".read": true,
             ".write": true
           }
         }
       }
     }

   - Skopiraj URL baze (npr. https://xxx-default-rtdb.europe-west1.firebasedatabase.app)

2) Vpiši URL v DVE datoteki (isti naslov):
   - cyd-github/firebase-public.js     (ta repo / GitHub Pages)
   - cyd-server/firebase-tunnel.json   (tvoj PC — tunel sem piše)

3) GitHub
   - nov repo, vanj daj vsebino mape cyd-github (index.html + firebase-public.js)
   - Settings → Pages → Deploy from branch → main /
   - Javni link: https://TVOJUSER.github.io/TVOJREPO/

4) Zagon doma
   - start.bat → S
   - tunnel.bat  (ali start.bat → 2 → 1)
   - ko se izpiše trycloudflare URL, se SAM pošlje v Firebase
   - kdo odpre GitHub stran, ga preusmeri na ta URL

Quick Tunnel se ob vsakem zagonu spremeni. GitHub link ostane isti.
================================================================================
