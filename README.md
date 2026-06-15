# 📊 Sistema de Registro de Ponto - Empresa

Um sistema simples e eficiente para registrar ponto de funcionários, calcular horas trabalhadas e gerar folha de pagamento mensal.

## 🎯 Funcionalidades

- ✅ Registro de ponto (entrada e saída)
- ✅ Cálculo automático de horas trabalhadas
- ✅ Visualização de registros diários
- ✅ Geração de folha de pagamento mensal
- ✅ Previsão de pagamento (5º dia útil do mês seguinte)
- ✅ Painel administrativo (visualizar todos os funcionários)

## 🛠️ Tecnologias Utilizadas

- **Frontend**: HTML5, CSS3, JavaScript
- **Backend**: PHP 7.4+
- **Banco de Dados**: MongoDB
- **Servidor Local**: XAMPP (Apache + MySQL/MongoDB)

## 📋 Pré-requisitos

- XAMPP instalado ([Download](https://www.apachefriends.org/))
- MongoDB instalado ([Download](https://www.mongodb.com/try/download/community))
- PHP 7.4 ou superior
- Navegador moderno (Chrome, Firefox, Safari, Edge)

## 🚀 Como Configurar

### 1. Clonar o Repositório

```bash
git clone https://github.com/davimatos2004176-ux/registro-ponto-empresa.git
cd registro-ponto-empresa
```

### 2. Configurar XAMPP

1. Coloque a pasta do projeto em `C:\xampp\htdocs\` (Windows) ou `/Applications/XAMPP/htdocs/` (Mac)
2. Inicie o Apache pelo painel de controle do XAMPP
3. Acesse: `http://localhost/registro-ponto-empresa/`

### 3. Configurar MongoDB

1. Inicie o servidor MongoDB
2. Crie um banco de dados chamado `registro_ponto`
3. Configure a conexão em `php/config.php`

### 4. Estrutura de Pastas

```
registro-ponto-empresa/
├── index.html                 # Página de login
├── dashboard.html             # Painel do funcionário
├── admin.html                 # Painel administrativo
├── css/
│   ├── style.css              # Estilos gerais
│   └── dashboard.css          # Estilos do dashboard
├── js/
│   ├── main.js                # Lógica principal
│   ├── registro.js            # Registro de ponto
│   └── calculo.js             # Cálculo de horas
├── php/
│   ├── config.php             # Conexão com MongoDB
│   ├── registrar_ponto.php    # Registra entrada/saída
│   ├── obter_registros.php    # Obtém dados do BD
│   ├── calcular_horas.php     # Calcula horas trabalhadas
│   └── gerar_folha.php        # Gera folha de pagamento
└── README.md                  # Este arquivo
```

## 📝 Como Usar

### Para Funcionários:

1. Acesse `http://localhost/registro-ponto-empresa/`
2. Faça login com suas credenciais
3. Clique em "Registrar Entrada" ao chegar
4. Clique em "Registrar Saída" ao sair
5. Visualize seu histórico de ponto

### Para Administrador:

1. Acesse o painel admin
2. Visualize todos os funcionários
3. Consulte as horas trabalhadas
4. Gere folhas de pagamento

## 💾 Estrutura do Banco de Dados

### Coleção: `funcionarios`
```json
{
  "_id": ObjectId,
  "matricula": "001",
  "nome": "João Silva",
  "email": "joao@empresa.com",
  "salario_base": 3000.00,
  "criado_em": ISODate()
}
```

### Coleção: `registros_ponto`
```json
{
  "_id": ObjectId,
  "matricula": "001",
  "data": ISODate("2026-06-15"),
  "hora_entrada": "08:00",
  "hora_saida": "17:00",
  "horas_trabalhadas": 8.5,
  "registrado_em": ISODate()
}
```

### Coleção: `folhas_pagamento`
```json
{
  "_id": ObjectId,
  "matricula": "001",
  "mes": "06/2026",
  "total_horas": 160,
  "salario_bruto": 3000.00,
  "descontos": 0,
  "salario_liquido": 3000.00,
  "data_pagamento": ISODate("2026-07-07"),
  "gerado_em": ISODate()
}
```

## 📞 Suporte

Dúvidas? Abra uma [issue](https://github.com/davimatos2004176-ux/registro-ponto-empresa/issues) no repositório.

## 📄 Licença

Este projeto é de código aberto e está disponível sob a licença MIT.

---

**Desenvolvido com ❤️ para simplificar o registro de ponto**
