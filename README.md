# Guia de Python: Aprenda a Linguagem de Programação Mais Versátil
Python é uma linguagem de programação de alto nível, conhecida por sua sintaxe simples e legibilidade, tornando-a ideal tanto para iniciantes quanto para desenvolvedores experientes. Criada por Guido van Rossum e lançada pela primeira vez em 1991, Python se destaca por sua facilidade de uso e ampla aplicação em áreas como desenvolvimento web, automação de scripts, análise de dados, inteligência artificial e aprendizado de máquina.

## Variáveis e Tipos
 ```
# Strings
nome = "João"

# Inteiros
idade = 30

# Floats
altura = 1.75

# Booleanos
is_estudante = True
```
## Operadores Aritméticos
```
# Aritméticos (3 % 2 = 1) | 4² = 4 * 4
sum = num1 + num2
sub = num1 - num2
div = num1 / num2
mult = num1 * num2
mod = num1 % num2
exp = num1 ** num2

# Comparação
maior = num1 > num2
menor = num1 < num2
igual = num1 == num2
diferente = num1 != num2
maior_igual = num1 >= num2
menor_igual = num1 <= num2

# Atribuição
num1 += 1 # num1 = num1 + 1
num1 -= 1 # num1 = num1 - 1
num1 *= 1 # num1 = num1 * 1
num1 /= 1 # num1 = num1 / 1
```
## Listas
```
# Criação
frutas = ["maçã", "banana", "laranja"]

# Acessar elemento
primeira_fruta = frutas[0]

# Adicionar elemento
frutas.append("uva")

# Remover elemento
frutas.remove("banana")
```
## Dicionários
```
# Criação
pessoa = {
    "nome": "Maria",
    "idade": 25,
    "cidade": "São Paulo"
}

# Acessar valor
nome = pessoa["nome"]

# Adicionar novo par chave-valor
pessoa["profissao"] = "Engenheira"
```
## Estruturas de Controle
```
# If-Else
idade = 18
if idade >= 18:
    print("Maior de idade")
else:
    print("Menor de idade")

# For Loop
for i in range(5):
    print(i)

# While Loop
contador = 0
while contador < 5:
    print(contador)
    contador += 1
```
## Funções
```
# Definição de função
def saudacao(nome):
    return f"Olá, {nome}!"

# Chamada de função
mensagem = saudacao("Ana")
print(mensagem)

# Função com valor padrão
def potencia(base, expoente=2):
    return base ** expoente

resultado = potencia(3)  # Retorna 9
```
## Classes e Objetos
```
class Pessoa:
    def __init__(self, nome, idade):
        self.nome = nome
        self.idade = idade
    
    def apresentar(self):
        print(f"Olá, eu sou {self.nome} e tenho {self.idade} anos.")

pessoa1 = Pessoa("João", 25)
pessoa1.apresentar()
```
```
class Carro:
    def __init__(self, marca, modelo):
        self.marca = marca
        self.modelo = modelo
    
    def descricao(self):
        return f"{self.marca} {self.modelo}"

meu_carro = Carro("Toyota", "Corolla")
print(meu_carro.descricao())
```
## Manipulação de Arquivo
```
# Escrita em arquivo
with open("arquivo.txt", "w") as f:
    f.write("Olá, mundo!")

# Leitura de arquivo
with open("arquivo.txt", "r") as f:
    conteudo = f.read()
    print(conteudo)

```
```
# Leitura de arquivo
with open('arquivo.txt', 'r') as f:
    conteudo = f.read()

# Escrita em arquivo
with open('novo_arquivo.txt', 'w') as f:
    f.write("Olá, mundo!")
```
## Exceções
```
try:
    numero = int(input("Digite um número: "))
    resultado = 10 / numero
    print(resultado)
except ValueError:
    print("Entrada inválida")
except ZeroDivisionError:
    print("Não é possível dividir por zero")
finally:
    print("Operação concluída")
```
## Compreensão de Lista
```
# Criar uma lista de quadrados
quadrados = [x**2 for x in range(10)]

# Filtrar números pares
numeros = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
pares = [x for x in numeros if x % 2 == 0]
```
## Módulo e Importações
```
# Importar módulo completo
import math

# Importar função específica
from random import randint

# Importar com alias
import numpy as np
```
## Manipulação de Strings
```
# Concatenação
nome = "Maria"
sobrenome = "Silva"
nome_completo = nome + " " + sobrenome

# Formatação
idade = 30
mensagem = f"{nome} tem {idade} anos"

# Métodos de string
texto = "python é incrível"
print(texto.capitalize())
print(texto.upper())
print(texto.split())
```
## Funções Lambda
```
# Função lambda simples
quadrado = lambda x: x**2

# Uso com map()
numeros = [1, 2, 3, 4, 5]
quadrados = list(map(lambda x: x**2, numeros))
```
## Decoradores
```
def meu_decorador(funcao):
    def wrapper():
        print("Antes da função")
        funcao()
        print("Depois da função")
    return wrapper

@meu_decorador
def saudacao():
    print("Olá, mundo!")
```
## Geradores
```
def contador(max):
    n = 0
    while n < max:
        yield n
        n += 1

for num in contador(5):
    print(num)
```
## Expressões Regulares
```
import re

texto = "O número de telefone é 123-456-7890"
padrao = r'd{3}-d{3}-d{4}'
match = re.search(padrao, texto)
if match:
    print(f"Número encontrado: {match.group()}")

# Substituição com regex
novo_texto = re.sub(r'd', 'X', texto)
print(novo_texto)
```
## Trabalhando com JSON
```
import json

# Dicionário para JSON
dados = {"nome": "João", "idade": 30}
json_string = json.dumps(dados)
print(json_string)

# JSON para dicionário
json_string = '{"nome": "Maria", "idade": 25}'
dados = json.loads(json_string)
print(dados["nome"])
```
## Intertools
```
from itertools import permutations, combinations, product

# Permutações
print(list(permutations([1, 2, 3])))

# Combinações
print(list(combinations([1, 2, 3, 4], 2)))

# Produto cartesiano
print(list(product([1, 2], ['a', 'b'])))
```
## Decoradores com Argumentos
```
def repetir(vezes):
    def decorador(funcao):
        def wrapper(*args, **kwargs):
            for _ in range(vezes):
                resultado = funcao(*args, **kwargs)
            return resultado
        return wrapper
    return decorador

@repetir(3)
def saudacao(nome):
    print(f"Olá, {nome}!")

saudacao("Maria")
```
## Context Managers
```
from contextlib import contextmanager

@contextmanager
def gerenciar_arquivo(nome_arquivo):
    try:
        f = open(nome_arquivo, 'w')
        yield f
    finally:
        f.close()

with gerenciar_arquivo('teste.txt') as arquivo:
    arquivo.write('Olá, mundo!')
```
## Manipulação de Data e Hora
```
from datetime import datetime, timedelta

# Data e hora atual
agora = datetime.now()
print(agora)

# Formatação de data
print(agora.strftime("%d/%m/%Y %H:%M:%S"))

# Operações com datas
amanha = agora + timedelta(days=1)
print(amanha)
```
## Programação Orientada a Objetos (POO)
```
class Animal:
    def __init__(self, nome):
        self.nome = nome
    
    def falar(self):
        pass

class Cachorro(Animal):
    def falar(self):
        return f"{self.nome} faz Au Au!"

class Gato(Animal):
    def falar(self):
        return f"{self.nome} faz Miau!"

rex = Cachorro("Rex")
felix = Gato("Felix")
print(rex.falar())
print(felix.falar())
```
