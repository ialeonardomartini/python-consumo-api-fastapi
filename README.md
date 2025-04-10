# 🍔 Projeto - Consumo de API com FastAPI

Este repositório foi desenvolvido durante o curso [Python: avance na Orientação a Objetos e consuma API](https://cursos.alura.com.br/course/python-avance-orientacao-objetos-consuma-api) da Alura.

O projeto une conceitos de orientação a objetos com consumo de APIs externas e criação de endpoints com FastAPI.

---

## 🚀 Aprendizados

Durante o desenvolvimento deste projeto, os seguintes tópicos foram abordados:

- ✅ Herança e classes abstratas em Python
- ✅ Polimorfismo e reuso de código
- ✅ Criação e uso de ambientes virtuais
- ✅ Consumo de APIs com `requests`
- ✅ Manipulação e persistência de dados com arquivos JSON
- ✅ Estruturação de APIs com **FastAPI**
- ✅ Criação de endpoints e parâmetros de consulta
- ✅ Testes de rotas com navegador e ferramentas como `httpie`

---

## 📂 Estrutura do Projeto

```
├── app.py                 # Script que consome a API externa e salva os dados em arquivos JSON
├── main.py                # API construída com FastAPI
├── requirements.txt       # Dependências do projeto
└── *.json                 # Arquivos de cardápio gerados automaticamente por restaurante
```

---

## ⚙️ Como instalar e rodar o projeto

1. **Clone o repositório**
```bash
git clone https://github.com/ialeonardomartini/python-consumo-api-fastapi.git
cd python-consumo-api-fastapi
```

2. **Crie e ative um ambiente virtual**
```bash
python -m venv venv
source venv/bin/activate     # Linux/macOS
venv\Scripts\activate        # Windows
```

3. **Instale as dependências**
```bash
pip install -r requirements.txt
```

4. **Execute a API com Uvicorn**
```bash
uvicorn main:app --reload
```

A API estará disponível em `http://127.0.0.1:8000`.

---

## 🔌 Endpoints da API

### `GET /api/hello`
Mensagem de teste simples.

**Resposta:**
```json
{
  "Hello": "World"
}
```

---

### `GET /api/restaurantes/`
Retorna o cardápio de todos os restaurantes da API externa.

### `GET /api/restaurantes/?restaurante=McDonald’s`
Retorna apenas o cardápio do restaurante informado.

**Exemplo de resposta:**
```json
{
  "Restaurante": "McDonald’s",
  "Cardapio": [
    {
      "item": "Big Mac",
      "price": "$5.99",
      "description": "Hambúrguer clássico com dois hambúrgueres, alface, queijo, molho especial..."
    }
  ]
}
```

---

## 🧾 Sobre a API externa utilizada

Os dados foram obtidos da URL:

```
https://guilhermeonrails.github.io/api-restaurantes/restaurantes.json
```

Essa API simula um banco de dados com cardápios de grandes redes de fast food.

---

## 💡 Melhorias futuras

- Adicionar testes automatizados com `pytest`
- Criar uma interface web com `Streamlit` ou `Flask`
- Publicar a API em nuvem (Render, Railway, Vercel)

---

## 👨‍🏫 Créditos

Projeto desenvolvido com base no curso da Alura com orientação de [Guilherme Lima](https://cursos.alura.com.br/user/guilhermeonrails) e [Laís Urano](https://cursos.alura.com.br/user/lais-urano).

---

## 📜 Licença

Este projeto está licenciado sob a licença MIT. Sinta-se à vontade para usar e modificar!
