import requests
import time
import csv

ceps = [

    "85865-160", "89229-101", "88070-760",
    "88301-040", "83045-090", "17700-000"

]

def buscar_cep(cep):
    try:
        url = f"https://viacep.com.br/ws/{cep}/json/"
        response = requests.get(url)
        response.raise_for_status()
        dados = response.json()
        if "erro" in dados:
            return {"cep": cep, "logradouro": "Não encontrado", "tipo_logradouro": "N/A"}
        logradouro = dados.get("logradouro", "Não especificado")
        tipo_logradouro = logradouro.split(" ")[0] if " " in logradouro else "N/A"
        return {
            "cep": cep,
            "logradouro": logradouro,
            "tipo_logradouro": tipo_logradouro
        }
    except Exception as e:
        return {"cep": cep, "logradouro": "Erro na consulta", "tipo_logradouro": str(e)}

resultados = []
for cep in ceps:
    resultados.append(buscar_cep(cep))
    time.sleep(0.5)

print(f"{'CEP':<10} {'Logradouro':<30} {'Tipo de Logradouro':<20}")
for r in resultados:
    print(f"{r['cep']:<10} {r['logradouro']:<30} {r['tipo_logradouro']:<20}")

with open("ceps_logradouros.csv", "w", newline="", encoding="utf-8") as csvfile:
    fieldnames = ["cep", "logradouro", "tipo_logradouro"]
    writer = csv.DictWriter(csvfile, fieldnames=fieldnames)
    writer.writeheader()
    writer.writerows(resultados)
