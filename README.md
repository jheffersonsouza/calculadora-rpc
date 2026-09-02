# Calculadora RPC

Atividade TL1 da disciplina de Sistemas Distribuídos, ministrada pelo
Prof. Dr. Julio Cesar. UFC, Campus Jardins de Anita, Itapajé.

A tarefa era montar uma calculadora usando RPC. O roteiro da disciplina traz o
código pronto da adição, e o trabalho era estender para as outras três
operações: subtração, multiplicação e divisão. O cliente manda os dois números
pela rede, o servidor faz a conta e devolve o resultado.

Autores: Jhefferson Abrahão Alves Barbosa Souza e Pablo Pinto Barbosa.

## Como rodar

Instale as dependências:

```
sudo apt-get install rpcsvc-proto rpcbind libtirpc-dev
```

Compile:

```
make -f Makefile.calc
```

Em um terminal, suba o servidor:

```
./calc_server
```

Em outro, chame o cliente:

```
./calc_client localhost add 10 20
```

As operações são `add`, `sub`, `mul` e `div`. O cliente imprime o resultado:

```
Result:30
```
