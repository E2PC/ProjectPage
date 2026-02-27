---
title: 2. Leitura e escrita em python
layout: template
filename: 2_leitura_e_escrita_em_python
button: 2. Leitura e escrita em python
type: python
---

# Leitura e escrita

## print()

A função print é responsável pela "saída" em python, por padrão uma linha é pulada ao fim da impressão.

codigo:
```
print("bom dia!")
```

saída:
```
bom dia!

```
<br>

*Também é possivel imprimir mais de um dado por vez.

codigo:
```
print("idade:", 20)
```

saída:
```
idade: 20

```
<br>

## input()

Input é o comando de "entrada" do programa, coletando informações no terminal e inserindo no algoritmo. 

codigo:
```
variavel = input()
print(variavel)
```

entrada:
```
boa noite!
```

saída:
```
boa noite!

```
<br>

*Seu uso não é limitado a variáveis.

codigo:
```
print(input())
```

entrada:
```
azul
```

saída:
```
azul

```
<br>

É importante comentar que input() sempre vai retornar o dado no formato de uma string, independente de seu formato.
<br>
<br>

[Próxima página](./3_tipos_de_dados_e_cast_em_python.md)
[sumário](./python_sumario.md)
[Página anterior](./1_introdução_a_python.md)
