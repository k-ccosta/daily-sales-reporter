# 📊 daily-sales-reporter

Automação do envio diário de relatório de vendas para a diretoria, eliminando um processo manual e repetitivo.

## O que o projeto faz

Todo dia, o sistema interno disponibiliza um arquivo Excel com as vendas do dia anterior em uma pasta no Google Drive. Este script automatiza as seguintes etapas:

1. Abre o navegador e acessa a pasta no Google Drive
2. Faz o download do arquivo de vendas
3. Lê o arquivo e calcula o faturamento total e a quantidade de produtos vendidos
4. Abre o Gmail e envia um e-mail com os indicadores para a diretoria

## Tecnologias utilizadas

- [Python 3.12](https://www.python.org/)
- [PyAutoGUI](https://pyautogui.readthedocs.io/en/latest/) — automação de mouse e teclado
- [Pandas](https://pandas.pydata.org/) — leitura e processamento do arquivo Excel
- [Pyperclip](https://pypi.org/project/pyperclip/) — manipulação da área de transferência

## Como rodar o projeto

### Pré-requisitos

- Python 3.12 instalado
- Google Chrome instalado
- Estar logado no Gmail e no Google Drive no navegador

### Passo a passo

**1. Clone o repositório**
```bash
git clone https://github.com/seu-usuario/daily-sales-reporter.git
cd daily-sales-reporter
```

**2. Crie e ative o ambiente virtual**
```bash
python -m venv venv

# Windows
.\venv\Scripts\activate

# Linux/Mac
source venv/bin/activate
```

**3. Instale as dependências**
```bash
pip install -r requirements.txt
```

**4. Configure o script**

Antes de executar, ajuste no notebook `script.ipynb`:
- O caminho do arquivo Excel baixado (`path`)
- O e-mail do destinatário
- As coordenadas de clique (`x`, `y`) conforme a sua resolução de tela (veja o utilitário na última célula do notebook)

**5. Execute o notebook**
```bash
jupyter notebook script.ipynb
```

---

> Desenvolvido por [Kelvin Costa](https://www.linkedin.com/in/k-ccosta/)
