📦 dev_aberto - Pacote Básico para Distribuição Python
Este repositório contém o código-fonte de um pacote Python simples (dev_aberto) criado para demonstrar as etapas de distribuição de software via pip e conteinerização com Docker.

O projeto faz parte das atividades da disciplina [Nome da Disciplina].

🔗 Links Úteis
Repositório da Disciplina: [Cole aqui o link para o repositório principal da disciplina]

Seu Perfil TestPyPI: [Cole aqui o link do seu perfil no TestPyPI após o registro]

🚀 Instalação do Pacote
Você pode instalar este pacote a partir do TestPyPI usando o pip.

1. Instalação (via TestPyPI)
Para instalar a versão mais recente do seu pacote, execute o comando, substituindo dev_aberto_SeuNome pelo nome que você usou no seu setup.py:

Bash

pip install --index-url https://test.pypi.org/simple/ dev_aberto_SeuNome
2. Uso como Script Executável
Após a instalação, o script hello.py estará disponível diretamente no seu sistema como um comando:

Bash

hello
3. Uso como Módulo Python
Você pode importar a função principal do pacote em seus próprios scripts:

Python

# Seu script Python
from dev_aberto import hello

# Exemplo de uso da função hello
mensagem = hello()
print(mensagem)
🛠️ Estrutura do Projeto
A estrutura do diretório segue o padrão básico para pacotes distribuíveis em Python:

package_example/
├── dev_aberto/         # Diretório do Módulo Principal
│   ├── __init__.py     # Marca como pacote e simplifica imports (e.g., from dev_aberto import hello)
│   └── dev_aberto.py   # Arquivo com a lógica do pacote (e.g., a função hello)
├── scripts/            # Contém scripts executáveis (e.g., hello.py)
├── setup.py            # Configuração para o pip (distribuição)
├── requirements.txt    # Lista de dependências para ambiente de desenvolvimento
├── README.md           # Este arquivo
└── LICENSE             # Licença MIT
⚙️ Configurações e Desenvolvimento
Pré-requisitos
Python 3.x

Pip

Setuptools

Twine (para upload no PyPI)

Docker (para a segunda parte do desafio)

Instalação em Modo de Edição
Para desenvolver ou testar o pacote localmente sem precisar publicá-lo:

Clone o repositório.

Navegue até o diretório raiz (package_example/).

Instale no modo editável:

Bash

pip install -e .
Criação e Upload do Pacote
Para criar e subir o pacote para o TestPyPI:

Bash

# 1. Cria o pacote sdist
python setup.py sdist

# 2. Faz o upload (necessita do Twine instalado: pip install twine)
twine upload --repository-url https://test.pypi.org/legacy/ dist/*
🐳 Desafio Docker (Challenge Server)
O objetivo desta seção é criar um Dockerfile robusto para implantar o Challenge Server de forma automática e persistente.

[Nesta seção, você pode incluir o seu Dockerfile e o comando de execução para o servidor, demonstrando que completou a segunda parte do desafio.]

Bash

# Exemplo de comando para construir e rodar a imagem Docker:
docker build -t challenge-server .
docker run -d -p 8080:8080 -v desafio_data:/app/data challenge-server
📝 Licença
Este projeto está licenciado sob a Licença MIT.
