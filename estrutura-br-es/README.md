# Estrutura BR–ES

Ferramenta de apoio ao desenho societário Brasil ⇄ Espanha: hierarquia, custo de manutenção,
simulação de carga tributária por faturamento e planeamento da transferência patrimonial.

Arquivo único (`index.html`), sem dependências, sem build. Salva no navegador.

---

## Árvore

```
Rafa & Bianca ──────────── residentes fiscais Espanha
      │
      └── HoldCo SL ─────── holding de participações (NÃO patrimonial)
            ├── DistriCo SL ..... distribuidora de alimentos e cafeteria
            ├── EventsCo SL ..... eventos
            ├── TechCo SL ....... sistema de IA, licenciamento a terceiros
            └── ConsultCo Ltda .. Brasil, lucro presumido

Holding dos pais (BR) ──╌╌╌► doação às PESSOAS FÍSICAS ──► aporte à HoldCo
```

**A patrimonialista ficou fora de propósito.** Só se paga com carteira de aluguel real, e
contamina a holding inteira se o ativo não afeto passar de 50% (art. 5.2 LIS).

---

## Relações e pontos de vazamento

| Fluxo | Carga | Base |
|---|---|---|
| ConsultCo → HoldCo | **10%** IRRF | Lei 15.270/2025, sem faixa de isenção para o exterior |
| Dividendo recebido na HoldCo | **1,25%** | exención 95%, art. 21 LIS |
| DistriCo / EventsCo → HoldCo | **1,25%** | idem |
| TechCo, licença a terceiros | **10%** ou 25% | Patent Box, art. 23 LIS, se houver nexus |
| HoldCo → pessoas físicas | 19–30% | IRPF del ahorro, só quando sacam |
| Pais → pessoas físicas | 5/7/9% + ITCMD | Llei 19/2010 com escritura pública, crédito art. 23 Ley 29/1987 |

---

## Três coisas que o desenho societário não resolve

1. **Direção efetiva da ConsultCo** (art. 8.1 LIS). Se estiver em Barcelona, a Espanha pode
   tratar a empresa como residente espanhola — a empresa inteira a 25%. Exige administrador
   brasileiro com poderes e remuneração reais, contratos assinados no Brasil, atas locais.
2. **Nexus do Patent Box.** O intangível precisa ser desenvolvido *dentro* da SL. IP criado
   pessoalmente e transferido depois é operação vinculada com ganho tributável.
3. **Impuesto sobre el Patrimonio** incide sobre patrimônio mundial. Deixar ativo no Brasil não
   o tira da base. A blindagem é a isenção de empresa familiar (art. 4.8 Ley 19/1991), que exige
   mais de 50% da renda total vinda da atividade — é onde a maioria falha o teste.

---

## Por que não há royalty da TechCo para a ConsultCo

No lucro presumido a base é a receita bruta presumida: despesa nenhuma reduz. O royalty custaria
15% de IRRF + 10% de CIDE + 9,25% de PIS/COFINS-Importação + ISS-importação — 25 a 30% da
remessa — sem abater nada. O dividendo custa 10%. Migrar para lucro real para obter a dedução
destrói mais do que economiza numa margem de 90%.

---

## Ordem de execução

A sequência importa mais que o desenho:

1. Saída fiscal da Bianca — **antes** da transferência de quotas
2. Retificações de DAA com denúncia espontânea (art. 138 CTN)
3. Constituir HoldCo / DistriCo / TechCo
4. Transferir quotas **colado à virada do exercício** — PJ ou sócio no exterior exclui do Simples
   já no mês seguinte ao evento
5. DAA 2026 (residente, renda mundial, crédito do tratado)
6. Saída definitiva no embarque → CSDP até fev/2028, DSDP em 2028

---

## Premissas editáveis na ferramenta

Faturamento e folha da ConsultCo, ISS, % distribuído, câmbio, faturamento e margem da DistriCo,
receita de licenças da TechCo, custos de manutenção por entidade, e todos os parâmetros da
sucessão (valor, % qualificável, ITCMD, nº de donatários, escritura pública, redução de 95%).

---

## Aviso

Mapa de decisão, não parecer. Antes de executar, validar com boutique de tributação internacional
com prática Brasil–Espanha, com os dois lados conversando.

Legislação de referência: Lei 15.270/2025 · Lei 14.596/2023 · LC 214/2025 · IN SRF 208/2002 ·
LIS arts. 5, 8, 21, 23, 100 · Ley 29/1987 arts. 20.6 e 23 · Llei 19/2010 (Catalunya) ·
Ley 19/1991 art. 4.8
