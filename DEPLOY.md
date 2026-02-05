# 🚀 Ghid Deployment pe Vercel

Acest ghid te ajută să urci proiectul pe Vercel fără să afectezi proiectul existent (avocat-site).

## ✅ Status Configurare

- ✅ **Vercel Config:** `vercel.json` este pregătit
- ✅ **Git Local:** Repository local configurat
- ✅ **Git Remote:** Configurat → `https://github.com/tudorchelaru/calculator-pfa.git`
- ⏳ **Repository GitHub:** Trebuie creat (sau deja există)

## 📋 Workflow Deployment (ca la avocat-site)

### Pasul 1: Creează Repository pe GitHub (dacă nu există)

1. **Mergi pe [github.com/tudorchelaru](https://github.com/tudorchelaru)**
2. **Click "New repository"**
3. **Nume:** `calculator-pfa`
4. **Public sau Private** (la alegere)
5. **NU adăuga** README, .gitignore sau licență (le avem deja)
6. **Click "Create repository"**

### Pasul 2: Push Codul pe GitHub (prima dată)

```bash
cd /Users/tchelaru/dev/calculator-pfa
git push -u origin main
```

### Pasul 3: Conectează cu Vercel (prima dată)

1. **Mergi pe [vercel.com](https://vercel.com)** și autentifică-te
2. **Click "Add New..." → "Project"**
3. **Importă repository-ul:**
   - Selectează `tudorchelaru/calculator-pfa` din listă
   - Dacă nu apare, click "Adjust GitHub App Permissions"
4. **Configurează:**
   - Project Name: `calculator-pfa`
   - Vercel detectează automat Astro
5. **Click "Deploy"**

### Pasul 4: Workflow Normal (după prima configurare)

**La fiecare modificare, folosește același workflow ca la avocat-site:**

```bash
npm run build
git add .
git commit -m 'mesaj commit'
git push
```

**Vercel va face auto-deploy automat la fiecare push!** 🚀

## 🔄 Workflow Zilnic (după prima configurare)

**Exact ca la avocat-site:**

```bash
# 1. Build local (opțional, pentru testare)
npm run build

# 2. Adaugă modificările
git add .

# 3. Commit
git commit -m 'descriere modificări'

# 4. Push pe GitHub
git push
```

**Vercel va detecta automat push-ul și va face deploy!** ✨

## 🚀 Deployment Manual (dacă e nevoie)

Dacă vrei să faci deploy manual (fără Git), poți folosi Vercel CLI:

```bash
npm install -g vercel
vercel login
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
