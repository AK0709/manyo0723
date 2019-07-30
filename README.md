# 万葉ワーク仕様
### テーブル設計について
テーブルはusers, tasks, labels, connect_tasks_labels　の4種類がある。
詳細については下記の通り。
|users|
|---|
|id|
|name:string<br>e_mail:text<br>password:string|

---

|tasks|
|---|
|id<br>user_id(FK)<br>connect_tasks_labels(FK)|
|title:string<br>content:text<br>dead_line:date<br>priority:integer<br>status:string<br>create_date:date|

---

|labels|
|---|
|id<br>users_id(FK)<br>connect_tasks_labels(FK)|
|contents:text|

---

|connect_tasks_labels|
|---|
|id<br>tasks_id(FK)<br>labels_id(FK)|

