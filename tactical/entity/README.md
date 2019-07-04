# Entity 實體

## 定義

擁有唯一 identity 的物件。他們的身份不是由屬性定義，而是由其認證標誌決定。屬性可能會隨時間改變，但只要 id 相同就還是同一個物件。

當物件的 use case 描述出現「改變」這個關鍵字時，就很有可能是一個 Entity。

![img](https://i.imgur.com/RysfRZk.png)
(image from [Patterns, Principles, Practices of Domain Driven Design]())

EX: 小美今年十歲且 130 公分高，過了 10 年後小美二十歲且 160 公分高。雖然很多狀態改變了，但還是同一個人。

EX: 體育場座位。如果是買對號座的票，那每張票都要有對應的座位號碼，因此座位就是 Entity；如果採入場券形式，座位的編號就沒有太大意義，軟體並不在乎，因此座位就不是 Entity 。

由此可見， Entity 的 id 非常重要，一個 entity 的 id 在產生後基本上不會再改變。，而在 IDDD 中 Vernon 推薦使用

## Identity 產生機制

* User Input
* 程式決定
* DB 自動生成
* 外部系統

Entity 可以是：string, uuid, int, value object (composite fields)

## 實作方式


