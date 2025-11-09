# Standard Deploy (SD) - Ferramenta de Automação e Implantação de Software

Standard Deploy (SD) é um script de automação desenvolvido em Python para ambientes Windows.

O objetivo principal desta ferramenta é **padronizar e agilizar** a instalação e desinstalação de software em lote (em massa) através de uma interface de console interativa.

A ferramenta é executada com privilégios de administrador e utiliza comandos silenciosos (silent install) para garantir que a instalação de múltiplos programas ocorra sem intervenção do usuário.

## ⚙️ Funcionalidades

| Ação | Descrição |
| :--- | :--- |
| **Instalação em Lote** | Realiza o download e a instalação silenciosa de todos os programas listados. |
| **Instalação Individual/Seletiva** | Permite selecionar e instalar apenas programas específicos que ainda não estão instalados. |
| **Desinstalação** | Oferece modos para desinstalação total ou individual de programas. |
| **Gerenciamento de Lista** | A lista de programas é editável através de um arquivo JSON. O usuário pode adicionar novos programas, editar parâmetros (URL, comandos silenciosos) e remover entradas. |
| **Verificação de Links** | Checa o status online de todas as URLs de download na lista. |
| **Utilitários** | Inclui opções para visualizar o log de instalação e limpar a pasta de instaladores. |

## 🛠️ Requisitos

* Sistema Operacional: Windows.
* Permissões de Administrador (O script solicita automaticamente).

## 🚀 Como Executar

1.  Baixe o executável `Standard_Deploy_SD.exe` (Disponível na pasta `dist/` após a compilação).
2.  Execute o arquivo como Administrador e utilize o menu para selecionar as operações desejadas.
