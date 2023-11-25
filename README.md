# config-git-bash-here

Essa configuração serve para quando estiver na pasta do seu projeto e for necessário utilizar o gitbash, apenas com click do botão direito na pasta, aparece a opção de abrir o gitbash ja com diretório na pasta de abertura.

1 - Abra um novo bloco de notas e salve o documento com o nome "OpenGitBash.reg" e o tipo como **todos os arquivos**.

2 - Cole o seguinte script dentro desse documento em branco, ignorando os (---) no inicio e no fim do código:

-----------------------------------------------------------------------

Windows Registry Editor Version 5.00
; Open files
; Default Git-Bash Location C:\Program Files\Git\git-bash.exe
[HKEY_CLASSES_ROOT\*\shell\Open Git Bash]
@="Open Git Bash"
"Icon"="C:\\Program Files\\Git\\git-bash.exe"
[HKEY_CLASSES_ROOT\*\shell\Open Git Bash\command]
@="\"C:\\Program Files\\Git\\git-bash.exe\" \"--cd=%1\""
; This will make it appear when you right click ON a folder
; The "Icon" line can be removed if you don't want the icon to appear
[HKEY_CLASSES_ROOT\Directory\shell\bash]
@="Open Git Bash"
"Icon"="C:\\Program Files\\Git\\git-bash.exe"
[HKEY_CLASSES_ROOT\Directory\shell\bash\command]
@="\"C:\\Program Files\\Git\\git-bash.exe\" \"--cd=%1\""
; This will make it appear when you right click INSIDE a folder
; The "Icon" line can be removed if you don't want the icon to appear
[HKEY_CLASSES_ROOT\Directory\Background\shell\bash]
@="Open Git Bash"
"Icon"="C:\\Program Files\\Git\\git-bash.exe"
[HKEY_CLASSES_ROOT\Directory\Background\shell\bash\command]
@="\"C:\\Program Files\\Git\\git-bash.exe\" \"--cd=%v.\""

-----------------------------------------------------------------------

3 - Clique no arquivos 2 vezes e execute.

4 - Feito isso, ja estará disponivel a opção "Open to GitBash" no seu Windows.
