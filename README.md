# Treinando um Modelo para Responder Perguntas com o Dataset Amazon Titles

## 📝 Descrição do Projeto

Este projeto foi desenvolvido como parte do Tech Challenge da **Pós-Graduação em IA para Devs**. O objetivo principal é realizar o fine-tuning de um *foundation model* (neste caso, `mistralai/Mistral-7B-Instruct-v0.3`) para uma tarefa específica: gerar descrições de produtos da Amazon a partir de seus títulos.

O processo utiliza a técnica de **LoRA** (Low-Rank Adaptation) para treinar eficientemente o modelo em um ambiente com recursos limitados, como o Google Colab.

### Objetivos Conformes ao Desafio:
- Executar o fine-tuning de um *foundation model* (Mistral-7B).
- Utilizar o dataset "The Amazon Titles-1.3MM", especificamente o arquivo `trn.json`.
- Treinar o modelo para, a partir de um prompt com o título de um produto, gerar sua respectiva descrição.

## 🛠️ Tecnologias Utilizadas

- **Linguagem:** Python 3.10+
- **Ambiente:** Google Colab (com GPU A100 do plano Pro)

## ⚙️ Configuração do Ambiente
1.  **Hardware:** Este projeto requer um ambiente com GPU. Recomenda-se o uso do Google Colab com uma GPU T4, V100 ou, idealmente, A100.
2.  **Dependências:** As bibliotecas necessárias serão instaladas quando o código do Google Colab for executado.

## 🚀 Como Executar

1.  **Clone o Repositório:**
    ```bash
    git clone https://github.com/iesalobato/fine_tuning_amazon_titles.git
    ```

2.  **Abra o Notebook no Google Colab:** Faça o upload do arquivo `.ipynb` para o seu ambiente Colab e configure o ambiente de execução para usar uma GPU.

3.  **Autenticação no Hugging Face:** Para baixar o modelo `mistralai/Mistral-7B-Instruct-v0.3`, é necessário autenticar sua conta do Hugging Face. Execute a célula de login e insira seu token de acesso. Lembre-se que sua conta precisa ter acesso prévio ao modelo.

4.  **Execute as Células:** Execute as células do notebook em ordem. O fluxo principal é:
    * **Instalação de Dependências:** Instala todas as bibliotecas.
    * **Carregamento e Limpeza dos Dados:** Baixa o dataset do Google Drive, carrega uma amostra, remove duplicatas e formata os prompts.
    * **Carregamento do Modelo e Tokenizador:** Carrega o Mistral-7B com quantização em 4-bit.
    * **Fine-Tuning:** Executa o treinamento com o `SFTTrainer` e os parâmetros otimizados.
    * **Avaliação e Demonstração:** Carrega o modelo treinado e apresenta os resultados, incluindo uma interface interativa.

## ✒️ Equipe:
- Iêsa Lobato
- Rilson Soares
- Ismael Costa
- Felipe Vieira
