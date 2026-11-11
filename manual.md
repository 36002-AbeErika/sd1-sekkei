# RPG Simple Dice について
## 概要

|機能|説明|
|---|---|
|TABLETOP|ダイスを振る、一度に何個振るか、出目の結果に補正をかけることも可能|
|HISTORY|どんなダイスを振って、どんな出目が出たかの記録をみることができる|
|Dice bag(三点リーダーから)|オリジナルのダイスを作ることができる|

- 三点リーダーからは、ほかにも、複数振った時の出目のソートも可能！
## 使うための準備
  - [x] 面倒な設定は一切ナシ！ストアでインストールしてすぐに使用可能！
## おまけ

>私が個人で書いたダイスを振るプログラム
``` java
import java.util.Scanner;

public class dice{
	public static void main(String[]args){
		int sum=0;
		int i,k,m,h,sum2;
		Scanner in=new Scanner(System.in);
		System.out.println("?d入力");
		k=in.nextInt();
		System.out.println(k+"d?入力");
		m=in.nextInt();
		System.out.println(k+"d"+m+"入力");
		System.out.println("補正は？");
		h=in.nextInt();
		System.out.println("");
		for(int c=1;c<=k;c++){
			i=(int)(Math.random()*m)+1;
			System.out.println(i);
			sum=sum+i;
		}
		System.out.println("");
		sum2=sum+h;
		System.out.println("結果"+sum2+"(ダイス合計"+sum+"　補正"+h+")");
		in.close();
	}
}
```

