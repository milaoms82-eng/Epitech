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
  print("====Empréstimo===")
  livro = escolher_livro(" Título do livro: ")
  if livro is None: 
    print("Livro não encontrado!") 
  if livro["disponivel"] == "Não" :
    print("Este livro encontra-se emprestado."
    return
livro["disponivel"] = "Não" 
salvar_livros() 
print(f"Empréstimo de '{livro['titulo']}' registrado. ")

def devolver_livros():
  print("\n====Devolução===")
  livro = escolher_livro("Título do livro:  ")
  if livro is None :
     print("Livro não encontrado.") 
     return
  if livro["disponivel"] == "Sim" :
     print(" Este livro já está disponível . ")
     return
     
 livro["disponível"] == "Sim"
 salvar_livros()
 print(f"Devolução de '{livro['titulo']}' registrada." )

 def contador_livros():
   total = len(livros)
   disponiveis = sum(1 for 1 in livros if 1["disponivel"] == 1  
   emprestados = total - disponiveis 
   print("\n===Resumo da Biblioteca===")
   print(f"Total de livros:   {total}")
   print(f"Livros disponíveis : {disponiveis}")
   print(f"Livros emprestados :  {emprestados}") 

def remover_livros():
  print("\n===Remoção de Livro===") 
  livro = escolher_livro("Título do livro a ser removido:  ")
  if livro is None :
    print("Livro não encontrado") 
    return

  confirmacao = input(f"Remover'{livro['titulo']}'? (s/n) : ") 
  if confirmação == "s" :
    livros.remove(livros)
    salvar_livros()
    print("O livro foi removido com sucesso. ")
  else: 
    print (" Remoção cancelada!") 

 def exibir_menu():
   print("===Sistema de Biblioteca===")
   print(" 1 - Cadastrar Livro ")
   print(" 2 - Listar Livros " ) 
   print(" 3 - Buscar Livro" ) 
   print(" 4 - Emprestar Livro) 
   print(" 5 - Devolver Livro) 
   print(" 6 - Resumo da Biblioteca " ) 
   print(" 7 - Remover Livro " ) 
   print(" 0 - Sair " ) 

def main():
  resgatar_livros()

acoes:{ 
"1" : cadastrar livro, 
"2" : listar_livros,
"3" : buscar_livro,
"4" : emprestar_livro, 
"5" : devolver_livro, 
"6" : contador_livros, 
"7" : remover_livro, 
} 

while True :
  exibir_menu()
  opcao = input("Escolha uma opcao")
  if opcao == "0" 
    salvar_livros()
    print("Obrigado por usar nosso sistema!")
    break
  acao= acoes.get(opcao)
  if acao :
     acao ()
  else :
    print("Opção inválida!")

  if _name_ == "_main_" :
     main()
    
    
    
    
    

   
   

   

  

    
  
  
    
  
  
  



  
    
  
  
  

    
    
    
   
    

        
      


    

      

      

        
       
       
       
      
      
       
       

  
    
  

          
      
      
      
      
        
  
    
  
