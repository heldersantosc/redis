#criado o arquivo docker-compose com a imagem do redis 5

#para rodar o terminal no docker
`docker exec -it [container_name / container_id] /bin/bash`

#para executar o client do redis
`redis-cli`

#para criar chaves
`set mykey mykey_value`

#para criar tipo estrutura de dados
`set user:login:id`

#para recuperar auma chave
`get mykey`

#para listar todas as chaves
`keys *`

#todas as chaves com um padrão
`keys my*`

#para definir mais de uma chave ao mesmo tempo
`mset key1 value1 key2 value2`

#para recuperar varias chaves
`mget key1 key2`

#para deletar uma key
`del key1`

#verifica a tipagem da chave
`type key1`

#comando dump que retorna uma valor serializado
`dump key1`

#comando para criar uma chave sem expiração
`restore key 0 "\x00\x06helder\t\x00\xec\xc1\xee\x9d\xb5\xd2\xc7\x1d"`

#comando para verificar se existe uma chave, retorna 1 se houver
`exists key`

#comando rename para renomear
`rename key key_nova`

#comando scan por padrão exibe 10 elementos
`scan 0`

#comando object, permite inspecionar o objeto
`object refcount key`

#comandos para incrementar e decrementar números
`incr number`
`decr number`

#comando para incrementar e decrementar com valor especifico
`incrby number 5`
`decrby number 5`

#comando para incrementar e decrementar com valor especifico
`incrbyfloat real 5.4`
`decrbyfloat real 5.4`

#append em strings
`set key bem`
`append key vindo`

#getrange
`getrange key 1 4`

#setrange
`setrange key 1 " santos"`

#cria um tempo de expiração da chave
`expire key1 10`

#persist remove o tempo de vida da chave em segundos
`persiste key1`

#configuração dos parâmetros de configuração do redis no linux
`find / -name redis.conf`

#definindo a porta pelo terminal
`redis-cli -p 6378`

#configurando autenticação no redis
`redis-cli`
`CONFIG SET REQUIREPASS minhasenha`
`auth minhasenha`

#verifincando informações
`INFO`
`MONITOR`

#persistindo dados com snapshot
`save`

#persistindo dados com .aof
`nano appendonly.aof`

#criando hashes
`hset user id 1`

#criando listas com o topo da lista
`lpush lista 1 2 3 4 5 6 7 8`

#criando listas com
`rpush lista 1 2 3 4 5 6`

#inserir valor no final de uma lista
`linsert lista before 8 9`

#inserir valor em um index especifico
`lset lista 0 school`

#exibir as lista por ranges nos indices
`lrange lista 0 4`

#exibir um elemento especifico da lista
`lindex lista 2`

#exibe o tamanho
`llen lista`

#removendo o primeiro elemento
`lpop lista`

#removendo da lista
`rpop lista`
