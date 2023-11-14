
# usersテーブル
| Column             | Type   | Options                  |
| ------------------ | ------ | ------------------------ |
| email              | string | null: fales, unique: true|
| encrypted_password | string | null: fales              |
| name               | string | null: fales              |
| profile            | text   | null: fales              |
| occupation         | text   | null: fales              |
| position           | text   | null: fales              |

## Association

- has_many :prototypes
- has_many :comments


# prototypesテーブル
| Column             | Type     | Options                  |
| ------------------ | -------- | ------------------------ |
| title              | string   | null: fales              |
| cacth_copy         | text     | null: fales              |
| concept            | text     | null: fales              |
| user               |references| null: fales              |

## Association
- belongs_to :user
- has_many :comments


# commentsテーブル
| Column             | Type     | Options                        |
| ------------------ | -------- | ------------------------------ |
| content            | text     | null: fales                    |
| prototype          |references| null: fales                    |
| user               |references| null: fales, foreign_ker: true |

## Association
- belongs_to :user
- belongs_to :prototeype