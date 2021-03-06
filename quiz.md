# オラクル課題

## 10/24
### 各自のユーザ

MY_EMPLOYEES表(1024.sql)

|    Name    |   Null   |     Type     |
|------------|----------|--------------|
| ID         | NOT NULL | NUMBER(4)    |
| LAST_NAME  |          | VARCHAR2(25) |
| FIRST_NAME |          | VARCHAR2(25) |
| USERID     |          | VARCHAR2(8)  |
| SALARY     |          | NUMBER(9,2)  |

サンプルデータ

| ID | LAST_NAME | FIRST_NAME |  USERID  | SALARY |
|:--:|-----------|------------|----------|-------:|
|  1 | Patel     | Ralph      | rpatel   |    895 |
|  2 | Dancs     | Betty      | bdancs   |    860 |
|  3 | Biri      | Ben        | bbiri    |   1100 |
|  4 | Newman    | Chad       | cnewman  |    750 |
|  5 | Rpeburn   | Audrey     | aropebur |   1550 |

1. MY_EMPLOYEES表の作成
1. サンプルの最初の行をMY_EMPLOYEES表に追加する  
INSERT句には列リストを指定しない
1. サンプルに2行目のをMY_EMPLOYEES表に追加  
今度はINSERT句に列リストを指定する
1. 残りの行をMY_EMPLOYEE表にロードするINSERT文を、  
動的に再利用可能なスクリプト・ファイルに記述します。  
スクリプトでは、すべての列(ID、LAST_NAME、FIRST_NAME、  
USERIDおよびSALARY)の入力をユーザーに求める必要があります。  
このスクリプトを1024.1.sqlファイルに保存
1. 残りのデータを上記のスクリプトファイルを用いて追加

## 10/19
### 「hr」ユーザ
1. 従業員の以前の職務IDと現行の職務IDを従業員IDの昇順  
で従業員IDと職務IDのリストを表示。  
この時、従業員IDと職務IDの組み合わせの重複は排除(1019.1.sql)
1. 職務IDのST_CLERKが含まれない部門の部門IDのリストを  
集合演算子を使用して表示(1019.2.sql)
1. 部門が存在しない国の国IDと国名を集合演算子を使用して  
表示(1019.3.sql)
1. 部門10、50および20に対する職務のリストをこの順に出力。  
集合演算子を使用して職務IDと部門IDを表示(1019.4.sql)
1. 現行の職務が会社に雇用された当初の職務と同じ  
(つまり職務を異動したが、現在は元の職務に戻っている)  
従業員の従業員IDと職務IDのリストを表示(1019.5.sql)


## 10/18
### 「hr」ユーザ
1. ユーザーに従業員の姓の入力を求めるプロンプトを表示し、  
入力された名前の従業員と同じ部門に所属するすべての従業員  
(入力した従業員は除く)の姓と雇用日を表示(1018.1.sql)
1. 給与が平均給与より多い従業員の従業員番号、姓および給与  
を給与の昇順で上位の5名表示(1018.2.sql)
1. 姓に“u”の文字が含まれる従業員が所属する部門に勤務する  
すべての従業員の従業員番号と姓を表示(1018.3.sql)
1. 部門の所在地IDが1700であるすべての従業員の姓、部門番号  
および職務IDを表示(1018.4.sql)
1. Kingを上司とするすべての従業員の姓と給与を表示(1018.5.sql)


## 10/17
### 「hr」ユーザ
1. LOCATIONS表とCOUNTRIES表をNATURAL JOINで結合し、  
所在地ID、番地、市、州または県、および国を表示(1017.1.sql)
1. 従業員の姓、部門番号および部門名を表示する  
従業員番号の昇順で上位の20名表示(1017.2.sql)
1. トロントで勤務しているすべての従業員の姓、職務、部門番号  
および部門名を表示(1017.3.sql)
1. 従業員の姓、従業員番号および担当マネージャの姓とマネージャ番号を表示  
列には、Employee、Emp#、ManagerおよびMgr#の別名(1017.4.sql)
1. 上記と同様な表示で、担当マネージャのいないKingを含める(1017.5.sql)
## 10/12
### 「hr」ユーザ
1. 従業員の従業員番号、職務およびDECODE関数を使用して  
以下の対応表を元に職務に基づく等級を表示(1012.1.sql)
1. CASE構文を使用して上記と同様の表示(1012.2.sql)
1. すべての従業員の給与の最高額、最低額、合計および平均を表示。  
列名はそれぞれMaximum、Minimum、Sum、Average。  
結果を最も近い整数に丸めて表示(1012.3.sql)
1. 職種ごとの給与の最低額、最高額、合計および平均を表示。  
列名はそれぞれMaximum、Minimum、Sum、Average。  
結果を最も近い整数に丸めて職種名の昇順で表示(1012.4.sql)
1. 同じ職務の従業員の数を職種名の昇順で表示(1012.5.sql)


|         職務         | 等級 |
|----------------------|:----:|
| AD_PRES              | A    |
| ST_MAN               | B    |
| IT_PROG              | C    |
| SA_REP               | D    |
| ST_CLERK             | E    |
| 上記のいずれでもない | 0     |



## 10/11
### 「hr」ユーザ
1. 2008年以降に雇用された従業員の従業員番号、姓、給与、雇用日付を  
雇用日付が新しい順に表示(1011.1.sql)
1. 歩合を受け取る従業員の姓、職務、給与および歩合を給与の降順で  
表示(1011.2.sql)
1. 従業員の姓と歩合の額を表示する。従業員が歩合を受け取らない場合は  
「No Commission」と表示。列名はCOMM(1011.3.sql)
1. 次のような形式でデータを表示  
<従業員の姓> earns <給与> montly but wants <給与の3倍>.  
列名はDream Salaries、給与の少ない順に5名表示(1011.4.sql)
1. 従業員の姓、雇用日、および6ヶ月の雇用期間後の最初の月曜日  
となる給与審査日を表示。列名はREVIEW  
「Monday, the Thirty-First of July, 2000」  
のような形式表示されるように日付の書式を設定  
従業員番号の昇順で上位の5名表示(1011.5.sql)

|                    Dream Salaries                     |
|:-------------------------------------------------------|
| Gienz earns $8,300.00 monthly but wants $24,900.00.    |
| Higgins earns $12,000.00 monthly but wants $36,000.00. |
| ・・・                                                 |

| LAST_NAME | HIRE_DATE |                   REVIEW                   |
|-----------|-----------|--------------------------------------------|
| King      | 17-JUN-87 | Monday, the Twenty-First of December, 1987 |
| Kochhar   | 21-SEP-89 | Monday, the Twenty-Sixth of March, 1990    |
| ・・・    |           |                                            |

## 10/10
### 「hr」ユーザ
1. 歩合が20%である従業員の姓、給与、歩合を表示(1010.1.sql)
1. システムの日付を表示する問い合わせ、列にDateというラベルをつける(1010.2.sql)
1. 従業員番号、姓、給与、15.5%増額された給与(整数で表示、列名はNew Salary)を  
給料の少ない順に5名表示(1010.3.sql)
1. 従業員ごとに姓を表示して、その従業員が雇用された日付から今日までの月数を  
計算(列名はMONTHS_WORKED)、月数は最も近い整数に丸め、月数の多い5名表示(1010.4.sql)
1. 従業員の姓と給与を給与の多い順に5名表示、給与は15文字長に設定し  
左側に$記号を埋め込む。列名はSALARY(1010.5.sql)

| LAST_NAME |      SALARY      |
|-----------|------------------|
| King      | $$$$$$$$$$$24000 |
| Kochhar   | $$$$$$$$$$$17000 |
| ・・・    |                  |



## 10/5
### 「hr」ユーザ
1. 給与が$12,000を超える従業員の姓名、給与の多い順に5名(1005.1.sql)  
1. 従業員番号176の姓名、部門番号(1005.2.sql)  
1. 給与が$5,000から$12,000の範囲に従業員の人数(1005.3.sql)  
1. 姓がMatosおよびTaylorである従業員の姓、職務ID、開始日(1005.4.sql)  
1. 部門20または50に所属する従業員の人数(1005.5.sql)  