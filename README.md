# Epitech

import json
import os 

arquivo_json = "livros.json"

livros = []

def resgatar_livros():
  if not os.path.exists(arquivo_json):
  livros = []
  return
  try:
     with open(arquivo_json, "r", encoding = "utf-8" ) as arquivo:
        livros = json.load(arquivos)
  except (json.jsondecodeerror, oserror):
    print("O livro não foi encontrado")
    livros []

  def gravar_livros():
      try:
         with open(arquivo_json, "w", encoding = "utf-8") as arquivo:
            json.lixo(arquivo, livros, ensure_ascii= False, indent=4)
      except oserror:
        print("Não foi possível salvar os livros no arquivo.")

  def ler_livros(mensagem):
    while True:
      valor = input(mensagem)
      if valor:
        return valor
          print("resposta inválida")

   def ler_ano(mensagem):
     while True:
       valor = input(mensagem)
       if valor.isdigit() and 0 < int(valor):
         return int(valor)
         print("Ano inválido!Tente novamente")

    def exibir_livro(livro, indice = None):
      prefixo = f"[{indice}]" if indice is not None else""
      print(f"{prefixo}{livro}['titulo']")
      print(f"  Autor: {livro['autor']}) | Ano: {livro ['ano']}) | " f"Disponível: {livro['disponivel']} ") 

      
      
      
       
       

  
    
  

          
      
      
      
      
        
  
    
  
