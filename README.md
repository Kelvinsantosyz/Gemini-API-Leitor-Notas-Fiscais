# 🚀 Automação de Notas Fiscais com Google Gemini e Colab

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

**Última Atualização:** Agosto de 2025

Este projeto automatiza a extração de dados de Notas Fiscais de Serviço (NFS-e) em formato de imagem ou PDF, utilizando o poder da API do Google Gemini. Os dados são processados e organizados em uma Planilha Google, eliminando a necessidade de digitação manual.

---

### 💡 Por que usar o Google Colab para este projeto?

O Google Colab é a plataforma ideal para este projeto pelos seguintes motivos:

* **Ambiente Zero-Config:** Você não precisa instalar Python ou nenhuma biblioteca na sua máquina. Tudo roda na nuvem do Google.
* **Integração Nativa:** Conecta-se perfeitamente com outras ferramentas Google, como Drive (para ler os arquivos) e Sheets (para salvar os dados).
* **Acesso Gratuito a Recursos:** Oferece poder de processamento gratuitamente para prototipagem e uso moderado.
* **Portabilidade e Compartilhamento:** Qualquer pessoa com uma conta Google pode abrir e executar seu código com um único clique.

---

### ✨ Funcionalidades

* **Extração Inteligente:** Lê arquivos `.pdf`, `.png`, `.jpg` e extrai dezenas de campos usando a mais recente IA do Google.
* **Fluxo Contínuo:** Busca novos arquivos em uma pasta do Google Drive e atualiza uma Planilha Google automaticamente.
* **Prevenção de Duplicatas:** Garante que cada arquivo seja processado apenas uma vez através de um hash MD5.
* **Segurança:** Mantém sua chave de API segura usando o gerenciador de segredos nativo do Colab.

---

### 💸 Custos e Limites de Uso da API

É fundamental entender os custos associados ao uso da API Gemini para evitar surpresas na fatura.

* **Nível Gratuito (Free Tier):** O Google geralmente oferece um nível gratuito generoso para a API Gemini, que pode ser suficiente para uso pessoal ou projetos de pequeno volume (ex: até 60 consultas por minuto, sujeito a alterações).
* **Uso Pago (Pay-as-you-go):** Acima do limite gratuito, os custos são calculados com base no tipo de entrada e no número de tokens (palavras/caracteres). Para este projeto, o custo principal vem da análise de imagens/PDFs.

**Exemplo de Custo (Valores Hipotéticos - Verifique a Documentação Oficial):**
* **Processamento de Imagem:** ~$0.0025 por imagem.
* **Processamento de PDF:** ~$0.0025 por página + custo por token.

> **⚠️ AVISO:** Os preços mudam. Sempre consulte a **[página oficial de preços do Google Cloud Vertex AI](https://cloud.google.com/vertex-ai/pricing)** para obter os valores mais recentes antes de processar um grande volume de documentos.

---

### 🛠️ Tecnologias Utilizadas

* **Python 3**
* **Google Colab**
* **Google Gemini API (Modelo `gemini-1.5-pro`)**
* **Google Drive API & Google Sheets API**
* **Bibliotecas:** `google-generativeai`, `gspread`, `pandas`, `pillow`

---

### 🚀 Guia Rápido: Do Zero à Automação

(... O guia de configuração e execução que criamos anteriormente continua aqui, pois já é excelente ...)

---

### 🌱 Próximos Passos e Melhorias Futuras

Este projeto é uma base poderosa. Aqui estão algumas ideias de como ele pode ser expandido:

* **📝 Logging Avançado de Erros:** Em vez de apenas imprimir erros no console, registrar falhas (ex: PDFs corrompidos, JSON malformado) em uma aba separada da planilha para fácil auditoria.
* **🗂️ Suporte a Mais Campos:** Modificar o *prompt* do Gemini para extrair informações adicionais, como impostos retidos (PIS, COFINS, etc.) ou detalhes específicos do serviço.
* **⚙️ Processamento em Lote (Batch Processing):** Para um grande volume de arquivos, adaptar o script para processar vários documentos em uma única chamada à API, otimizando o custo e o tempo.
* **🔔 Notificações:** Integrar com um serviço de e-mail ou mensageria (como o Telegram) para enviar um resumo diário dos totais processados ou alertar sobre erros.

---

### 🤝 Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para abrir uma *issue* para relatar bugs ou um *pull request* com novas funcionalidades.

### 📝 Licença

Distribuído sob a Licença MIT.
