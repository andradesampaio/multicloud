# Comandos Git
git config --list

git config --global user.name "Andrade Sampaio"
git config --global user.email "teste@gmail.com"

git config --global color.ui auto
git config --global core.editor vim

# Confira as configurações:
git config --list

# Criação do repositório com o comando
git init

# Checar o status do repositório.
git status

# Fazendo um commit. 
# Para isso é preciso adicionar todos os arquivos e as alterações no "pacote" (no commit):
git add --all
git status


# Para realizar um commit você sempre precisa redigir uma mensagem 
# Como por exemplo, "Corrigindo o Bug X", "Adicionando a Feature Y", etc. Em nosso caso estamos criando o arquivo Readme:
git commit -m "Criando o Readme"

# Veja o histórico de versões do seu repositório:
git log
git log -p

# Cadastro da Chave SSH

# Comando para gerar a chave e dê enter para todas opções mantendo a default:
ssh-keygen

# Copie o hash de sua chave SSH através do comando:
cat ~/.ssh/id_rsa.pub

# Na sequência precisamos voltar em nosso repositório local no terminal e informar qual será o nosso repositório remoto no GitHub conforme instruções na página do GitHub.
git remote add origin git@github.com:andradesampaio/firstrepo.git

# Agora podemos enviar nosso primeiro commit para um repositório remoto:
git push -u origin master

# Caso você tenha mexido no arquivo de forma errada, você pode desfazer essa ação antes de adicioná-la no próximo commit executando o comando abaixo:
git checkout -- README.md