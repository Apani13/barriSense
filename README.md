# BarriSense

**Sense calma, sense comerç local, sense descans...  

Barri sense barri.**

---

## 🚀 1. Resum

BarriSense és una web participativa on la ciutadania pot enviar queixes sobre el seu barri i veure-les representades en un mapa de calor que mostra el nivell de malestar social a Barcelona.

---

## 💡 2. Motivació i problema

Els veïns necessiten un espai per ser escoltats i expressar com la pressió turística afecta la seva vida quotidiana.  
BarriSense dona forma a aquestes veus, convertint-les en informació social de valor per entendre el benestar i la percepció real dels barris.

---

## 🧩 3. Solució

Els usuaris poden registrar queixes de manera senzilla i veure com s’acumulen al mapa segons el volum per barri.  
Sense classificacions ni filtres: el mapa mostra on la tensió ciutadana és més alta i com es viu la ciutat des de dins.

---

## ⚙️ 4. Tecnologies usades

| Capa | Tecnologia |
|------|-------------|
| Frontend | React + vite |
| Backend | Java + Spring Boot |
| Base de dades | H2 (memòria temporal) |

---

## 🧱 5. Arquitectura breu

```
[Frontend React/Leaflet] ⇄ [API REST Spring Boot] ⇄ [H2 Database]
```

L’aplicació utilitza H2 com a base de dades embeguda, ideal per a proves i prototips sense necessitat d’instal·lació addicional.

---

# 🧪 6. Com provar-la

El projecte està dividit en dos repositoris: un per al **frontend** i un altre per al **backend**.  
Per provar la solució completa, segueix aquests passos:

---

Accedeix al repositori del backend i segueix les instruccions d'instalació detallades al README

> https://github.com/Apani13/barriSense-Backend

Després, accedeix al repositori del frontend i segueix les instruccions d'instalació detallades al README

> https://github.com/OhMyLaia/barriSense-frontend

---

## 🧠 8. Equip

| Nom | Rol |
|------|------|
| Flavio | Backend |
| Aurelien | Fullstack |
| Andrea | backend |
| Jose | Backend |
| Lara | Frontend |
| Laia | Frontend |


---

## 🗺️ 9. Futur / Roadmap

- Afegir filtres per tipologia o temps.  
- Incorporar sistemes de votació o priorització.  
- Crear un panell per a administracions amb estadístiques ciutadanes.  
- Obrir la plataforma com a observatori social de convivència urbana.

---

✊ **Allà on les dades oficials es queden curtes, BarriSense escolta.**  
*Perquè darrere de cada punt al mapa hi ha una persona, un veí, una història.*
