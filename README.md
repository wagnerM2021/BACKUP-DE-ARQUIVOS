🔎 Função do Script
Interface inicial

Mostra título e instruções para o usuário digitar as pastas que deseja copiar.

Exemplo: C:\Users\Desktop;C:\Users\Documents.

Entrada de dados

O usuário informa:

As pastas de origem (separadas por ;).

O destino onde será salvo o backup.

Validação

Se o usuário não informar nada, o script encerra com aviso.

Criação da pasta destino

Gera uma subpasta com data e hora atuais no nome, para organizar os backups.

Exemplo: Backup_2026-07-15_10-22.

Log de execução

Cria um arquivo backup_log.txt dentro da pasta destino.

Registra início, erros (como pastas não encontradas) e conclusão.

Processo de backup

Usa o comando robocopy para copiar cada pasta informada:

/E → copia todos os arquivos e subpastas.

/R:2 → tenta recopyar 2 vezes em caso de erro.

/W:2 → espera 2 segundos entre tentativas.

/COPY:DAT → copia dados, atributos e timestamps.

/DCOPY:T → mantém timestamps das pastas.

/LOG+ → adiciona informações ao log.

/TEE → mostra no console e grava no log ao mesmo tempo.

Finalização

Exibe mensagem de conclusão.

Mostra onde o log foi salvo e qual é a pasta destino.

📂 Em resumo
Esse script:

Pergunta quais pastas você quer salvar.

Pergunta onde salvar.

Cria uma pasta organizada por data/hora.

Copia tudo com o robocopy.

Gera um log detalhado do processo.

É uma forma prática de automatizar backups sem precisar de programas externos.
