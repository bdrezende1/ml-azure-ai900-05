# ml-azure-ai900-05
Abordaremos o Copiloto e exploraremos os recursos da OpenAI, concentrando-nos tanto nos filtros de conteúdo quanto na criação. 

---

Vamos lá, vou reescrever em primeira pessoa, assim fica mais fácil para quem está lendo se identificar com o processo.

---

### Laboratório de IA Generativa com Azure

**Passo 1: Criar uma Conta no Azure**
Primeiro, preciso criar uma conta no Azure, caso ainda não tenha uma. Acesso [o site do Azure](https://azure.microsoft.com/) e clico em "Iniciar gratuitamente". Sigo as instruções para criar minha conta.

**Passo 2: Criar um Recurso de Serviço Cognitivo**
Para trabalhar com IA generativa, preciso criar um recurso de Serviço Cognitivo:
1. No portal do Azure, clico em `Criar um recurso`.
2. Seleciono `Inteligência Artificial e Machine Learning`, depois `Serviços Cognitivos`.
3. Clico em `Criar`.

**Preenchendo o Formulário de Criação:**
- **Assinatura**: Escolho minha assinatura do Azure.
- **Grupo de Recursos**: Crio um novo grupo de recursos ou uso um existente.
- **Nome**: Escolho um nome para o meu recurso.
- **Região**: Seleciono a região mais próxima de mim.
- **Plano de Tarifa**: Escolho um plano gratuito se estiver disponível.
- Clico em `Revisar + Criar`, e depois em `Criar`.

**Passo 3: Obter as Chaves e o Endpoint**
Depois de criar o recurso, preciso das chaves de acesso e do endpoint:
1. Navego até meu recurso de Serviço Cognitivo.
2. No menu à esquerda, clico em `Chaves e Endpoint`.
3. Anoto as duas chaves e o endpoint fornecidos.

**Passo 4: Configurar meu Ambiente de Desenvolvimento**
Para interagir com os serviços cognitivos, configuro meu ambiente de desenvolvimento. Se estiver usando Python, instalo as bibliotecas necessárias:
```bash
pip install openai
```

**Passo 5: Escrever o Código para IA Generativa**
Com o ambiente configurado, posso começar a trabalhar com IA generativa. Veja um exemplo de como gerar texto com Python:
```python
import openai

openai.api_key = 'SUA_CHAVE_AQUI'

response = openai.Completion.create(
  engine="text-davinci-003",
  prompt="Escreva uma história curta sobre um robô que queria ser humano.",
  max_tokens=100
)

print(response.choices[0].text.strip())
```

### Explorando o AI Studio

**Passo 1: Acessar o AI Studio**
O AI Studio é uma plataforma interativa onde posso explorar e experimentar com diferentes modelos de IA. Acesso [AI Studio](https://microsoftlearning.github.io/mslearn-ai-studio/Instructions/01-Explore-ai-studio.html) para iniciar.

**Passo 2: Navegar pelo AI Studio**
Ao acessar o AI Studio, vejo uma interface amigável que permite criar, treinar e testar modelos de IA. Exploro os diversos painéis e ferramentas disponíveis.

**Passo 3: Criar um Projeto no AI Studio**
1. Clico em `Novo Projeto`.
2. Dou um nome ao meu projeto e seleciono o tipo de modelo que desejo explorar, como modelos de linguagem ou visão computacional.
3. Sigo as etapas guiadas para configurar e treinar meu modelo.

**Passo 4: Testar o Modelo**
Depois de treinar meu modelo, posso testá-lo diretamente no AI Studio. Insiro dados de teste e observo os resultados gerados pelo modelo.

### Filtros de Conteúdo no AI Studio

**Passo 1: Configurar Filtros de Conteúdo**
Os filtros de conteúdo são usados para garantir que o conteúdo gerado pela IA esteja de acordo com minhas políticas de uso. Acesso [Explore Content Filters](https://microsoftlearning.github.io/mslearn-ai-studio/Instructions/06-Explore-content-filters.html) para mais detalhes.

**Passo 2: Ativar e Ajustar Filtros**
1. No AI Studio, vou para as configurações do projeto.
2. Ativo os filtros de conteúdo e ajusto as configurações conforme necessário para filtrar linguagem imprópria, conteúdo sensível, etc.

**Passo 3: Testar Filtros de Conteúdo**
Testo os filtros de conteúdo gerando várias saídas do modelo e verificando se os filtros estão funcionando conforme o esperado.

https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/12-generative-ai.html
https://microsoftlearning.github.io/mslearn-ai-studio/Instructions/01-Explore-ai-studio.html
https://microsoftlearning.github.io/mslearn-ai-studio/Instructions/06-Explore-content-filters.html
