# 🧠 Brave Goggle – AI & Automatisation Web

Un filtre de recherche Brave conçu pour les développeurs, créateurs d'automatisations et passionnés d’intelligence artificielle.  
Ce Goggle privilégie les résultats issus de sources techniques fiables (OpenAI, n8n, Zapier, HuggingFace, Dev.to, GitHub…)  
et élimine les sites non pertinents ou à faible valeur ajoutée (Pinterest, Quora, forums, etc.).

## ⚙️ Utilisation rapide

Copiez simplement ce lien dans le champ **“goggles”** du [Brave Search API Playground](https://api-dashboard.search.brave.com/app/playground?codeSample=js) :

```
https://raw.githubusercontent.com/pacacreaweb/brave-goggles/main/ai-automation.goggle
```

Ou utilisez-le dans vos requêtes API :

```json
"goggles": [
  "https://raw.githubusercontent.com/pacacreaweb/brave-goggles/main/ai-automation.goggle"
]
```

## 💡 Objectif

> Filtrer et hiérarchiser les résultats autour de :
> - L’intelligence artificielle (ChatGPT, LLM, API…)
> - L’automatisation (n8n, Zapier, Pipedream, Make…)
> - Le développement web (Node.js, API REST, Dev.to, GitHub…)
> - Les outils no-code/low-code et productivité.

## 🧱 Structure du Goggle

```yaml
version: 1
title: "AI & Automatisation Web"
description: "Filtre de recherche Brave pour la veille technique sur l’IA, l’automatisation et le développement web."
include_domains:
  - openai.com
  - huggingface.co
  - n8n.io
  - zapier.com
  - make.com
  - pipedream.com
  - dev.to
  - github.com
  - notion.so
exclude_domains:
  - pinterest.com
  - quora.com
  - reddit.com
boost_terms:
  - ai
  - automation
  - workflow
  - n8n
  - zapier
  - api
```

## 🧩 Exemple d’utilisation avec cURL

```bash
curl -X POST "https://api.search.brave.com/res/v1/web/search"   -H "Accept: application/json"   -H "X-Subscription-Token: VOTRE_CLE_API_BRAVE"   -d '{
        "query": "automation workflows",
        "goggles": [
          "https://raw.githubusercontent.com/pacacreaweb/brave-goggles/main/ai-automation.goggle"
        ]
      }'
```

## 📘 À propos

Auteur : **Jean-Michel Guilmot (PacaCreaWeb.fr)**  
Contact : [https://pacacreaweb.fr](https://pacacreaweb.fr)  
Licence : MIT  

🧭 *Optimisé pour la veille IA et les projets d’automatisation intelligente.*
