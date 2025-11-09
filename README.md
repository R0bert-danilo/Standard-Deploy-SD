# ⚙️ Standard Deploy (SD) - Framework de Automação de Implantação de Software

Olá, sou **Robert Danilo**, e este é o Standard Deploy.

## 🧑‍💻 Quem Eu Sou e Objetivo

Eu sou **aluno de Análise e Desenvolvimento de Sistemas (ADS)** e trabalho na área de **Suporte Técnico N3**. Desenvolvi o Standard Deploy como um projeto prático focado em resolver os desafios de **tempo e padronização** que enfrentamos no dia a dia do suporte.

Este projeto visa criar uma solução em Python para automatizar a implantação e manutenção de software, reduzindo a intervenção manual e o erro humano. Convido a comunidade a testar e contribuir!

---

## ✨ Visão Geral do Projeto

O Standard Deploy é um utilitário de console (CLI) construído em Python, focado na gestão do ciclo de vida de softwares em sistemas **Windows**. Ele opera com **privilégios de Administrador** para garantir a eficácia dos comandos de **instalação silenciosa** e a manipulação correta do **Registro do Windows** (winreg) para verificar o status de instalação.

### Arquitetura e Módulos Chave

| Módulo | Função Técnica |
| :--- | :--- |
| **`subprocess`** | Execução e controle de comandos de instalação/desinstalação externos (`.exe` com `/S` ou `.msi` com `/qn`). |
| **`requests` e `tqdm`** | Gerenciamento de requisições HTTP e download de binários, com rastreamento visual do progresso. |
| **`winreg`** | Acesso e leitura das chaves de desinstalação no Registro (`HKEY_LOCAL_MACHINE`, `HKEY_CURRENT_USER`) para verificação de status. |
| **`colorama`** | Aplica formatação ANSI (cores e estilos) para melhorar a experiência e legibilidade no console do Windows. |
| **`tkinter`** | Utilizado para abrir a caixa de diálogo nativa do sistema para seleção de arquivos JSON externos (opção [J]). |

### Fluxos de Operação

* **Instalação Silenciosa em Lote:** Baixa e executa a instalação sem interação.
* **Desinfecção Total:** Fluxo de duas fases: desinstalação silenciosa completa seguida por uma reinstalação limpa.
* **Gerenciamento de Lista (JSON):** Manipulação direta e interativa da lista de softwares e seus parâmetros de instalação/desinstalação.

## ⬇️ Download e Implementação

A versão compilada (stand-alone) não requer dependências Python no sistema de destino.

### 🔗 Link de Download (Executável Stand-Alone)

[**BAIXE Standard Deploy (SD) - v1.0**](https://bit.ly/4qQYp0a)

### 📋 Instruções Operacionais

1.  **Elevação de Privilégio:** Inicie o arquivo **`Standard_Deploy_SD.exe`** **obrigatoriamente** com privilégios de Administrador.
2.  **Seleção de Fluxo:** Utilize as opções do menu (ex: **[1] FLUXO COMPLETO** ou **[D] DESINFECÇÃO TOTAL**) para iniciar a automação.
3.  **Auditoria:** Consulte a opção **[6]** no menu para visualizar o **`log_instalacao.txt`** e rastrear códigos de retorno e falhas operacionais.

---

## 💻 Instruções de Compilação e Desenvolvimento

Para quem deseja clonar o repositório e rodar o script diretamente ou gerar o próprio executável.

### Instalação de Bibliotecas Python (Requerimentos)

Para rodar o script a partir do código-fonte (`.py`), você precisará das seguintes bibliotecas. Instale-as usando `pip`:

```bash
pip install colorama requests tqdm beautifulsoup4
