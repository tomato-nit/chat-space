
## users テーブル
|Column|Type|Options|
|------|----|-------|
|nickname|string|null: false|
|email|string|null: false|
|password|string|null: false|

### Association
- has_many :groups
- has_many :chats




## chats テーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group id|integer|null: false, foreign_key: true|
|chat|text|null: false|
|image|text| |

### Association
- belongs_to :user





## group テーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|groupname|integer|null: false|

### Association
- has_many :users
- has_many :chats





## users_groups テーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user