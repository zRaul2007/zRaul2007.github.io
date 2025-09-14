# 🐾 Sistema de Monitoramento para Saúde de Animais de Estimação

> Monitoramento inteligente para o bem-estar do seu melhor amigo.

![Banner do Projeto](https://via.placeholder.com/1200x400.png/3b82f6/ffffff?text=PetCare+IoT)
---

## 📄 Sobre o Projeto

Este projeto é um Trabalho de Conclusão de Curso (TCC) do curso Técnico em Mecatrônica da Etec Presidente Vargas. Desenvolvemos uma solução completa de Internet das Coisas (IoT) para o monitoramento remoto da saúde de pets.

O sistema é composto por uma **coleira inteligente** que coleta sinais vitais em tempo real e um **aplicativo multiplataforma** onde o tutor pode acompanhar os dados, visualizar históricos e receber alertas importantes sobre a saúde do seu animal.

### ✨ Principais Funcionalidades

-   📈 **Monitoramento em Tempo Real:** Acompanhamento de Frequência Cardíaca, Saturação de Oxigênio (SpO₂) e Temperatura.
-   📱 **Aplicativo Intuitivo:** Interface clara e fácil de usar para visualização dos dados (desenvolvido em Flutter).
-   ☁️ **Dados na Nuvem:** Sincronização automática dos dados com o Google Firebase.
-   🔔 **Sistema de Alertas:** Notificações são enviadas ao tutor caso algum sinal vital esteja fora dos parâmetros normais.
-   👤 **Gerenciamento de Pets:** O tutor pode cadastrar e gerenciar múltiplos animais no mesmo aplicativo.

---

## 🛠️ Tecnologias Utilizadas

A solução é dividida em três pilares principais: Hardware (a coleira), Backend (a nuvem) e Frontend (o aplicativo).

### Hardware

-   **Microcontrolador:** ESP32 C3 Mini
-   **Sensor de Frequência Cardíaca e SpO₂:** MAX30102
-   **Sensor de Temperatura:** DS18B20 (à prova d'água)

### Backend & Cloud

-   **Banco de Dados e Autenticação:** Google Firebase (Firestore, Authentication, Storage)
-   **Funções Serverless:** Firebase Cloud Functions (escritas em TypeScript) para processamento de alertas.

### Frontend (Aplicativo)

-   **Framework:** Flutter
-   **Linguagem:** Dart
-   **Gerenciamento de Estado:** Provider

---

## 🏛️ Arquitetura do Sistema

O fluxo de dados do nosso sistema foi projetado para ser simples e eficiente:

1.  Os **sensores** na coleira capturam os dados vitais do animal.
2.  O **ESP32** processa esses dados e os envia via Wi-Fi para o nosso banco de dados **Firebase Firestore**.
3.  O **aplicativo Flutter** lê os dados do Firestore em tempo real e os exibe para o tutor de forma gráfica e organizada.
4.  As **Cloud Functions** monitoram o banco de dados e disparam notificações push para o aplicativo se alguma medição crítica for detectada.

![Fluxograma do Sistema](https://via.placeholder.com/800x400.png/e5e7eb/4b5563?text=Fluxograma+do+Sistema)
---

## 📸 Screenshots do Aplicativo

<p align="center">
  <img src="https://via.placeholder.com/250x500.png/e5e7eb/4b5563?text=Tela+Login" alt="Tela de Login" width="200"/>
  <img src="https://via.placeholder.com/250x500.png/e5e7eb/4b5563?text=Tela+Home" alt="Tela Principal" width="200"/>
  <img src="https://via.placeholder.com/250x500.png/e5e7eb/4b5563?text=Tela+Medições" alt="Tela de Medições" width="200"/>
  <img src="https://via.placeholder.com/250x500.png/e5e7eb/4b5563?text=Tela+Alertas" alt="Tela de Alertas" width="200"/>
</p>
---

## 🚀 Como Executar o Projeto (App Flutter)

Para rodar o aplicativo localmente, siga os passos abaixo:

1.  **Clone o repositório:**
    ```bash
    git clone [https://github.com/zraul2007/flutter_application_1.git](https://github.com/zraul2007/flutter_application_1.git)
    cd flutter_application_1
    ```

2.  **Instale as dependências:**
    ```bash
    flutter pub get
    ```

3.  **Configure o Firebase:**
    -   Crie um projeto no [console do Firebase](https://console.firebase.google.com/).
    -   Adicione um app para Android e/ou iOS.
    -   Baixe o arquivo de configuração `google-services.json` (para Android) ou `GoogleService-Info.plist` (para iOS) e adicione-o nas pastas corretas do projeto, conforme a documentação do Firebase.

4.  **Execute o aplicativo:**
    ```bash
    flutter run
    ```

---

## 🧑‍💻 Equipe do Projeto

| Nome                              | Função Principal                  |
| --------------------------------- | --------------------------------- |
| **Davi Lucas N. R. Andrade** | Desenvolvedor Flutter             |
| **Enzo Maximus Mota Silva** | Projeto de Hardware               |
| **Pedro Mortari Fonseca Lima** | Documentação e Pesquisa           |
| **Raul Pedrogan de Moura** | Desenvolvedor Flutter e UI/UX     |
| **Thiago Hiroshi F. Ongawa** | Firmware e Testes                 |

---

## 📄 Licença

Este projeto é distribuído sob a licença MIT. Veja o arquivo `LICENSE` para mais detalhes.
