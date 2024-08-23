# Aohoadientoandammay
Code_Demo

using System;

class Program
{
    
    static bool KtSoNguyenTo(int number)
    {
        if (number <= 1) return false;
        if (number == 2) return true; // 2 là số nguyên tố

        // Kiểm tra từ 2 đến căn bậc hai của số
        for (int i = 2; i * i <= number; i++)
        {
            if (number % i == 0) return false;
        }

        return true;
    }

    // Hàm chính
    static void Main(string[] args)
    {
        // Tạo số ngẫu nhiên
        Random random = new Random();
        int randomNumber = random.Next(1, 100); // Số ngẫu nhiên từ 1 đến 99
        Console.WriteLine($"Số ngẫu nhiên được tạo ra: {randomNumber}");

        // Kiểm tra xem số ngẫu nhiên có phải là số nguyên tố không
        if (KtSoNguyenTo(randomNumber))
        {
            Console.WriteLine($"{randomNumber} là số nguyên tố.");
        }
        else
        {
            Console.WriteLine($"{randomNumber} không phải là số nguyên tố.");
        }
    }
}

