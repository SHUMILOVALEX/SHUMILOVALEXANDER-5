TASK 1
#include <iostream>
#include <cstdlib>
int main () {
    int razmer;
    double sred = 0;
    std::cout << "What is the size of the array?"<<"\n";
    std::cin >> razmer;
    int arr[razmer];
    for (int i = 0; i < razmer; i++){
        double c;
        arr[i] = rand()%10;
        c = arr[i];
        sred = sred + c;
        std::cout << arr[i] << ", ";
    }
    std::cout << "\n";
    std::cout << "sredniy"<<"="<<sred/razmer;
}
Task 2
#include <iostream>
#include <cstdlib>
int main () {
    int razmer;
    std::cout << "What is the size of the array?"<<"\n";
    std::cin >> razmer;
    int arr[razmer];
    int chet = 0;
    int nechet = 0;
    for (int i = 0; i < razmer; i++){
        int c;
        arr[i] = rand()%10;
        c = arr[i];
        if (c%2!=0){
            nechet++;
        }
        else{
            chet++;
        }
        std::cout<<c<<' ';
    }
    std::cout << "\n";
    std::cout << "chet"<<" = "<<chet<<"\n"<<"nechet"<<" = "<<nechet;
    
}
  Task 3
  #include <iostream>
  #include <cstdlib>
  int main(){
    int razmer;
    std::cout<<"What is the size of the array?"<<"\n";
    std::cin>> razmer;
    int list[razmer];
    int c;
    int min=10 ;
    int max=0;
    for (int i = 0; i<razmer; i++){
        list[i]=random()%10;
        c = list[i];
        std::cout<<c<<' ';
        for (int k = 0; k<razmer; k++){
            if (min>c){
                min=c;
            }
            if (c>max){
                max=c;
            }
        }
    }std::cout<<"min"<<min<<" max"<<max;
}
  Task 4
    #include <iostream>
  #include <cstdlib>
  #include <ctime>
  int main() {
    int N, M;
     std::cout<<"Enter the value of the N parameter"<<"\n";
      std::cin >> N ;
      std::cout<<"Enter the value of the M parameter"<<"\n";
      std::cin >> M ;
    srand(static_cast<unsigned>(time(nullptr))); 
    int** map = new int*[N];
    for (int i = 0; i < N; ++i) {
        map[i] = new int[M];
    }
    for (int i = 0; i < N; ++i) {
        for (int j = 0; j < M; ++j) {
            map[i][j] = rand() % 10; 
        }
    }
    for (int i = 0; i < N; ++i) {
        for (int j = 0; j < M; ++j) {
            std::cout << map[i][j] << " ";
        }
        std::cout << "\n";
      }
    }
  Task 5
  #include <iostream>
  #include <cstdlib>
  #include <ctime>
  
  int main() {
      int N, M;
      std::cout<<"Enter the value of the N parameter"<<"\n";
      std::cin >> N ;
      std::cout<<"Enter the value of the M parameter"<<"\n";
      std::cin >> M ;
      int SUM = 0;
      int C;
      srand(static_cast<unsigned>(time(nullptr))); 
      int** map = new int*[N];
      for (int i = 0; i < N; ++i) {
          map[i] = new int[M];
      }
      for (int i = 0; i < N; ++i) {
          for (int j = 0; j < M; ++j) {
              map[i][j] = rand() % 10;
              C = map[i][j];
              SUM += C;
          }
      }
      for (int i = 0; i < N; ++i) {
          for (int j = 0; j < M; ++j) {
              std::cout << map[i][j] << " ";
          }
          std::cout << "\n";
    }std::cout <<"SUM"<< " = " <<SUM;}
    }
    Task 6 
    #include <iostream>
    #include <cstdlib>
    #include <ctime>
    int main() {
    int N, M;
    std::cout<<"Enter the value of the N parameter"<<"\n";
    std::cin >> N ;
    std::cout<<"Enter the value of the M parameter"<<"\n";
    std::cin >> M ;
    int SUM = 0;
    int C = 0;
    srand(static_cast<unsigned>(time(nullptr))); 
    int** map = new int*[N];
    for (int i = 0; i < N; ++i) {
        map[i] = new int[M];
    }
    for (int i = 0; i < N; ++i) {
        for (int j = 0; j < M; ++j) {
            map[i][j] = rand() % 10;
        }
    }
    for (int i = 0; i < N; ++i) {
            SUM += map[i][i];
    }
    for (int i = 0; i < N; ++i) {
        for (int j = 0; j < M; ++j) {
            std::cout << map[i][j] << " ";
        }
        std::cout << "\n";
    }std::cout << "SUM"<<" = "<< SUM;
    }
