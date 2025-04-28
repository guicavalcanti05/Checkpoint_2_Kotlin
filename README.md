# Checkpoint_2_Kotlin
📈 CryptoMonitor
Aplicativo Android feito para monitorar o valor do Bitcoin em tempo real usando a API pública do Mercado Bitcoin.

🚀 Sobre o Projeto
O CryptoMonitor é um app simples que mostra:

O preço atual do Bitcoin em reais 🇧🇷

A última data/hora de atualização 📅

Um botão para atualizar manualmente os dados 🔄

Ele foi feito usando Kotlin, Retrofit para consumo de API e Coroutines para chamadas assíncronas.

📋 Como Funciona o MainActivity.kt
A MainActivity é o coração da aplicação:

Quando o app é aberto, ela configura a Toolbar (a barra superior bonitona com o nome do app).

Ela também conecta o botão de Refresh que, ao ser clicado, faz uma chamada à API para buscar o valor mais recente do Bitcoin.

Quando a chamada é bem-sucedida, ela:

Atualiza o preço do Bitcoin (lblValue) formatado no padrão brasileiro (R$ 00,00).

Atualiza a data/hora (lblDate) convertendo o timestamp da API.

Se der ruim (API fora do ar, internet caiu, etc), mostra um Toast (aquela mensagenzinha pop-up) avisando o que aconteceu.

📦 Arquitetura do Backend
MercadoBitcoinService.kt: Interface Retrofit que define o endpoint da API (/api/BTC/ticker/).

MercadoBitcoinServiceFactory.kt: Fábrica que cria uma instância do Retrofit com a URL base do Mercado Bitcoin.

TickerResponse.kt: Modelos de dados que mapeiam o JSON da resposta da API.

🎨 Interface
O app também utiliza um tema bonitinho com:

Cores customizadas definidas em Color.kt

Tipografia personalizada em Type.kt

Controle de tema claro/escuro em Theme.kt

⚙️ Tecnologias Usadas
Kotlin

Android Studio

Retrofit 2

Coroutines

Material 3

API pública do Mercado Bitcoin

🧠 Possíveis Melhorias Futuras
Mostrar gráfico de variação do BTC 📊

Notificações de mudança de preço 🔔

Suporte a outras criptomoedas 🪙


Imagem 1
![image](https://github.com/user-attachments/assets/c81e535d-c05d-45b4-afe6-7e9da1a1391d)

Imagem 2
![image](https://github.com/user-attachments/assets/70039e8b-9463-4916-8fee-28475c427a14)

