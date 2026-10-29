# Computação Quântica — Semana Acadêmica 2026

**Palestrante:** Yohanna Dvorak (`ydvorak@id.uff.br`)

Repositório com os slides, guias rápidos de consulta (1 página A4) e notebooks práticos em **Qiskit** das duas palestras sobre Computação Quântica:

1. **Palestra 1 (1h — Teórica):** *Computação Quântica: Um Panorama Geral*
2. **Palestra 2 (2h — Prática):** *Programação Quântica na Prática com Qiskit*

---

## Estrutura do Repositório

```text
semana_academica_2026/
├── slides/
│   ├── palestra1_panorama.pdf        # Slides da Palestra 1 (Teórica - 1h)
│   └── palestra2_pratica.pdf         # Slides da Palestra 2 (Prática - 2h)
├── guias/
│   ├── guia_palestra1.pdf            # Guia Rápido 1 (1 página A4): Fundamentos e Portas
│   └── guia_palestra2.pdf            # Guia Rápido 2 (1 página A4): Qiskit e Algoritmos
├── pratica/
│   ├── pratica_qiskit_aluno.ipynb    # Notebook com os exercícios (# TODO:) para os alunos
│   └── pratica_qiskit_completo.ipynb # Notebook gabarito completo + Demonstração Extra (Cuccaro n=3)
├── requirements.txt                  # Dependências Python para execução local
└── README.md
```

---

## Conteúdo das Palestras

### Palestra 1: Computação Quântica — Um Panorama Geral (1h)
* Do bit clássico ao **Qubit** ($\ket{\psi} = \alpha\ket{0} + \beta\ket{1}$) e **Esfera de Bloch**.
* Os 3 Pilares: **Superposição**, **Interferência** e **Emaranhamento**.
* **Medição** e Regra de Born ($P(0) = |\alpha|^2$, $P(1) = |\beta|^2$).
* **Portas Lógicas Quânticas:** Matrizes unitárias ($U^\dagger U = I$), transposto conjugado ($\dagger$) e ação explícita de $I, H, X, Z, Y, S, T, U$, **CNOT ($CX$)** e **Toffoli ($CCX$)** nos estados $\ket{0}, \ket{1}, \ket{+}, \ket{-}$.
* Aplicações reais, impacto na criptografia (Shor e Grover), era **NISQ** e correção de erros.

### Palestra 2: Programação Quântica na Prática (2h)
* Revisão das portas no **Qiskit**, convenção *Little-Endian* ($\ket{q_{n-1}\dots q_0}$) e como inverter portas/circuitos (`.inverse()`).
* **Exercício 0:** Aquecimento — Criando e medindo o Par de Bell ($\ket{\Phi^+}$).
* **Exercício 1: Codificação Superdensa (*Superdense Coding*)** — Enviando 2 bits clássicos usando apenas 1 qubit emaranhado.
* **Exercício 2: Teletransporte Quântico** — Transferindo um estado quântico $\ket{\psi}$ de Alice para Bob.
* **Exercício 3: Algoritmo de Busca de Grover ($n = 2$ qubits)** — Oráculo de Fase e Difusor de Grover para amplificar o estado $\ket{11}$ com 1 única consulta.
* **Exercício 4: Grover com Somador de Cuccaro ($n = 2$ bits)** — Usando a porta `CDKMRippleCarryAdder` do Qiskit dentro do oráculo (Soma $\to$ Marca $X$ $\to$ Descomputa com `.inverse()`) para descobrir qual número $A$ satisfaz $A + Y = X$.
* **Extra (Demonstração no Gabarito):** Grover com Somador de Cuccaro para $n = 3$ bits (7 qubits).

---

## Como Executar os Notebooks da Prática

### Opção 1: No VS Code (Execução Local)
1. Clone este repositório e abra a pasta no **VS Code**:
   ```bash
   git clone https://github.com/Dvoraky/semana_academica_2026.git
   cd semana_academica_2026
   code .
   ```
2. Certifique-se de ter as extensões **Python** e **Jupyter** instaladas no VS Code.
3. Crie um ambiente virtual e instale os pacotes (pelo terminal do VS Code):
   ```bash
   python -m venv .venv
   source .venv/bin/activate  # No Windows: .venv\Scripts\activate
   pip install -r requirements.txt
   ```
4. Abra o arquivo `pratica/pratica_qiskit_aluno.ipynb` (ou crie o seu próprio arquivo `.ipynb` no VS Code), selecione o kernel `.venv` no canto superior direito e execute as células!

### Opção 2: No Google Colab (Sem instalar nada)
1. Acesse [colab.research.google.com](https://colab.research.google.com/).
2. Clique na aba **GitHub**, cole a URL deste repositório (`https://github.com/Dvoraky/semana_academica_2026`) e abra `pratica/pratica_qiskit_aluno.ipynb`.
3. Execute a primeira célula do notebook (ela instala automaticamente `qiskit`, `qiskit-aer` e `pylatexenc`).

---

## Referências para Continuar Estudando

* **Livro Clássico:** M. A. Nielsen & I. L. Chuang, *Quantum Computation and Quantum Information* (Cambridge University Press).
* **Cursos e Tutoriais Interativos (Qiskit):** [IBM Quantum Learning](https://learning.quantum.ibm.com/)
* **Outras Referências Recomendadas:** [https://lnkd.in/p/d46rDy9P](https://lnkd.in/p/d46rDy9P)
