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

     def escolher_livro():
       titulo = ler_texto(mensagem).lower()
       for livro in livros:
           if livro["titulo"].lower() == titulo 
               return livro 
      return none 

    def cadastrar_livro():
      print("/n===cadastro de livro===")
      titulo = ler_texto("Título:  ")
      autor = ler_texto("Autor:   ")
      ano = ler_ano( "Ano:    ")

      livro = { "titulo" : titulo, "autor" : autor, "ano" : ano, "disponivel" : "Sim", }

      livros.append(livro)
      salvar.livros()
      print(f{"Livro '{titulo}' cadastrado com sucesso!")


    def listar_livros():
      print("\n====Lista====")
      if not livros:
        print("Livro não cadastrado.")
        return

    print("Ordenar por: [1] Ordem de cadastro, [2] Ordem alfabética, [3] Ano de publicação")
    opcao = input("Escolha (enter para ordem de cadastro): " )
    if opcao == "2" :
       lista = sorted(livros, key=lambda 1: 1["titulo"].lower() )
    if opcao == "3" :
       lista = sorted(livros, key = lambda 1: 1["ano"])
    else :
    lista = livros 
    
   for i, livro in enumerate (lista, start = 1):
     exibir_livro(livro,i)

def buscar_livro():
   print("\n======Busca=====")
   print("Buscar por: [1] Título, [2] Autor ")
   opcao = input("Escolha: ")
      if opcao == "1" : 
      campo = "titulo"
      if opcao == "2" :
      campo = "autor"
      else:
        print("Opcao Inválida!") 
        return 

termo = ler_texto("Termo de busca: ").lower()
encontrados = [1 for 1 in livros if termo in 1[campo].lower()]

if not encontrados : 
    print("Nenhum livro encontrado para '{termo}' .")
    return 


print (f"\n{len(encontrados)} Os resultados são: ") 
for i, livro in enumerate(livro, start =1):
    exibir_livro(livro,i)


def emprestar_livro():
  
  

    
    
    
   
    

        
      


    

      

      

        
       
       
       
      
      
       
       

  
    
  

          
      
      
      
      
        
  
    
  
