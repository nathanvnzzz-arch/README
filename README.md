from __future__ import print_function
# CALCULADORA DE ORÇAMENTO DE PESSOAL

# EDITÁVEL PELO USUÁRIO
salario_base = 3000 # Salário de cada funcionário
num_funcionarios = 4 # Quantidade de pessoas
despesas_fixas = 1500 # Outras despesas mensais

# ENCARGOS TRABALHISTAS (valores médios)
inss = 0.20 # 20%
fgts = 0.08 # 8%
ferias_terco = 0.1111 # 11,11%
decimo_terceiro = 0.0833 # 8,33%

# ----------------------------
# CÁLCULO POR FUNCIONÁRIO
# ----------------------------
# CORREÇÃO 1: A operação matemática foi unida em uma única linha,
# pois estava incompleta na linha de baixo, causando um erro.
salario_com_encargos = salario_base * (1 + inss + fgts + ferias_terco + decimo_terceiro)

# CÁLCULO TOTAL
custo_total_salarios = salario_com_encargos * num_funcionarios
custo_total_geral = custo_total_salarios + despesas_fixas

# ----------------------------
# RESULTADOS
# ----------------------------
print("=== ORÇAMENTO DE PESSOAL ===")
print(f"Salário base: R$ {salario_base:,.2f}")
print(f"Número de funcionários: {num_funcionarios}")
print(f"Despesas fixas: R$ {despesas_fixas:,.2f}")

print("===== ORÇAMENTO DE PESSOAL =====")
print(f"Salário base: R$ {salario_base:,.2f}".replace(",", "X").replace(".", ",").replace("X", "."))
print(f"Salário c/ encargos (por funcionário): R$ {salario_encargos:,.2f}".replace(",", "X").replace(".", ",").replace("X", "."))
print(f"Número de funcionários: {num_funcionarios}")
print(f"Custo total salários + encargos: R$ {custo_total_salarios:,.2f}".replace(",", "X").replace(".", ",").replace("X", "."))
print(f"Despesas fixas: R$ {despesas_fixas:,.2f}".replace(",", "X").replace(".", ",").replace("X", "."))
print(f"CUSTO GERAL TOTAL: R$ {custo_total_geral:,.2f}".replace(",", "X").replace(".", ",").replace("X", "."))
