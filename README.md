
# Comandos mais utilizados

## Configurar Git
Comandos básicos para configurar seu git
##### Definir usuário
    git config --global user.name "username"
##### Definir e-mail
    git config --global user.email "email@email.com"
##### Definir a branch padrão
	git config --global init.dafultbranch main 
##### Visualizar configurações
    git config --list

## Repositório local
Acesse a pasta que você quer utilizar pelo o terminal de sua preferencia e utilize o seguinte comando:

    git init
    
##### Verificar o estado dos arquivos:
	git status
	
##### Adicionar um arquivo para staged:
	git add nomedoarquivo.tipo
	
##### Adicionar todos os arquivos para staged:
	git add .

##### Fazer o commit das suas alterações:
	git commit -m "mensagem"
	
##### Atualizar mensagem do último commit:
	git commit-m "mensagem atualizada" --amend

##### Visualizar log dos commits:
    git log

##### Visualizar log dos commits de forma resumida:
    git log --oneline
    
##### Voltar arquivo para staged:
	 git restore --staged nomedoarquivo.tipo
    
##### Retornar arquivo para o último commit:
    git restore nome.arquivo
    
##### Desfazer último commit:
	git reset HEAD~
Obs: para desfazer mais commits basta adicionar a quantidade após o ~
Exemplo: HEAD~3 (Desfaz os últimos 3 commits)

##### Voltar para o commit e mater alterações em staged:
	git reset --soft <commit>: "Retorno Suave, Mantendo Mudanças"

##### Voltar para o commit e desfazendo o staging:
	git reset --mixed <commit>

##### Voltar para um commit e apagar as mudanças
	git reset --hard <commit>

## Alias (Novos "comandos"/atalhos)
##### Para criar um alias globalmente:
	git config --global alias.<identificador>  <comando>
Uma forma simples de visualizar os aliases configurados é usando o seguinte comando: git config --list

## Branch
##### Visualizar as branchs:
	git branch
	
##### Alterar entre as branchs:
	git checkout NomeDaBranch
ou

	git switch NomeDaBranch

##### Criar uma nova branch:
	git branch NomeDaBranch
	
##### Criar e ir para nova branch
    git checkout –b NomeDaBranch

##### Apagar uma branch:
	git branch -d NomeDaBranch

##### Fazer um merge:
	git merge -m "mensagem" NomeDaBranch

## Arquivo .gitignore
adicione "nome do arquivo.extensão" dentro do arquivo .ignore para arquivos que serão ignorados

## Repositório online
##### Para iniciar:

    git remote add origin <link do repositorio>
    git remote -v
    git push -u origin main

Ou crie o repositório no git e faça um clone do mesmo em seu computador com o comando:

	git clone link_do_repósitorio.git
	
## Git e Github

##### Push (Enviar do local para o remoto)
    git push origin main

##### Pull (Receber do remoto para o local)
    git pull




## Tag
##### Criar tag
    git tag -a "nome tag" -m "comentario"
    
##### Ver tag
    git tag

#####  Informações da tag
    git show "nome da tag"
    
##### Push da tag
    git push origin --tag
