# O custo oculto do parcelamento "sem juros"

> Uma análise baseada em dados reais para responder uma pergunta simples:
>
> **Quem realmente paga pelo parcelamento sem juros?**

## Sobre o projeto

No Brasil, é comum encontrar anúncios como:

> **"12x sem juros."**

À primeira vista, parece que financiar uma compra durante um ano não possui custo.

Mas isso levanta uma questão econômica importante:

**Se existe um custo para antecipar o dinheiro da venda e o dinheiro tem valor no tempo, quem está pagando essa conta?**

Este projeto utiliza dados reais de 2025 para responder essa pergunta através de simulações financeiras simples e reproduzíveis.

---

## Objetivos

Este estudo busca mostrar:

* como funciona o custo do parcelamento para o lojista;
* por que esse custo frequentemente aparece embutido no preço do produto;
* o impacto da inflação e da taxa de juros sobre compras parceladas;
* quando vale mais a pena pagar à vista;
* quando vale mais a pena parcelar e manter o dinheiro investido.

O objetivo é educativo. Não há recomendação de investimento nem defesa de um método específico de pagamento.

---

## Dados utilizados

O notebook utiliza informações públicas de 2025:

* IPCA mensal (IBGE)
* CDI / Selic Over (Banco Central)
* Faixas médias de MDR (Merchant Discount Rate) praticadas por adquirentes brasileiras

Todos os valores podem ser facilmente atualizados para anos futuros.

---

## O que é analisado

O notebook está dividido em cinco partes.

### 1. Custo do parcelamento

Simulação do custo que um lojista suporta para oferecer vendas parceladas.

São apresentados cenários de:

* 2 parcelas
* 3 parcelas
* 4 parcelas
* 6 parcelas
* 8 parcelas
* 10 parcelas
* 12 parcelas

---

### 2. Valor do dinheiro no tempo

Utilizando o IPCA de 2025, calcula-se quanto uma parcela recebida meses depois perde em poder de compra.

Também é mostrado o custo de oportunidade utilizando o CDI acumulado.

---

### 3. Formação do preço

Demonstra como um lojista precisa reajustar o preço anunciado para receber determinado valor líquido após pagar os custos do parcelamento.

O estudo também mostra quanto poderia ser concedido como desconto para pagamento à vista.

---

### 4. Parcelar ou pagar à vista?

São apresentados dois modelos distintos.

### Modelo A

Ambos os consumidores começam com exatamente o mesmo patrimônio.

Compara qual deles termina o período com maior riqueza.

### Modelo B

Modelo clássico de finanças pessoais.

Responde à pergunta:

> Vale a pena abrir mão do desconto para manter o dinheiro investido?

O notebook calcula automaticamente o **break-even**, isto é, o desconto mínimo necessário para que pagar à vista seja financeiramente mais vantajoso.

---

### 5. Evolução mês a mês

Apresenta toda a evolução do investimento durante o período do parcelamento.

São exibidos:

* saldo inicial;
* rendimento mensal;
* saque correspondente à parcela;
* saldo final.

---

## Principais conclusões

O estudo mostra que:

* parcelamento "sem juros" não significa ausência de custos;
* o custo do parcelamento normalmente é suportado pelo lojista e frequentemente incorporado ao preço do produto;
* consumidores que pagam à vista sem negociar desconto podem acabar pagando parte desse custo;
* a decisão entre pagar à vista ou parcelar depende da taxa de juros disponível e do desconto oferecido;
* existe um ponto de equilíbrio ("break-even") que pode ser calculado matematicamente.

---

## Estrutura do projeto

```text
.
├── parcelado_sem_juros_2025 - 1.ipynb
├── imagens/
└── README.md
```

---

## Tecnologias

* Python
* NumPy
* Pandas
* Matplotlib
* Jupyter Notebook

---

## Como executar

Clone o repositório:

```bash
git clone https://github.com/ErikCassiocs/12-sem-juros.git
```

Instale as dependências:

```bash
pip install -r requirements.txt
```

Abra o notebook:

```bash
jupyter notebook
```

Execute todas as células para reproduzir os resultados.

---

## Aviso

Este projeto possui finalidade exclusivamente educacional.

As simulações utilizam hipóteses simplificadas e valores médios de mercado. Custos efetivos de adquirência, descontos comerciais, políticas de preço e condições de financiamento podem variar entre empresas, instituições financeiras e períodos analisados.

---

## Licença

Este projeto está disponível sob a licença MIT.
