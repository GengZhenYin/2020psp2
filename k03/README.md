# 課題3 レポート

aa83988848 薗田光太郎

## 課題

住んでるA県で生まれたジモティー20歳の男性の平均と分散が分かっているので，典型的なA県生まれの20歳男性の身長を新たに捏造することが可能である．5人分捏造してみよ．int rand(void)は0〜RAND_MAXの疑似乱数（整数）を1つ生成する関数である．この関数は整数しか出力されないので，0から1の間の一様乱数を生成するために，関数 double r_unif(void)を作成した．また，詳細は省くがこの一様乱数生成関数 r_unifを用いて，正規乱数生成関数 double r_stdnorm(void)を作成した(box-muller法)．
  
  ```{c}
  #include <stdlib.h>
  #include <math.h>

  double r_unif(void)
  {
    return (double)(rand()+1)/(RAND_MAX+2);
  }
  
  double r_norm(void)
  {  
    return sqrt( -2.0*log(r_unif()) ) * sin( 2.0*M_PI*r_unif() );
  } 
  ```

## ソースコードの説明

## 修正履歴

