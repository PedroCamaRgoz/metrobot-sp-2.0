# MetrôBot SP 2.0

Projeto desenvolvido para a disciplina de Inteligência Artificial e Machine Learning.

O MetrôBot SP 2.0 representa parte da rede do Metrô de São Paulo como um grafo, utilizando as Linhas 1-Azul, 2-Verde e 3-Vermelha.

O sistema permite calcular rotas entre estações, considerar estações bloqueadas e condições de acessibilidade, identificar baldeações e comparar os algoritmos de busca BFS e DFS.

## Funcionalidades

- Representação da rede de metrô utilizando grafos
- Busca de rotas utilizando BFS e DFS
- Tratamento de estações bloqueadas
- Identificação automática de integrações entre linhas
- Regras de lógica proposicional e lógica de primeira ordem
- Encadeamento para frente para aplicação das regras R1–R7
- Tratamento de acessibilidade e elevadores em manutenção
- Simulação de paralisação de linhas
- Interpretação de pedidos em linguagem natural
- Geração de respostas sobre as rotas encontradas
- Interface interativa utilizando ipywidgets
- Visualização das três linhas e do caminho encontrado
- Testes automatizados dos principais cenários

## Como executar

1. Abra o arquivo `MetroBot2_0.ipynb` no Google Colab.
2. Execute todas as células do notebook na ordem apresentada.
3. Aguarde a instalação das dependências e a criação da interface.
4. Utilize a interface exibida ao final do notebook para realizar as consultas de rota.

O projeto também possui um modo offline, permitindo sua execução sem acesso a uma API de modelo de linguagem.

Para utilizar o Groq, configure `PROVEDOR = "groq"` e adicione a chave `GROQ_API_KEY` nos Secrets do Google Colab. A chave da API não deve ser inserida diretamente no código.

## Testes

O notebook possui testes automatizados para verificar o funcionamento das buscas, bloqueios, baldeações e regras lógicas.

Ao executar corretamente, a seção de testes deve finalizar com:

`Todos os testes passaram!`

### Explicação dos testes 5 e 6

**Teste 5 — Vila Madalena → Jabaquara com Paraíso fechada**

Ao fechar a estação Paraíso, a Linha 2-Verde fica interrompida entre Brigadeiro e Ana Rosa. Como a viagem começa em Vila Madalena, o passageiro não consegue alcançar Ana Rosa para realizar a integração com a Linha 1-Azul. Por isso, não existe rota até Jabaquara.

**Teste 6 — Vila Prudente → Jabaquara com Paraíso fechada**

Nesse caso, a viagem começa em Vila Prudente, do outro lado da interrupção. Mesmo com Paraíso fechada, é possível chegar até Ana Rosa pela Linha 2-Verde. Em Ana Rosa, o passageiro realiza a integração com a Linha 1-Azul e segue até Jabaquara. Por isso, existe uma rota com 13 paradas.

## Tecnologias utilizadas

- Python
- Google Colab
- BFS e DFS
- Lógica proposicional
- Lógica de primeira ordem
- Groq API
- ipywidgets
- Matplotlib

## Autor

Pedro Paulo Camargo da Silva
