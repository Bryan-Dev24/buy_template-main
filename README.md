# Comprar — Lista de Compras

Aplicativo móvel de lista de compras desenvolvido com **React Native** e **Expo**. Permite adicionar, marcar como concluído e remover itens da lista, com persistência local via **TinyBase** + **SQLite**.

## Funcionalidades

- Adicionar itens à lista de compras
- Marcar/desmarcar itens como comprados
- Remover itens da lista
- Dados persistidos localmente no dispositivo (SQLite)
- Atualização reativa via listeners do TinyBase

## Tecnologias

| Tecnologia   | Versão   |
| ------------ | -------- |
| React Native | 0.83.2   |
| Expo         | ^55.0.6  |
| TinyBase     | ^8.0.1   |
| expo-sqlite  | ~55.0.10 |
| TypeScript   | ~5.9.2   |

## Estrutura do Projeto

```
src/
├── app/
│   └── Home/           # Tela principal
│       ├── index.tsx
│       └── styles.ts
└── components/
    ├── Button/         # Botão reutilizável
    ├── Input/          # Campo de texto reutilizável
    └── Item/           # Item da lista (checkbox + texto + delete)
```

## Como executar

### Pré-requisitos

- [Node.js](https://nodejs.org/)
- [Expo CLI](https://docs.expo.dev/get-started/installation/)
- Expo Go instalado no dispositivo ou emulador configurado

### Instalação

```bash
npm install
```

### Executar

```bash
# Iniciar o servidor de desenvolvimento
npm start

# Android
npm run android

# iOS
npm run ios

# Web
npm run web
```

## Persistência de Dados

Os dados são armazenados localmente usando **TinyBase** com o persister `persister-expo-sqlite`, que salva as informações em um banco SQLite (`database.db`) no dispositivo. O auto-save garante que qualquer alteração seja persistida automaticamente.
