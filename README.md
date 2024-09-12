## ADS-POO - Media do consumo de água em 30 dias!
```
class Programa {

    public static void Main() {
        int i;
        int media = 0;
        int aguaTotal = 0;
        int consumoMinimo = int.MaxValue;
        int consumoMaximo = int.MinValue;
        int diaMinimo = 0;
        int diaMaximo = 0;

        for (i = 0; i < 2; i++) {

            Console.Write($"Digite o consumo de água no dia {i + 1}: ");
            int agua = Convert.ToInt32(Console.ReadLine());

            if (agua < consumoMinimo) {
                consumoMinimo = agua;
                diaMinimo = i + 1;  
            }

            
            if (agua > consumoMaximo) {
                consumoMaximo = agua;
                diaMaximo = i + 1;
            }

            media = media + agua;
            aguaTotal = aguaTotal + agua;
        }

        media = media / 2;

        Console.WriteLine($"\nAgua consumida total: {aguaTotal} Litros");
        Console.WriteLine($"\nO consumo médio é: {media} Litros");
        Console.WriteLine($"\nO consumo Máximo de água foi no dia {diaMaximo}: {consumoMaximo}");
        Console.WriteLine($"\nO consumo mínimo de água foi no dia {diaMinimo}: {consumoMinimo}");

        Console.ReadLine();  // Mantém o console aberto até que o usuário pressione Enter
    }
}

##PROGRAMAÇÃO 5 CLASSES
using System.Threading.Channels;

    
class Pessoa {
    
    
    // Atributos
    public string Nome { get; set; }
    public int Idade { get; set; }
    public string Sexo { get; set; }
    public string Endereco { get; set; }
    public string Email { get; set; }

    // Métodos
    public void Apresentar() {
        Console.WriteLine($"Olá, meu nome é {Nome}, tenho {Idade} anos e sou do sexo {Sexo}.\n");
    }

    public void Envelhecer() {
        Idade++;
        Console.WriteLine($"Aniversário celebrado! Agora tenho {Idade} anos.\n");
    }

    public void MudarEndereco(string novoEndereco) {
        Endereco = novoEndereco;
        Console.WriteLine($"Endereço atualizado para: {Endereco}\n");
    }

    public void EnviarEmail(string mensagem) {
        Console.WriteLine($"Email enviado para {Email}: {mensagem}\n");
    }
}

class Carro {
    // Atributos
    public string Marca { get; set; }
    public string Modelo { get; set; }
    public int Ano { get; set; }
    public string Cor { get; set; }
    public int Velocidade { get; set; }

    // Métodos
    public void Acelerar() {
        Velocidade += 10;
        Console.WriteLine($"Acelerando! Velocidade atual: {Velocidade} km/h\n");
    }

    public void Frear() {
        Velocidade -= 10;
        Console.WriteLine($"Freando! Velocidade atual: {Velocidade} km/h\n");
    }

    public void TrocarCor(string novaCor) {
        Cor = novaCor;
        Console.WriteLine($"Cor do carro alterada para: {Cor}\n");
    }

    public void MostrarDetalhes() {
        Console.WriteLine($"Marca: {Marca}, Modelo: {Modelo}, Ano: {Ano}, Cor: {Cor}, Velocidade: {Velocidade} km/h\n");
    }
}

class Produto {
    // Atributos
    public string Nome { get; set; }
    public double Preco { get; set; }
    public int Estoque { get; set; }
    public string Categoria { get; set; }
    public string Descricao { get; set; }

    // Métodos
    public void MostrarDetalhes() {
        Console.WriteLine($"Produto: {Nome}, Preço: R${Preco}, Estoque: {Estoque}, Categoria: {Categoria}\n");
    }

    public void AlterarPreco(double novoPreco) {
        Preco = novoPreco;
        Console.WriteLine($"Preço alterado para R${Preco}\n");
    }

    public void AtualizarEstoque(int quantidade) {
        Estoque += quantidade;
        Console.WriteLine($"Estoque atualizado para: {Estoque} \n");
    }

    public void MostrarDescricao() {
        Console.WriteLine($"Descrição do produto: {Descricao} \n");
    }
}

class Animal {
    // Atributos
    public string Nome { get; set; }
    public string Tipo { get; set; }
    public int Idade { get; set; }
    public string Habitat { get; set; }
    public string Som { get; set; }

    // Métodos
    public void EmitirSom() {
        Console.WriteLine($"{Nome} faz o som: {Som}\n");
    }

    public void Dormir() {
        Console.WriteLine($"{Nome} está dormindo zZzZz\n");
    }

    public void MudarHabitat(string novoHabitat) {
        Habitat = novoHabitat;
        Console.WriteLine($"{Nome} agora vive em {Habitat}");
    }

    public void MostrarDetalhes() {
        Console.WriteLine($"Nome: {Nome}, Tipo: {Tipo}, Idade: {Idade}, Habitat: {Habitat}\n");
    }
}

class Program {

    static void Main(string[] args) {
        // Exemplo de uso das classes
        Pessoa pessoa1 = new Pessoa();
        pessoa1.Nome = "João";
        pessoa1.Idade = 30;
        pessoa1.Sexo = "Masculino";
        pessoa1.Endereco = "Rua A, 123";
        pessoa1.Email = "joao@example.com";

        pessoa1.Apresentar();
        pessoa1.Envelhecer();
        pessoa1.MudarEndereco("Rua B, 456");
        pessoa1.EnviarEmail("Olá, João! Como vai?");

        Carro carro1 = new Carro();
        carro1.Marca = "Toyota";
        carro1.Modelo = "Corolla";
        carro1.Ano = 2022;
        carro1.Cor = "Prata";
        carro1.Velocidade = 0;

        carro1.Acelerar();
        carro1.Frear();
        carro1.TrocarCor("Vermelho");
        carro1.MostrarDetalhes();

        Produto produto1 = new Produto();
        produto1.Nome = "Notebook";
        produto1.Preco = 3500.00;
        produto1.Estoque = 50;
        produto1.Categoria = "Eletrônicos";
        produto1.Descricao = "Notebook com processador Intel Core i5 e 8GB de RAM.";

        produto1.MostrarDetalhes();
        produto1.AlterarPreco(3200.00);
        produto1.AtualizarEstoque(-10);
        produto1.MostrarDescricao();

        Animal animal1 = new Animal();
        animal1.Nome = "Leão";
        animal1.Tipo = "Mamífero";
        animal1.Idade = 5;
        animal1.Habitat = "Savana";
        animal1.Som = "Rugido";

        animal1.EmitirSom();
        animal1.Dormir();
        animal1.MudarHabitat("Floresta");
        animal1.MostrarDetalhes();
    }
}


