# Autenticador de Boletos

## Descricao
Servico de autenticacao e validacao de boletos bancarios com:
- Validacao de codigo de barras (Mod 11)
- Interface responsiva com validacoes em tempo real
- Namespace separado por modulos
- Regras de negocio bem estruturadas

## Arquitetura

### Estrutura de Diretorios
```
autenticador-boletos/
├── src/
│   ├── models/
│   │   └── Boleto.cs
│   ├── services/
│   │   └── ValidadorBoletos.cs
│   ├── ui/
│   │   └── BoletoUI.cs
│   └── Program.cs
├── README.md
└── autenticador-boletos.csproj
```

## Modulos Principais

### 1. Modelo de Dados (Boleto.cs)
```csharp
public class Boleto
{
    public string CodigoBarras { get; set; }
    public decimal Valor { get; set; }
    public DateTime DataVencimento { get; set; }
    public string Beneficiario { get; set; }
    public bool EstaValido { get; set; }
}
```

### 2. Servico de Validacao
- Validacao Mod 11 para codigo de barras
- Verificacao de digito verificador
- Regras de negocio bancarias

### 3. Camada de UI
- Menu interativo
- Validacoes em tempo real
- Mensagens de feedback ao usuario

## Funcionalidades

✅ Validar codigo de barras
✅ Calcular digito verificador (Mod 11)
✅ Consultar informacoes do boleto
✅ Interface amigavel com validacoes
✅ Tratamento de erros robusto

## Como Usar

1. Clone o repositorio
2. Abra no Visual Studio ou VS Code
3. Execute: `dotnet run`
4. Siga as instrucoes na interface

## Conceitos Aplicados

- **Namespace**: Organizacao de codigo em modulos
- **Encode**: Traducao de informacoes para formato legivel
- **UI Responsiva**: Interface que se adapta ao usuario
- **Validacoes**: Regras de negocio implementadas
- **Tratamento de Exceções**: Erros tratados elegantemente

## Tecnologias

- C# .NET
- Console Application
- POO (Programacao Orientada a Objetos)

## Projeto DIO
Desenvolvido como parte do desafio "Criando um Servico Autenticador de Boletos" na plataforma Digital Innovation One (DIO).
