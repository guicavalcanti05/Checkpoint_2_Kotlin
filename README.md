# CryptoMonitor 📈

App Android para monitorar o valor do Bitcoin em tempo real.

---

## Sobre o projeto

O CryptoMonitor é um app simples e funcional. Ele mostra:

- 💰 O preço atual do Bitcoin em reais (BRL)
- 📅 A data e hora da última atualização
- 🔄 Um botão para atualizar os dados manualmente

Tudo isso puxando informações direto da API pública do Mercado Bitcoin.

---

## Como funciona o MainActivity.kt

- Ao abrir o app, a `MainActivity` configura a Toolbar com o título do app.
- O botão "Refresh" dispara uma chamada para a API (`makeRestCall()`).
- Quando a resposta chega:
  - Atualiza o valor do Bitcoin (`lbl_value`) formatado como moeda brasileira.
  - Atualiza a data/hora (`lbl_date`) baseado no timestamp retornado.
- Se a chamada der erro (tipo 404 ou 500), o app mostra um Toast avisando o que rolou.

A chamada à API é feita usando coroutines pra não travar a UI.

---

## Estrutura de chamadas à API

- `MercadoBitcoinService.kt` → Define o endpoint `/api/BTC/ticker/` usando Retrofit.
- `MercadoBitcoinServiceFactory.kt` → Cria uma instância do Retrofit já configurada.
- `TickerResponse.kt` → Modela a resposta da API (valores como `last`, `high`, `low`, `date`, etc.).

---

## Estilo e Temas

- Cores definidas em `Color.kt`
- Tipografia customizada em `Type.kt`
- Suporte a tema claro/escuro em `Theme.kt`

---

## Tecnologias usadas

- Kotlin
- Android Studio
- Retrofit 2
- Coroutines
- Material Design 3
- API do [Mercado Bitcoin](https://www.mercadobitcoin.com.br/)

---



## Prints

Imagem 1
![image](https://github.com/user-attachments/assets/0bf3a9b8-0e8d-4fcc-a68d-99bce38cd230)


Imagem 2
![image](https://github.com/user-attachments/assets/a83add36-3d53-42f0-b41e-3bef42c8e037)

---

