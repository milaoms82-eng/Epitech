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

     
        
  
    
  
