# 🚀 Ghid Deployment pe Vercel

Acest ghid te ajută să urci proiectul pe Vercel fără să afectezi proiectul existent (avocat-site).

## ✅ Status Configurare

- ✅ **Git Remote:** Deja configurat → `https://github.com/tudorchelaru/calculator-pfa.git`
- ✅ **Vercel Config:** `vercel.json` este pregătit
- ⏳ **Repository GitHub:** Trebuie creat (sau deja există)

## 📋 Pași pentru Deployment

### Pasul 1: Creează Repository pe GitHub (dacă nu există)

1. **Mergi pe [github.com/tudorchelaru](https://github.com/tudorchelaru)**
2. **Click "New repository"**
3. **Nume:** `calculator-pfa`
4. **Public sau Private** (la alegere)
5. **NU adăuga** README, .gitignore sau licență (le avem deja)
6. **Click "Create repository"**

### Pasul 2: Push Codul pe GitHub

```bash
cd /Users/tchelaru/dev/calculator-pfa
git branch -M main
git push -u origin main
```

**Notă:** Dacă repository-ul este gol, GitHub va sugera comenzile. Folosește cele de mai sus.

### Pasul 3: Deployment pe Vercel

#### Opțiunea A: Via Dashboard (Recomandat) ⭐

1. **Mergi pe [vercel.com](https://vercel.com)** și autentifică-te

2. **Click pe "Add New..." → "Project"**

3. **Importă repository-ul:**
   - Selectează repository-ul `tudorchelaru/calculator-pfa` din listă
   - Dacă nu apare, click "Adjust GitHub App Permissions" și autorizează accesul
   - **IMPORTANT:** Acest proiect este separat de `avocat-site` - nu se vor afecta reciproc

4. **Configurează proiectul:**
   - **Project Name:** `calculator-pfa` (sau alt nume unic)
   - **Framework Preset:** Vercel detectează automat Astro
   - **Root Directory:** `./` (lasă gol)
   - **Build Command:** `npm run build` (deja setat)
   - **Output Directory:** `dist` (deja setat)
   - **Install Command:** `npm install` (deja setat)

5. **Click "Deploy"**

6. **Așteaptă build-ul** (1-2 minute)

7. **Gata!** Proiectul va fi live la un URL de tip: `calculator-pfa.vercel.app`

#### Opțiunea B: Via CLI

1. **Instalează Vercel CLI:**
   ```bash
   npm install -g vercel
   ```

2. **Autentifică-te:**
   ```bash
   vercel login
   ```

3. **Deploy:**
   ```bash
   vercel
   ```

4. **Răspunde la întrebări:**
   - Set up and deploy? → **Y**
   - Which scope? → Selectează contul tău
   - Link to existing project? → **N** (pentru proiect nou)
   - Project name? → `calculator-pfa` (sau alt nume)
   - Directory? → `./` (Enter)
   - Override settings? → **N**

5. **Pentru production:**
   ```bash
   vercel --prod
   ```

## ✅ Verificare

După deployment, verifică:
- ✅ Site-ul se încarcă corect
- ✅ Calculatorul funcționează
- ✅ Calculele sunt corecte
- ✅ Design-ul este responsive

## 🔄 Updates Viitoare

După ce proiectul este conectat cu Git:
- Fiecare `git push` va declanșa automat un nou deployment
- Vercel va face build automat
- Preview deployments pentru fiecare branch/PR

## 🛡️ Protecție Proiect Existente

**IMPORTANT:** Acest proiect este complet separat de `avocat-site`:
- ✅ Fiecare proiect are propriul nume unic (`calculator-pfa` vs `avocat-site`)
- ✅ Fiecare proiect are propriul URL (`calculator-pfa.vercel.app` vs `avocatchelaru.ro`)
- ✅ Nu se afectează reciproc - sunt proiecte independente
- ✅ Poți avea multiple proiecte pe același cont Vercel
- ✅ Același cont GitHub (`tudorchelaru`) dar repository-uri diferite

## 📝 Note

- Proiectul folosește configurația din `vercel.json`
- Build-ul se face automat la fiecare push
- Vercel oferă SSL gratuit (HTTPS)
- Poți configura domeniu custom din dashboard

## 🆘 Probleme?

Dacă întâmpini probleme:
1. Verifică că `npm run build` funcționează local
2. Verifică logs-urile din Vercel Dashboard
3. Asigură-te că toate dependențele sunt în `package.json`
