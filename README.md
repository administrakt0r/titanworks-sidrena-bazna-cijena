# Titanworks Bazna Cijena

<img src=".github/readme-banner.svg" alt="Titanworks Bazna Cijena: sidrena cijena, najniža cijena u 30 dana i javni cjenici" width="100%">

WordPress dodatak za hrvatske trgovce: evidencija i prikaz sidrene cijene,
izračun najniže cijene u prethodnih 30 dana za posebne oblike prodaje te dnevni
CSV i XML cjenici po prodajnom mjestu. Radi s WooCommerceom ili s ugrađenim
samostalnim katalogom.

[Preuzmi titanworks-bazna-cijena.zip](https://github.com/administrakt0r/titanworks-sidrena-bazna-cijena/releases/latest/download/titanworks-bazna-cijena.zip) · [Sva izdanja](https://github.com/administrakt0r/titanworks-sidrena-bazna-cijena/releases) · [Web-stranica](https://sidrenacijena.eu/) · [Demo trgovina](https://wordpress.sidrenacijena.eu/)

## Instalacija

1. Preuzmite ZIP s gornje poveznice.
2. U WordPressu otvorite **Dodaci → Dodaj novi dodatak → Učitaj dodatak**,
   odaberite `titanworks-bazna-cijena.zip` i instalirajte ga.
3. Aktivirajte **Titanworks Bazna Cijena**.
4. U izborniku **Sidrena cijena → Postavke** provjerite referentne datume i
   način prikaza. Unesite prodajna mjesta te evidentirajte ili uvezite
   potkrijepljene povijesne cijene.
5. Izradite cjenik i provjerite javni prikaz i arhivu prije oslanjanja na
   automatsku objavu.

Paket sadrži mapu `titanworks-bazna-cijena/` s datotekama dodatka.
Pri nadogradnji zadržite isti naziv mape kako WordPress ne bi prepoznao
zasebnu instalaciju. Ako ste starije izdanje instalirali pod nazivom
`sidrena-cijena-eu`, prvo napravite sigurnosnu kopiju i provjerite postupak
zamjene na testnoj instalaciji.

## Što dodatak radi

- Bilježi sidrene cijene, izvore, autore i razloge ispravaka uz trajnu povijest.
- Prikazuje aktualnu i sidrenu cijenu uz proizvode i WooCommerce varijacije.
- Zasebno računa najnižu cijenu u prethodnih 30 dana za evidentirane posebne
  oblike prodaje. Sidrena cijena i najniža cijena u 30 dana imaju odvojene uloge.
- Izrađuje dnevne CSV i XML cjenike za svako prodajno mjesto, s provjerom
  podataka, kontrolnim sumama i arhivom objava.
- Nudi javni cjenik s pretraživanjem, arhivu te JSON, CSV i XML sučelja.
- Uvozi CSV uz pregled prije potvrde te prikazuje nalaze provjera i povijest cijena.

Nedostajuće povijesne cijene morate potkrijepiti i unijeti. Dodatak može
zabilježiti stvarno viđenu prvu ponudu pri objavi novog proizvoda.

## Zahtjevi

| Komponenta | Najmanja verzija |
| --- | --- |
| WordPress | 6.8 |
| PHP | 7.4 |
| MySQL / MariaDB | 5.7 / 10.4 |
| WooCommerce | 8, ako koristite integraciju |

## Prikaz na stranicama

Umetnite shortcode u sadržaj WordPress stranice:

| Shortcode | Prikaz |
| --- | --- |
| `[twbce_cijena product_id="123"]` | Cijene proizvoda s ID-jem 123 |
| `[twbce_cjenik]` | Javni cjenik s pretraživanjem i straničenjem |
| `[twbce_arhiva]` | Arhiva objavljenih cjenika |

Od izdanja 2.0.26 stranice s oznakama `[sidrena-cjenik]` i `[sidrena-arhiva]`
treba ažurirati na `[twbce_cjenik]` i `[twbce_arhiva]`.

REST sučelja koriste prefiks `/wp-json/sidrena-cijena/v1/`:

| GET ruta | Sadržaj |
| --- | --- |
| `prices` | Aktualni cjenik u JSON-u |
| `prices.csv` | CSV cjenik |
| `prices.xml` | XML cjenik |
| `publications` | Popis objavljenih cjenika |
| `status` | Status dodatka; potrebna je prijava i dozvola |

Za provjeru podataka i ručnu objavu putem WP-CLI-ja:

```bash
wp sidrena-cijena status
wp sidrena-cijena validate
wp sidrena-cijena generate --force
```

## Izdanja i provjera preuzimanja

Ovaj repozitorij sadrži instalacijske pakete i kontrolne sume. Najnovije izdanje
je [2.0.42](https://github.com/administrakt0r/titanworks-sidrena-bazna-cijena/releases/tag/v2.0.42).
Popis izmjena nalazi se u bilješkama izdanja i u `readme.txt` unutar paketa.

Svaka mapa u `versions/` sadrži `titanworks-bazna-cijena.zip` i `SHA256SUMS.txt`.
Preuzmite obje datoteke iz istog izdanja i provjerite ih u istoj mapi:

```bash
sha256sum -c SHA256SUMS.txt
```

Povijesnim paketima preimenovana je korijenska mapa u `titanworks-bazna-cijena/`.
Datoteke dodatka zadržale su isti sadržaj, a kontrolne sume paketa ažurirane su.
GitHubove automatske poveznice **Source code** preuzimaju ovaj repozitorij;
za instalaciju odaberite priloženi `titanworks-bazna-cijena.zip`.

## Objavljeni podaci i odgovornost trgovca

Cjenici, adrese prodajnih mjesta i javna sučelja dostupni su bez prijave.
U katalog i dokaze unosite podatke namijenjene objavi, bez podataka o kupcima.
Dodatak obrađuje cijene i izrađuje datoteke na vašoj WordPress instalaciji;
ne šalje podatke kataloga ni telemetriju vanjskim servisima.

Trgovac odgovara za unesene cijene, datume i klasifikaciju posebnih oblika
prodaje. Dodatak je tehnička pomoć, a ne pravni savjet ili jamstvo usklađenosti.

## Podrška i licenca

Problem prijavite kroz [GitHub Issues](https://github.com/administrakt0r/titanworks-sidrena-bazna-cijena/issues).
Navedite verzije dodatka, WordPressa i PHP-a te korake za ponavljanje problema.
Iz prijave uklonite lozinke, tokene i osobne podatke.

Licenca: [GPL-2.0-or-later](https://www.gnu.org/licenses/gpl-2.0.html).
