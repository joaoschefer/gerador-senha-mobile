# 📱 Projeto: Gerador de Senhas Mobile

Este projeto é um app mobile desenvolvido com **React Native via Expo**, que permite ao usuário gerar, salvar e visualizar senhas de forma simples e segura. As senhas são armazenadas localmente no dispositivo usando `AsyncStorage`.

---

## 🚀 Tecnologias Utilizadas

- **React Native + Expo**  
  Framework para desenvolvimento de aplicativos mobile multiplataforma (Android/iOS), com suporte nativo via Expo.

- **AsyncStorage**  
  Usado para **armazenar as senhas localmente** no dispositivo de forma persistente.

- **React Navigation**  
  Biblioteca de navegação entre telas no React Native.

- **Safe Area Context**  
  Garante que os elementos da UI respeitem as áreas seguras da tela (notch, barra de status etc.).

- **Clipboard**  
  Permite copiar a senha gerada para a área de transferência do dispositivo.

---

## 📦 Dependências instaladas

| Pacote                                      | Descrição                                                                                  |
|---------------------------------------------|---------------------------------------------------------------------------------------------|
| **expo**                                     | Plataforma que facilita o uso do React Native, com diversas APIs nativas integradas.       |
| **react-native**                             | Framework para desenvolvimento nativo com React.                                           |
| **react**                                    | Biblioteca base do React Native.                                                           |
| **@react-native-async-storage/async-storage** | Armazena e recupera dados localmente de forma persistente (usado para salvar senhas).      |
| **@react-navigation/native**                 | Biblioteca principal de navegação entre telas no React Native.                             |
| **@react-navigation/bottom-tabs**            | Componente de abas inferiores para navegação (tabs).                                       |
| **react-native-safe-area-context**           | Garante que os elementos respeitem áreas seguras da tela (barra de status, notch etc.).    |
| **react-native-screens**                     | Otimiza a performance da navegação entre telas no React Navigation.                        |
| **expo-clipboard**                           | Permite copiar texto (como senhas) para a área de transferência.                           |
| **expo-status-bar**                          | Componente para controlar a aparência da barra de status (cor, visibilidade etc.).         |
| **@react-native-community/slider**           | Componente deslizante (slider), usado para definir o tamanho da senha.                     |
| **react-native-web**                         | Permite que o app também rode no navegador (modo web com Expo).                            |

---

## 📁 Estrutura do Projeto

| Pasta / Arquivo                        | Função                                                                 |
|----------------------------------------|------------------------------------------------------------------------|
| `src/hooks/useStorage.js`              | Hook customizado para salvar, buscar e deletar senhas com AsyncStorage.|
| `src/pages/home/index.js`              | Tela inicial onde o usuário gera a senha.                              |
| `src/pages/passwords/index.js`         | Tela que lista todas as senhas salvas.                                 |
| `src/pages/passwords/components/`      | Contém o componente `PasswordItem` que exibe cada senha.               |
| `src/components/modal/`                | (Provavelmente) componentes modais reutilizáveis.                      |
| `App.js`                               | Ponto de entrada da aplicação.                                         |
| `routes.js`                            | Configuração das rotas e navegação entre as páginas.                   |

---

## 🛠️ Scripts disponíveis

| Script                 | Descrição                              |
|------------------------|----------------------------------------|
| `npx expo start`       | Inicia o app com Expo.                 |

---

## 📌 Observações

- As senhas são armazenadas no dispositivo, ou seja, não há necessidade de conexão com internet.
- O app já está preparado para Android, iOS e Web (via `react-native-web`).
- A exclusão de senhas é feita com um **toque longo** no item da lista.
