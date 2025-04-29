# 🏨 Projeto de Sistema de Hospedagem em C#

Este projeto é um desafio prático proposto pela [DIO - Digital Innovation One](https://www.dio.me) no curso **Trilha .NET - Explorando a linguagem C#**. O objetivo é aplicar os conceitos aprendidos de orientação a objetos e estruturação de código em C#, desenvolvendo um sistema simples de hospedagem de hotel.

## 📚 Desafio Proposto

Você foi contratado para construir um sistema de hospedagem, que será usado para realizar reservas em um hotel. O sistema deve conter as seguintes classes:

- `Pessoa`: Representa um hóspede.
- `Suite`: Representa o tipo de suíte do hotel.
- `Reserva`: Responsável por gerenciar a reserva, incluindo os hóspedes e a suíte.

## 🎯 Regras de Negócio e Funcionalidades

- ✅ **Validação de Capacidade**: Não deve ser possível realizar uma reserva com mais hóspedes do que a capacidade da suíte. Se isso ocorrer, o sistema deve lançar uma exceção.
- ✅ **Cálculo de Valor da Diária**: O valor da diária é calculado com base na multiplicação dos dias reservados pelo valor da diária da suíte.
- ✅ **Desconto Progressivo**: Se a reserva for para 10 dias ou mais, deve ser aplicado um desconto de 10% no valor total da hospedagem.
- ✅ **Quantidade de Hóspedes**: O sistema deve retornar corretamente a quantidade total de hóspedes cadastrados na reserva.

## 🧪 Exemplo de Uso

```csharp
// Cria os hóspedes
List<Pessoa> hospedes = new List<Pessoa>
{
    new Pessoa(nome: "Hóspede 1"),
    new Pessoa(nome: "Hóspede 2")
};

// Cria a suíte
Suite suite = new Suite(tipoSuite: "Premium", capacidade: 2, valorDiaria: 30);

// Cria a reserva
Reserva reserva = new Reserva(diasReservados: 10);
reserva.CadastrarSuite(suite);
reserva.CadastrarHospedes(hospedes);

// Exibe informações
Console.WriteLine($"Hóspedes: {reserva.ObterQuantidadeHospedes()}");
Console.WriteLine($"Valor diária: {reserva.CalcularValorDiaria()}");
```

## 📦 Estrutura do Projeto

- `Pessoa.cs` – Define o modelo de hóspede.
- `Suite.cs` – Define o modelo de suíte, com tipo, capacidade e valor da diária.
- `Reserva.cs` – Lida com a lógica de negócios: cadastro de hóspedes e suítes, cálculo de valores e aplicação de regras.

## 🚀 Tecnologias Utilizadas

- C#
- .NET 6 ou superior
- Console Application

## 📌 Observações

Este projeto tem fins educacionais e foi desenvolvido como parte de um desafio da DIO para praticar os conceitos fundamentais de C# e programação orientada a objetos.
