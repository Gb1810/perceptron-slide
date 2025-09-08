
# Perceptron – Atividade Prática (IA)

📌 Aluno: Guilherme Barroso dos Santos  
📌 RA: 125111401820  
📌 Curso: Engenharia de Software  
📌 Professor: Alexandre “Montanha” de Oliveira  
📌 Data de entrega: 07/09/2025  

---

Este repositório contém um exemplo simples de Perceptron em Python e as respostas às perguntas solicitadas pelo professor.  
O código está em `main.py` e o README inclui uma explicação didática sobre o modelo e sobre o processo de treinamento.

> Observação: o código fornecido como base não implementa *treinamento*; ele demonstra as funções de entrada (`perceptron_input`) e de saída (`perceptron_output`) e um `main` para execução.  
> As respostas sobre treinamento descrevem o procedimento geral de um Perceptron para fins pedagógicos.

---

## Como executar
1. Tenha o Python 3 instalado.
2. Rode:
   ```bash
   python main.py




# Perceptron – Atividade Prática (IA)

Este repositório contém um exemplo simples de Perceptron em Python e as respostas às perguntas solicitadas pelo professor. O código está em `main.py` e o README inclui uma explicação didática sobre o modelo e sobre o processo de treinamento.

> Observação: o código fornecido como base não implementa *treinamento*; ele demonstra as funções de entrada (`perceptron_input`) e de saída (`perceptron_output`) e um `main` para execução. As respostas sobre treinamento descrevem o procedimento geral de um Perceptron para fins pedagógicos.

## Como executar
1. Tenha o Python 3 instalado.
2. Rode:
   ```bash
   python main.py
   ```

---

## Perguntas respondidas

### 1) Conceito
O Perceptron é um neurônio artificial que calcula uma soma ponderada das entradas, adiciona um **viés** (*bias*) e aplica uma função de ativação do tipo degrau para gerar saídas binárias (0 ou 1). Historicamente, ele foi um dos primeiros modelos de redes neurais (final dos anos 1950), abrindo caminho para o estudo de aprendizado de máquina ao mostrar que uma máquina pode **aprender** ajustando pesos a partir de dados. Embora simples, serviu de base para arquiteturas modernas mais profundas.

### 2) Funcionamento (classificador linear) e limitações
Dizer que o Perceptron é um **classificador linear** significa que ele procura um hiperplano (uma linha no 2D, um plano no 3D, etc.) que **separa** as classes no espaço de atributos. Se os dados forem **linearmente separáveis**, o Perceptron consegue encontrar um conjunto de pesos que classifica corretamente os exemplos.
  
**Limitações principais:**
- Não resolve problemas **não linearmente separáveis** (ex.: padrão XOR) sem engenharia de atributos ou camadas extras.
- Pode ser sensível à **escala** dos atributos e à escolha da **taxa de aprendizado**.
- Modela apenas **fronteiras de decisão lineares**; relações complexas exigem modelos mais expressivos (p.ex., redes multicamadas).

### 3) Código: etapas do treinamento (conceito geral)
O arquivo `main.py` desta base não contém um laço de treinamento; ele mostra apenas funções de cálculo e um `main` para impressão de resultados. Em um *treinamento* típico de Perceptron, as etapas seriam:
1. **Inicializar** pesos e viés (geralmente pequenos valores, aleatórios ou zeros).
2. Para cada amostra (entrada `x`, rótulo `y`):
   - **Predizer**: \( \hat{y} = \text{step}(w \cdot x + b) \).
   - **Calcular o erro**: \( e = y - \hat{y} \).
   - **Atualizar** pesos e viés (regra do Perceptron):  
     \( w \leftarrow w + \eta \cdot e \cdot x \) e \( b \leftarrow b + \eta \cdot e \), onde \(\eta\) é a taxa de aprendizado.
3. **Iterar** sobre o conjunto de dados por algumas épocas até convergir (ou atingir um critério de parada).

No código base, você encontrará:
- `perceptron_input(...)`: soma ponderada + bias.
- `perceptron_output(...)`: aplica o limiar (degrau) para obter 0/1.
- `main()`: apenas demonstra a chamada das funções.

### 4) Aplicação prática (exemplo)
Um exemplo simples: **detecção de spam** com poucas características binárias (ex.: presença de certas palavras-chave). Se existir uma combinação linear dessas características que separa razoavelmente “spam” de “não spam”, o Perceptron pode funcionar bem, com baixo custo computacional e fácil implementação. Em contextos mais complexos, modelos não lineares seriam preferíveis.

---

## Estrutura do projeto
```
perceptron-slide/
├─ main.py
├─ README.md
├─ LICENSE
└─ .gitignore
```

## Licença
MIT. Veja o arquivo `LICENSE`.

---

*Gerado em 08/09/2025.*
