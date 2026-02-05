# Calculator Taxe PFA

Un calculator online pentru calcularea taxelor pentru PFA (Persoană Fizică Autorizată) în România.

## 🚀 Tehnologii

- [Astro](https://astro.build) - Framework modern pentru site-uri statice
- TypeScript - Tipuri statice pentru JavaScript
- Vercel - Platformă de deployment

## 📋 Funcționalități

- ✅ Calcul automat al taxelor PFA conform legislației 2025-2026
- ✅ Calcul CAS (25%) - datorat peste 12 SM, plafonat la 24 SM
- ✅ Calcul CASS (10%) - minim 6 SM pentru nesalariați, proporțional 6-60 SM, plafon 60 SM
- ✅ Calcul Impozit pe venit (10%) - aplicat pe baza: venit net - CAS - CASS
- ✅ Suport pentru anii 2025 și 2026 (cu salarii minime diferite)
- ✅ Opțiune pentru statut salariat (afectează calculul CASS sub 6 SM)
- ✅ Calcul venit net (venit brut - cheltuieli deductibile)
- ✅ Afișare detalii despre praguri și plafonări
- ✅ Rata efectivă de impozitare
- ✅ Interfață modernă și responsive
- ✅ Calcule în timp real

## 🛠️ Instalare

```bash
npm install
```

## 🏃 Development

```bash
npm run dev
```

Aplicația va rula la `http://localhost:4321`

## 📦 Build

```bash
npm run build
```

## 🚢 Deployment pe Vercel

1. Conectează repository-ul Git cu Vercel
2. Vercel va detecta automat configurația din `vercel.json`
3. Build-ul se va face automat la fiecare push

Sau folosește CLI-ul Vercel:

```bash
npm i -g vercel
vercel
```

## 📊 Cum funcționează

Calculatorul calculează taxele conform legislației în vigoare:

1. **Venit Net** = Venit Brut - Cheltuieli Deductibile
2. **CAS (25%)** - datorat doar peste 12 salarii minime, plafonat la 24 salarii
3. **CASS (10%)** - minim 6 SM pentru nesalariați, proporțional 6-60 SM, plafon 60 SM
4. **Impozit (10%)** - aplicat pe baza: venit net - CAS - CASS (nu poate fi negativă)

### Praguri 2026:
- 6 SM = 24.300 RON (minim CASS pentru nesalariați)
- 12 SM = 48.600 RON (prag minim CAS)
- 24 SM = 97.200 RON (plafon CAS)
- 60 SM = 243.000 RON (plafon CASS)

### Praguri 2025:
- 6 SM = 19.800 RON
- 12 SM = 39.600 RON
- 24 SM = 79.200 RON
- 60 SM = 198.000 RON

## 📝 Notă

Acest calculator oferă estimări bazate pe legislația în vigoare. Pentru calcule exacte și consultanță fiscală, consultă un contabil autorizat.

## 📄 Licență

MIT
