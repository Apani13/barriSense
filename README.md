# 🌍 BarriSense

![Preview](assets/screenshot1.png)

**BarriSense** és una plataforma web per **visualitzar i entendre** com la **pressió turística** afecta els barris de Barcelona. A partir de **queixes ciutadanes**, ofereix una imatge **real i no edulcorada** de la situació a cada districte. Mostrem un **mapa de calor** amb el nivell d’afectació per barri (volum i tipologia de queixes) i permetem consultar l’estat del teu barri o d’altres zones de la ciutat.

---

## 🎯 Objectiu
Crear un espai on la **ciutadania** faci sentir la seva **veu** i, alhora, consultar l’impacte real de la pressió turística. BarriSense fa visibles els **desequilibris urbans** i aporta eines a les **administracions** per decidir millor.

## 💬 Valor per a la ciutadania
- Centralitza les **queixes** i les converteix en **veu col·lectiva**.
- Mostra amb claredat què passa al teu barri: **soroll, massificació, pèrdua d’identitat, manca de descans**.
- Fomenta **consciència col·lectiva** sobre convivència i límits de la sostenibilitat turística.

## 🏛️ Valor per a les institucions
- **Diagnosi participativa** amb dades reals aportades pels veïns.
- Complementa **fonts oficials** amb **informació social qualitativa**.
- Ajuda a **prioritzar polítiques públiques** on hi ha més tensió o conflicte.

## 🔮 Evolució (roadmap curt)
A futur, incorporarem **APIs públiques** i **indicadors ambientals**:
- Nivells de **soroll** i **contaminació**
- Densitat d’**allotjaments turístics**
- **Fluxos de mobilitat**
- Indicadors de **benestar i descans** urbà

> ✊ **Missatge clau**
> BarriSense **no edulcora** la realitat: mostra **barris sense pau, sense silenci, sense descans… sense barri.** Només reconeixent el **malestar** podrem construir una ciutat **més habitable**.

---

## 💫 Com evolucionem la proposta original
El repte demanava una app amb **dades públiques** i **indicadors oficials** sobre saturació turística.
A BarriSense hi afegim el que les dades no capten: **el sentir dels veïns**.

- Les **APIs públiques** (p. ex. cartografia municipal) donen **marc i mapa**.
- La **veu ciutadana** aporta el **relat viu**: queixes i percepcions del dia a dia.

👉 **Combinem dades oficials + dades socials** per una imatge **més completa i humana** de la ciutat.

> 🧩 *Les dades mostren **on** passen les coses; les veus ciutadanes expliquen **per què** passen.*

---

## 🧭 Resum narratiu (per transició oral/slide)
Neixem del repte de visualitzar la pressió turística per barris amb **dades obertes**, i hi sumem el **bategar** del carrer.
**APIs públiques** posen el mapa; **aportacions veïnals** en posen la vida.
El resultat: una eina de **diagnosi** i, alhora, un **espai de veu col·lectiva**.

---

## 🧩 Arquitectura (alt nivell)
[Frontend React/Leaflet] ⇄ [API REST Spring Boot] ⇄ [MySQL]

yaml
Copia el codi

📦 **Repos tècnics**
- 🖥️ Frontend → https://github.com/TUUSUARIO/barriSense-frontend
- ⚙️ Backend → https://github.com/TUUSUARIO/barriSense-backend

> ℹ️ Cada sub-repo conté el seu `README` específic (instal·lació i scripts).

---

## 🧰 Execució **local** (únic mode suportat)

### Requisits
- **Node.js 18+**
- **Java 17+**
- **MySQL 8+** (local)
  *(Opcional: si el backend té perfil H2, el podeu usar: `-Dspring.profiles.active=h2`)*

### 1) Backend
```bash
# 1. Variables (exemple per MySQL local)
#   SPRING_DATASOURCE_URL=jdbc:mysql://localhost:3306/barrisense
#   SPRING_DATASOURCE_USERNAME=root
#   SPRING_DATASOURCE_PASSWORD=secret

cd barriSense-backend
./mvnw spring-boot:run
# L'API queda a: http://localhost:9000
2) Frontend
bash
Copia el codi
cd barriSense-frontend
# .env.local
#   REACT_APP_API_URL=http://localhost:9000
npm install
npm start
# Web a: http://localhost:3000
3) Dades de prova
El backend seeda barris i algunes incidències d’exemple a l’arrencar.

Endpoints útils:

GET http://localhost:9000/health

GET http://localhost:9000/api/barrios

GET http://localhost:9000/api/quejas

POST http://localhost:9000/api/quejas (JSON amb { barrioId, tipo, intensidad, comentario })

✅ Validació ràpida (2 minuts pel jurat)
Obrir http://localhost:3000

Veure el mapa i el calor per barris.

Crear una queixa (formulari) i comprovar que el mapa/llistat s’actualitza.

(Opcional) Test API:

bash
Copia el codi
curl http://localhost:9000/health
curl http://localhost:9000/api/barrios
🧱 Tecnologies
Capa	Stack
Frontend	React, Leaflet, Vite/CRA, HTML/CSS
Backend	Java 17, Spring Boot (REST)
Dades	MySQL 8 (o H2 en perfil dev)
Dev	GitHub, README + docs-as-code

🧩 Problemes comuns (FAQ)
CORS: assegura http://localhost:3000 com a origen permès al backend.

Ports: backend 9000, frontend 3000 (canvia REACT_APP_API_URL si cal).

MySQL: crea el schema barrisense i usuari/contrassenya correctes.

Seed: si no apareixen dades, revisa logs d’arrencada o executa data.sql.

👥 Equip
Nom	Rol	Àrea
Mariona Pan	Coordinació / Backend	API, model de dades
Leo Fernández	Frontend & UX	UI, mapa, interacció
Rayane Ben	Dades / Integracions	cartografia i persistència

🗺️ Estructura del repo principal
lua
Copia el codi
barriSense/
├─ README.md
├─ docs/
│  ├─ architecture.md
│  └─ roadmap.md
├─ assets/
│  ├─ screenshot1.png
│  └─ screenshot2.gif
└─ (enllaços als sub-repos)