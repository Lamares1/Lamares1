# Define uma função que recebe uma lista ordenada e um elemento a ser buscado
def pesquisa_binaria(lista, elemento):
  # Inicializa os índices da esquerda e da direita da lista
  esquerda = 0
  direita = len(lista) - 1
  # Enquanto a esquerda for menor ou igual à direita
  while esquerda <= direita:
    # Calcula o índice do meio da lista
    meio = (esquerda + direita) // 2
    # Se o elemento for igual ao valor do meio da lista
    if elemento == lista[meio]:
      # Retorna o índice do meio
      return meio
    # Se o elemento for menor que o valor do meio da lista
    elif elemento < lista[meio]:
      # Atualiza o índice da direita para o meio - 1
      direita = meio - 1
    # Se o elemento for maior que o valor do meio da lista
    else:
      # Atualiza o índice da esquerda para o meio + 1
      esquerda = meio + 1
  # Se o elemento não for encontrado, retorna -1
  return -1

# Define uma lista ordenada de exemplo
lista = [1, 3, 4, 7, 8, 9, 10, 45, 50, 90, 100, 150, 600, 1000]
# Define um elemento a ser buscado
elemento = 90
# Chama a função de pesquisa binária e armazena o resultado
resultado = pesquisa_binaria(lista, elemento)
# Se o resultado for diferente de -1
if resultado != -1:
  # Imprime uma mensagem informando que o elemento foi encontrado e o seu índice
  print(f"Elemento {elemento} encontrado no índice {resultado}.")
# Se o resultado for igual a -1
else:
  # Imprime uma mensagem informando que o elemento não foi encontrado
  print(f"Elemento {elemento} não encontrado.")
  
