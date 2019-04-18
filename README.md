# ShowTheAtomDataManipulation
![linguagem](https://img.shields.io/badge/Python-2.7-brightgreen.svg)
![versão](https://img.shields.io/badge/version-v0.2-orange.svg)
Script for Manipulation of Data of Project Show The Atom

 - **Situação atual**:
	 ````
	 def sitAtual():
	     r = requests.get('http://ffc3ed57.ngrok.io/atoms')
	     print r.json()
	 ````
 - **Inserir Dados**:
	 ````
	 def insert(id, name, numatom, description):
	     descricao = open(description)
	     descricao = descricao.read()
	     r = requests.post('http://ffc3ed57.ngrok.io/atom', data={'id': id,'element': name, 'numatom': numatom, 'description': descricao})
	     print r.status_code
	     print r.text 
	 ````
- **Deletar Dados**:
	````
	def delete(id):
	    link = 'http://ffc3ed57.ngrok.io/atom/' + id
	    r = requests.delete(link)
	    print r.status_code
	    print r.text
	````
- **Atualizar Dados**:
	````
	def atualizar(id, name, numatom, description):
	    descricao = open(description)
	    descricao = descricao.read()[:-1]
	    r = requests.patch('http://ffc3ed57.ngrok.io/atom/'+str(id), data={'id': id ,'element': name, 'numatom': numatom, 'description': descricao})
	    print r.status_code
	    print r.text
	````




`

