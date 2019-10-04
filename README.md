## usersテーブル
|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
|mail|string|null: false, unique: true|
|pass|string|null: false|

### Association
- has_many:tweets
- has_many:comments

## tweetsテーブル
|Column|Type|Options|
|------|----|-------|
|body|text||
|image|string||
|user_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :user
- has_many:comments

## commentsテーブル
|Column|Type|Options|
|------|----|-------|
|body|text||
|user_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :user
- belongs_to :tweet