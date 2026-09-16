# eex_cron

Spúšťač pre súkromné repo [`mizitean/eex_data`](https://github.com/mizitean/eex_data).

Neobsahuje dáta ani kód — len cron, ktorý raz denne zavolá `workflow_dispatch`
na súkromnom repe. Dôvod: scheduled workflow sa na súkromnom repe nemusí
spustiť, kým vo verejnom beží spoľahlivo a bez limitu minút.

Minúty sa míňajú súkromnému repu, tu sa spotrebuje pár sekúnd denne.

## Nastavenie

Secret `EEX_TOKEN` = fine-grained PAT s právom **Actions: write** výlučne na
`mizitean/eex_data`. Žiadne iné právo a žiadne iné repo.
