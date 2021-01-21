# テーブル設計

## users テーブル

| Column   | Type   | Options     |
| -------- | ------ | ----------- |
| nickname | string | null: false |
| password | string |             |





### Association
- has_many :article
- has_many :comments
- 
  

## article テーブル

| Column     | Type   | Options     |
| ------     | ------ | ----------- |
| title      | string | null: false |
| text       | text   | null: false |
| user       | reference            |

* user    foreign_key



### Association

- belong_to:user
- has_many :comments

   

## comments テーブル

| Column   | Type       | Options                        |
| -------  | ---------- | ------------------------------ |
| content  | text       |  null: false                   |
| article  | references |                                |
| user     | references |                                |

* article foreign_key
* user    foreign_key


### Association

- belongs_to :article
- belongs_to :user