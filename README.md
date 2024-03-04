## ADS-POO

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
