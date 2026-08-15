# Verificador de Palíndromos

Este projeto verifica se um texto é um palíndromo, ou seja, se pode ser lido da mesma forma de trás para frente. O programa também ignora espaços, pontuação e diferenças entre letras maiúsculas e minúsculas convertendo todo o texto para minúsculo.


## Instalação:
Para executar o projeto, é necessário **apenas** ter o Python 3 instalado.

## Como executar:
- Salve o código em um arquivo chamado main.py
- execute no terminal: python main.py

# Exemplo:

## Entrada 
- texto1 = "A sacada da casa de cadasa"
- texto2 = "Socorram-me, subi no ônibus em Marrocos"
```python
import re

def analisar(entrada):
    if entrada is None:
        return False
    
    # Remove tudo que não for letra ou número e converte para minúsculas
    limpa = re.sub(r'[^a-zA-Z0-9]', '', entrada).lower()
    
    # Inverte a string usando fatiamento (slicing)
    invertida = limpa[::-1]
    
    return limpa == invertida

if __name__ == "__main__":
    texto1 = "A sacada da casa de cadasa"
    texto2 = "Socorram-me, subi no ônibus em Marrocos"

    print(f"Teste 1: {analisar(texto1)}")
    print(f"Teste 2: {analisar(texto2)}")
```

## Saída
- False
- True
```python

    print("false");
    print("True");
```

# Lógica do algoritmo
## *A função analisa e recebe um texto a partir disso ela verifica se ele é um palíndromo.*

- Primeiro, verifica se a entrada é None.
- Depois, remove caracteres especiais, espaços e pontuação.
- Converte todas as letras para minúsculas.
- Inverte o texto usando a função [::-1].
- Compara o texto original com o texto invertido.
- Retorna True quando os dois textos são iguais e False caso contrário.
