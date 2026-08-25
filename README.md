# AppFiscalizacao.py

# 🔍 Portal de Fiscalização GGTAB/ANVISA

Uma aplicação web interativa desenvolvida em Python e Streamlit para otimizar e digitalizar o processo de auditoria e fiscalização de produtos regulados. O sistema unifica bases de dados e permite operações em tempo real com geração automatizada de autos de infração.

O projeto resolve o desafio do preenchimento manual de relatórios em campo, eliminando redundâncias e centralizando as informações de apreensões (como dispositivos eletrônicos para fumar e propagandas irregulares) em uma interface ágil e conectada à nuvem.

## 🚀 Principais Funcionalidades

* **Sincronização em Nuvem (Supabase):** Banco de dados global integrado. Produtos recém-cadastrados por um fiscal ficam imediatamente disponíveis para toda a equipe.
* **Visão Computacional (OCR):** Extração automática de numerações de CNPJ a partir de fotografias de rótulos utilizando Tesseract, acelerando a identificação de produtos.
* **Geração Dinâmica de Documentos:** Exportação instantânea de Autos de Inspeção em formato PDF (com evidências fotográficas anexadas) e planilhas Excel consolidadas por loja.
* **Trilha de Auditoria (Logs):** Monitoramento contínuo das ações dos usuários para garantir a integridade e rastreabilidade das operações.
* **Mecanismos de Resiliência:** O sistema funciona graciosamente mesmo se as bibliotecas de OCR ou a conexão com a nuvem falharem, garantindo que o fiscal nunca fique travado em campo.

## 🛠️ Tecnologias Utilizadas

* **Python & Streamlit:** Para a construção da lógica de negócio e interface de usuário.
* **Supabase (PostgreSQL):** Como Backend-as-a-Service para persistência de dados e auditoria.
* **Pytesseract & Pillow:** Para processamento de imagens e Reconhecimento Óptico de Caracteres.
* **Pandas, OpenPyXL e FPDF:** Para estruturação de dados tabulares e geração de relatórios oficiais.

## ⚙️ Como Configurar e Executar

1. Clone o repositório e acesse a pasta do projeto:
   git clone [https://github.com/seu-usuario/nome-do-repositorio.git](https://github.com/seu-usuario/nome-do-repositorio.git)
   cd nome-do-repositorio

   Crie um ambiente virtual e instale as dependências:
  python -m venv venv
  source venv/bin/activate  # Linux/Mac
  venv\Scripts\activate     # Windows
  pip install -r requirements.txt

  Configuração de Segredos: Crie uma pasta .streamlit na raiz do projeto e adicione um arquivo secrets.toml com suas credenciais do Supabase:

  Ini, TOML
  SUPABASE_URL = "sua_url_aqui"
  SUPABASE_KEY = "sua_chave_aqui"

  Execute a aplicação:
  streamlit run app.py

  No futuro caso queira rodar ele de formar online só usar esse mesmo repositório no Streamlit Community Cloud
