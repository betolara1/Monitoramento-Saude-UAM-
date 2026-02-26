# 🏥 Sistema de Monitoramento de Saúde & DCNT

> Uma plataforma completa para gestão de saúde pública e privada, focada no acompanhamento de pacientes com Doenças Crônicas Não Transmissíveis (DCNTs).

![Banner Principal](assets/screenshots/dashboard-geral.png)

## 🎯 Objetivo e Problema

### O Problema
O acompanhamento de pacientes com doenças crônicas (DCNTs), como Hipertensão e Diabetes, muitas vezes é fragmentado. Equipes de saúde enfrentam dificuldades em manter um histórico centralizado, calcular riscos de forma rápida e garantir a adesão medicamentosa, o que pode levar a complicações evitáveis.

### O Objetivo
Prover uma ferramenta unificada que centraliza o prontuário, automatiza cálculos clínicos (como o Risco Cardiovascular) e facilita a comunicação entre diferentes níveis de atendimento (Médico, ACS, Paciente), melhorando o desfecho clínico e a gestão de recursos.

## 🏗️ Arquitetura do Sistema

```mermaid
graph TD
    A[Usuário/Browser] <-->|HTTPS| B(Web Server - Apache/PHP)
    B <--> C{Business Logic / MVC}
    C <--> D[(MySQL Database)]
    C <--> E[Service Workers / PWA]
    E -->|Notificações| A
```

O sistema utiliza uma arquitetura **MVC (Model-View-Controller)** implementada em PHP Puro para garantir leveza e controle total sobre as regras de negócio de saúde.

## 🛠️ Tecnologias Utilizadas

**Backend & Banco de Dados**
* ![PHP](https://img.shields.io/badge/PHP-7.4%2B-777BB4?style=flat&logo=php&logoColor=white) **PHP Nativo:** Arquitetura MVC robusta.
* ![MySQL](https://img.shields.io/badge/MySQL-00000F?style=flat&logo=mysql&logoColor=white) **MySQL:** Modelagem relacional complexa.

**Frontend**
* ![Bootstrap](https://img.shields.io/badge/Bootstrap-5-563D7C?style=flat&logo=bootstrap&logoColor=white) **Bootstrap 5.**
* ![jQuery](https://img.shields.io/badge/jQuery-0769AD?style=flat&logo=jquery&logoColor=white) **jQuery & AJAX.**

## 🚀 Como Executar

### Desenvolvimento Local
1. Clone este repositório.
2. Configure um servidor Apache/PHP (como XAMPP ou Laragon).
3. Importe o schema do banco de dados (disponível sob consulta).
4. Configure as credenciais no arquivo `config.php`.


## 📡 Exemplos de API (Requests/Responses)

### Cálculo de Risco Cardiovascular
**Request:** `POST /api/calcular-risco`
```json
{
  "idade": 55,
  "sexo": "masculino",
  "pa_sistolica": 140,
  "fumante": true,
  "colesterol_total": 200
}
```

**Response:**
```json
{
  "risco": "alto",
  "probabilidade": "20%",
  "recomendacao": "Encaminhamento prioritário para cardiologia."
}
```

## 📸 Galeria & Interface

| Dashboard & Métricas | Prontuário do Paciente |
|:---:|:---:|
| ![Dashboard](assets/screenshots/dashboard-geral.png) | ![Prontuário](assets/screenshots/paciente-prontuario.png) |

| Ferramentas Avançadas | Controle Farmacêutico |
|:---:|:---:|
| ![Calculadora de Risco](assets/screenshots/calculadora-risco.png) | ![Medicamentos](assets/screenshots/gestao-medicamentos.png) |

---
**Nota:** Este repositório serve como portfólio técnico. O código-fonte principal é privado para proteção de propriedade intelectual.

