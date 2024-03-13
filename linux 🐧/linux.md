# LINUX commands

    basic - 
        whoami -> retorna o usuário 

        echo -> 'ecoar algo'
        
        echo -> $0 -> ecoar pasta atual

        history -> histórico de comandos


    gerenciando pacotes - 
        apt (advanced package tools) -
            apt list -> listar os pacotes na maquina

            apt update -> atualizar os pacotes mais utilizados

            apt install <packageName> -> instalar um pacote

            apt remove <packageName> -y -> desinstalar um pacote


    sistema de arquivos -
        (https://www.thegeekstuff.com/2010/09/linux-file-system-structure/)
        
        / (C:\ do linux)

        # -> root (maior privilégio do linux)

        ls -> listar os diretórios
            ls -1 -> listar um abaixo do outro
            ls -l -> inforamções sobre cada diratório

        pwd (print working directory) -> retorna o diretório atual

        cd (change directory) -> muda para o diretório especificado

        cd ~ -> muda para o "home"

        mkdir <name> (make directory) -> cria um diretório

        mv <oldName> <newName> -> renomear diretório / arquivos

        touch <name.extension> -> criar arquivos

        rm <name> ->  remover arquivos 

        rm -r <name> -> remover diretórios
        
        editando arquivos -
        	cat <archiveName> ->  visualizar o arquivo todo sem abrir
        	
        	more <archiveName> ->  visualizar x% do arquivo sem abrir
        	
        	cat <archiveName1> <archiveName2> -> copia do primeiro para o segundo
        	
        GREP - global expression print 
        	grep <word> <archive> -> procura por uma pavra dentro de um arquivo
        	grep <word> <archive1> <archive2> -> busca em mais de um arquivo ao mesmo tempo
        	
        	grep -i -r <word> . -> buscar dentro de um diretorio 
        	
        FIND - procurar por arquivos
        	find -> busca os arquivos no seu diretório
        	
        	find <directoryName> -> busca os arquivos no diretório
        	
        	find -type <f/d> - buscar pelo tipo (f - file / d - directory) 
        	 
		find -type f -name "<archiveName>" - buscar um arquivo / diretório especifico 
		
		find -type f -name "<word*>" - buscar um arquivo / diretório que contenha o que antecede o *
		
		
	Multiplos comandos - 
		mkdir beck; cd beck; echo ok -> separar os comando por ;
		
		mkdir beck && cd beck && echo ok -> se algum falhar ele para 
	
	Gerenciando processos - 
		ps -> verificar os processos em andamento
		kill <pid> - matar um processo (pid - process id)
		
	Gerenciamento de usuários - 
		useradd -m <name> -  adiciona um usuário
		
		 docker exec -it -u <user> 214436f0009e bash -> logar em outro terminal com o usuario criado
		 
		
	Gerenciamento de grupos - 
		groups <user> - ver os grupos de um usuario
		
		groupadd <name> -> adicionar um novo grupo
		
		usermod -G <groupName> <user> -> adicionar um usuario a um grupo
		
	
	Permissões de arquivo - 
		d -> directory 
		- -> archive
		r -> read
		w -> write
		x -> execute 
		
		1° - usuário 
		2° - grupo 
		3° - outros
		
		
		chmod u+<letter> <file/directory> -> adicionar permissão  
		
