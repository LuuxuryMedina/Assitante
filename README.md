# Assitante — OmniRoute

[OmniRoute](https://github.com/cheaper-inference/OmniRoute) : passerelle IA open source (MIT),
un seul endpoint compatible OpenAI pour des centaines de fournisseurs, avec bascule automatique.

## Démarrage

```bash
npm install
npm start          # lance OmniRoute
```

Dashboard : http://localhost:20128 — ajoutez-y vos fournisseurs / clés API.
Endpoint OpenAI-compatible : `http://localhost:20128/v1`

Alternative Docker : `docker compose up -d`

## Utilisation

Dans n'importe quel client (Claude Code, Cursor, Cline, SDK OpenAI…) :

- Base URL : `http://localhost:20128/v1`
- API key : celle générée dans le dashboard OmniRoute

Ne commitez jamais `.env` ni `data/` (clés API).

## Sécurité

Par défaut OmniRoute écoute sur `0.0.0.0` sans clé API obligatoire. Sur un réseau non fiable :

```bash
OMNIROUTE_SERVER_HOST=127.0.0.1 REQUIRE_API_KEY=true npm start
```
