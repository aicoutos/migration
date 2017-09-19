# plain2sql
:pencil: Converte arquivos de texto para tabelas SQL

## Composer
	composer require plain2sql/plain2sql
	
## tables/user (o nome do arquivo é o nome da tabela)
```
id
name
email
passoword
token
token_expiration
```
	
## Instalação
```
<?php
require 'vendor/autoload.php';
$dir='tables';
$db=[
	'server'=>'localhost',
	'name'=>'test',
	'user'=>'root',
	'password'=>''
];
$p2s=new Plain2SQL\Plain2SQL($dir,$db);
```

## Apagar todas as tabelas (dropAll)
	$p2s->dropTables();

## Migrar todas as tabelas (migrateAll)
	$p2s->migrateAll();

## Esvaziar todas as tabelas (truncateAll)
	$p2s->truncateTables();
