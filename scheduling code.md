```
import java.util.Random;

public class scheduling {
    public static void main(String[] args){
        int n = 4;  //작업의 개수
        int m = 2;  //기계의 개수
        Random random = new Random();
        int[] time = new int[n];
        for(int i=0; i<time.length; i++){
            time[i] = random.nextInt(10)+1;
        }

        System.out.println("작업에 걸리는 시간");
        for(int i=0; i<time.length; i++){
            System.out.println(time[i]);
        }

        int[] L = new int[m];	//0번 인덱스 = m1, 1번 인덱스 = m2
        int result = 0;
        int min = 0;

        for(int i=0; i<L.length; i++)
            L[i]=0;

        for(int i=0; i<time.length; i++){
            for(int j=0; j<L.length; j++){
                if(L[j] < L[min])
                    min = j;
            }
            L[min] += time[i];
        }

        for(int i=0; i<L.length; i++){
            if(result < L[i])
                result = L[i];
        }
        System.out.println("결과는 " + result);
    }
}
```

