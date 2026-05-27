# blue-hat-comandos
Somente um repositório para eu salvar meus comandos e deixar registrado o que eu já estudei sobre o Linux especificamente fedora.

# Guia de Comandos Essenciais para Fedora Linux

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Fedora](https://img.shields.io/badge/Fedora-37-blue?logo=fedora)](https://getfedora.org/)

Um repositório colaborativo com os comandos mais úteis e essenciais para quem utiliza o Fedora Linux, seja você iniciante ou usuário avançado.

## 📖 Sobre

Este guia foi criado para servir como uma referência rápida de comandos de terminal no Fedora. Aqui você encontrará desde navegação básica em diretórios até comandos avançados de rede e gerenciamento de pacotes com o `dnf`, o gerenciador oficial do Fedora.

> **Dica de Ouro**: Para obter a documentação completa de qualquer comando listado aqui, use `man <comando>` (ex: `man dnf`).

---

## 📂 1. Navegação em Arquivos e Pastas

Comandos fundamentais para se locomover e explorar o sistema de arquivos.

| Comando | Função |
| :--- | :--- |
| `ls` | Lista o conteúdo de um diretório. |
| `pwd` | Mostra o caminho completo do diretório atual (*Print Working Directory*). |
| `cd` | Troca de diretório (*Change Directory*). |
| `locate` | Procura um arquivo em todo o sistema e exibe seu caminho (usa um banco de dados). |
| `find` | Encontra arquivos dentro de um diretório específico em tempo real. |

## 🛠️ 2. Operações com Arquivos e Pastas

Criar, copiar, mover, deletar e visualizar arquivos.

| Comando | Função |
| :--- | :--- |
| `mkdir` | Cria um novo diretório. |
| `rmdir` | Remove um diretório **vazio**. |
| `rm` | Exclui arquivos (use `rm -rf` com cuidado para pastas). |
| `cp` | Copia um arquivo ou diretório para outro local. |
| `mv` | Move ou renomeia um arquivo ou pasta. |
| `touch` | Cria um arquivo vazio ou atualiza a data/hora de um existente. |
| `file` | Mostra o tipo (formato) de um arquivo. |
| `zip` / `unzip` | Compacta ou extrai arquivos no formato ZIP. |
| `tar` | Agrupa/compacta arquivos em tarball (`.tar`, `.tar.gz`). |
| `nano`, `vi` ou `jed` | Abre um editor de texto direto no terminal. |
| `cat` | Exibe o conteúdo completo de um arquivo no terminal. |
| `grep` | Encontra linhas específicas que casam com um padrão dentro de um arquivo. |
| `sed` | Busca e substitui um padrão em um arquivo (stream editor). |
| `head` | Mostra apenas as primeiras 10 linhas de um arquivo. |
| `tail` | Mostra apenas as últimas 10 linhas de um arquivo. |
| `awk` | Linguagem de script para busca e manipulação de padrões em arquivos. |
| `sort` | Reorganiza o conteúdo de um arquivo em ordem alfabética ou numérica. |
| `cut` | Seleciona e imprime partes específicas (colunas) de um arquivo. |
| `diff` | Compara o conteúdo de dois arquivos linha por linha. |
| `tee` | Envia a saída de um comando ao mesmo tempo para um arquivo e para o terminal. |
| `echo` | Imprime um texto na tela (muito usado em scripts). |
| `ln` | Cria links físicos (hard) ou simbólicos (soft) entre arquivos. |
| `alias` / `unalias` | Cria ou remove um apelido para um comando (ex: `alias ll='ls -la'`). |

## 📦 3. Gerenciamento de Pacotes (DNF)

O coração do Fedora. Comandos essenciais para instalar e gerenciar softwares.

| Comando | Função |
| :--- | :--- |
| `dnf install <pacote>` | Instala um pacote no sistema. |
| `dnf remove <pacote>` | Remove um pacote do sistema. |
| `dnf update` | Atualiza **todos** os pacotes do sistema para a versão mais recente. |
| `dnf search <termo>` | Busca por pacotes que contenham o termo no nome ou descrição. |
| `dnf info <pacote>` | Exibe informações detalhadas sobre um pacote (versão, licença, tamanho). |
| `dnf list installed` | Lista todos os pacotes já instalados no sistema. |
| `dnf provides <arquivo>` | **Comando Ninja:** Descobre qual pacote fornece um determinado arquivo (ex: `dnf provides /usr/bin/nano`). |
| `sudo dnf clean all` | Limpa todo o cache do DNF, liberando espaço em disco. |
| `sudo dnf autoremove` | Remove dependências que não são mais necessárias para nenhum pacote. |
| `dnf history` | Mostra um histórico completo de todas as transações do DNF (instalações, remoções). |

## 👥 4. Gerenciamento de Usuários e Permissões

Controle de acesso e segurança.

| Comando | Função |
| :--- | :--- |
| `sudo` | Executa um comando com privilégios de superusuário (root). |
| `su` | Troca para outro usuário (normalmente root). |
| `whoami` | Mostra o nome do usuário atualmente logado. |
| `chmod` | Altera as permissões de leitura, escrita e execução de um arquivo/pasta. |
| `chown` | Altera o dono (owner) e/ou o grupo de um arquivo/pasta. |
| `useradd` / `userdel` | Adiciona ou remove um usuário do sistema. |
| `passwd` | Define ou altera a senha de um usuário. |

## 📊 5. Monitoramento do Sistema e Processos

Fique de olho no desempenho e no que está rodando.

| Comando | Função |
| :--- | :--- |
| `df` | Mostra o uso do disco em todas as partições montadas. |
| `du` | Mostra o tamanho de uma pasta e do seu conteúdo. |
| `top` | Exibe processos em execução e consumo de recursos em tempo real. |
| `htop` | Lista e gerencia processos (interface mais amigável e colorida). |
| `ps` | Mostra um resumo dos processos em um momento específico (snapshot). |
| `uname` | Exibe informações do kernel e do sistema operacional. |
| `time` | Mede o tempo total de execução de um comando ou programa. |
| `systemctl` | Gerencia serviços (daemons) do systemd (start, stop, status, enable). |
| `watch` | Executa um comando repetidamente a cada 2 segundos (ex: `watch df -h`). |
| `jobs` | Mostra programas em execução em segundo plano no shell atual. |
| `kill` | Encerra um processo pelo seu PID (Process ID). |
| `shutdown` | Desliga o sistema de forma segura. |
| `history` | Mostra uma lista numerada de todos os comandos executados anteriormente. |
| `man` | Abre o manual oficial de um comando (ex: `man grep`). |

## 🌐 6. Comandos de Rede

Conectividade, diagnósticos e transferências.

| Comando | Função |
| :--- | :--- |
| `hostname` | Mostra o nome do host (computador) na rede. |
| `ping` | Envia pacotes ICMP para um destino (testa conectividade básica). |
| `wget` | Baixa arquivos da internet via HTTP/HTTPS/FTP. |
| `curl` | Transfere dados de/para uma URL (suporta incontáveis protocolos). |
| `ip` | Gerencia e mostra configurações de rede (substitui o antigo `ifconfig`). |
| `netstat` | Exibe informações de rede (portas abertas, tabelas de roteamento). |
| `ss` | Utilitário moderno que substitui o `netstat`. Ex: `ss -tulpn` (mostra portas abertas). |
| `traceroute` | Mostra o caminho (roteadores) que os pacotes percorrem até o destino. |
| `nslookup` | Consulta informações de DNS (descobre o IP de um domínio). |
| `dig` | Exibe detalhes avançados de um domínio (DNS). |
| `scp` | Copia arquivos de forma segura entre dois sistemas via SSH. |
| `rsync` | Sincroniza arquivos de forma eficiente entre dois sistemas pela rede. |

## 🧹 7. Limpeza e Manutenção

Mantenha seu Fedora sempre limpo e rápido.

| Comando | Função |
| :--- | :--- |
| `sudo dnf clean all` | Limpa todos os caches do DNF. |
| `sudo dnf autoremove` | Remove pacotes órfãos (dependências não usadas). |
| `journalctl --vacuum-size=200M` | Limpa os logs antigos do sistema, mantendo apenas os últimos 200MB. |

## 🚀 8. Dicas Ninja e Atalhos

Para ganhar produtividade no dia a dia.

| Comando | Função |
| :--- | :--- |
| `!!` | Executa o último comando novamente. **Exemplo clássico:** `sudo !!` (roda o comando anterior com sudo). |
| `Ctrl + L` | Limpa a tela do terminal (equivalente ao comando `clear`). |
| `Tab` | Tecla mágica do **autocomplete**. Digite o início e aperte Tab para completar comandos ou caminhos. |
| `<comando> --help` | Mostra um resumo rápido das opções mais usadas de qualquer comando. |

## 🤝 Como Contribuir

Sinta-se à vontade para abrir uma *Issue* ou um *Pull Request* se quiser adicionar mais comandos, corrigir alguma informação ou sugerir uma melhoria na organização.

1.  Faça um *Fork* do projeto.
2.  Crie uma branch para sua feature (`git checkout -b feature/NovoComando`).
3.  Commit suas mudanças (`git commit -am 'Adiciona comando XYZ'`).
4.  Push para a branch (`git push origin feature/NovoComando`).
5.  Abra um novo *Pull Request*.

## 📜 Licença

Este projeto está sob a licença MIT. Consulte o arquivo [LICENSE](LICENSE) para mais informações.

---
⭐ **Se este repositório te ajudou, não se esqueça de deixar uma estrela!** ⭐
