# itsa-no.8
#include <iostream>

using namespace std;

 bool isPrime(int n) //定義一個isPrime函數來判斷一個整數是否為質數

{ 

    if (n <= 1) return false;  // 若輸入的質為1或等於1則直接輸出"不是質數"

    for (int i = 2; i * i <= n; i++) {
        if (n % i == 0) {   //判斷是否有能整除n的數，若有，則輸出"不是質數"，反之亦然
            return false;
        }
    }
    return true;
}

int main() 
{

    int n;
    cout << "請輸入一個整數：";
    cin >> n;
    if (isPrime(n)) {
    
        cout << n << " 是質數\n";
        
    } else 
    {
        cout << n << " 不是質數\n";
    }
    return 0;
}
