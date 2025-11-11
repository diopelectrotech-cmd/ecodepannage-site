
# 🚀 GUIDE DE DÉPLOIEMENT VERCEL - ECO DEPANNAGE TV

## ✅ ÉTAPE 3 : TÉLÉCHARGER VOTRE CODE

### 📦 1. Téléchargez le fichier ZIP de votre site

**👉 Cliquez sur ce lien pour télécharger :**
[Télécharger le code du site](FILES_PANEL)

**Le fichier s'appelle :** `nextjs_space.zip`

---

## ✅ ÉTAPE 4 : CRÉER UN DÉPÔT GITHUB

### 📝 Instructions détaillées :

1. **Allez sur GitHub**
   👉 [https://github.com/new](https://github.com/new)

2. **Créez un nouveau dépôt**
   - **Repository name** : `ecodepannage-site`
   - **Description** : `Site ECO DEPANNAGE TV - Réparation électronique`
   - Laissez **Public** coché
   - ❌ NE COCHEZ PAS "Add a README file"
   - Cliquez sur **"Create repository"**

3. **Vous verrez une page avec des instructions**
   - ✋ **ATTENDEZ** - Ne faites rien pour l'instant !

---

## ✅ ÉTAPE 5 : UPLOADER VOTRE CODE SUR GITHUB

### 🖱️ Méthode SIMPLE (Sans ligne de commande) :

1. **Sur votre page GitHub**, cherchez le bouton **"uploading an existing file"**
   - Cliquez dessus

2. **Dézippez le fichier** `nextjs_space.zip` sur votre ordinateur

3. **Glissez-déposez** TOUS les fichiers dans GitHub
   - Faites attention : il faut glisser les fichiers **à l'intérieur** du dossier, pas le dossier lui-même

4. **En bas de la page**, cliquez sur **"Commit changes"**

5. **Attendez** que GitHub finisse d'uploader (ça peut prendre 1-2 minutes)

---

## ✅ ÉTAPE 6 : CONNECTER GITHUB À VERCEL

1. **Retournez sur Vercel**
   👉 [https://vercel.com/dashboard](https://vercel.com/dashboard)

2. **Cliquez sur "Add New"** → **"Project"**

3. **Importez votre dépôt GitHub**
   - Cherchez **"ecodepannage-site"**
   - Cliquez sur **"Import"**

4. **Configuration** :
   - **Framework Preset** : Next.js (déjà sélectionné)
   - **Root Directory** : `.` (laissez par défaut)
   - **Build Command** : `yarn build` (laissez par défaut)
   - **Output Directory** : `.next` (laissez par défaut)

5. **Variables d'environnement** (TRÈS IMPORTANT) :
   - Cliquez sur **"Environment Variables"**
   - Ajoutez ces variables :

   ```
   DATABASE_URL=postgresql://user:password@host:5432/database
   AWS_BUCKET_NAME=votre-bucket
   AWS_FOLDER_PREFIX=votre-prefix/
   ```

   ⚠️ **JE VOUS DONNERAI CES VALEURS** - Ne les inventez pas !

6. **Cliquez sur "Deploy"**

7. **Attendez 2-3 minutes** ⏳

8. **Votre site est en ligne !** 🎉

---

## ✅ ÉTAPE 7 : CONFIGURER VOTRE DOMAINE

1. **Sur Vercel**, allez dans **"Settings"** → **"Domains"**

2. **Ajoutez votre domaine** :
   - Tapez : `ecodepannage.com`
   - Cliquez sur **"Add"**

3. **Vercel vous donnera des instructions** pour configurer votre DNS

4. **Allez chez votre registrar** (OVH, Gandi, etc.)

5. **Ajoutez un enregistrement A** :
   ```
   Type: A
   Nom: @
   Valeur: 76.76.21.21
   ```

6. **Ajoutez un enregistrement CNAME** :
   ```
   Type: CNAME
   Nom: www
   Valeur: cname.vercel-dns.com
   ```

7. **Attendez 24-48h** pour la propagation DNS

---

## 🆘 BESOIN D'AIDE ?

**Dites-moi où vous êtes bloqué** :
- ❓ "Je ne trouve pas comment uploader sur GitHub"
- ❓ "Je ne vois pas mon dépôt sur Vercel"
- ❓ "J'ai besoin des variables d'environnement"
- ❓ "Je ne sais pas configurer mon DNS"

**On résout ça ensemble !** 👍
