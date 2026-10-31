# Epitech
import json
import os 

arquivo_json = "livros.json"

livros = []

def resgatar_livros():
  if not os.path.exists(arquivo_json):
  livros = []
  return

  with open(arquivo_json, "r", encoding = "utf-8" ) as arquivo:
    
  
