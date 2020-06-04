
## users テーブル
|Column|Type|Options|
|------|----|-------|
|nickname|string|null: false|
|email|string|null: false|
|password|string|null: false|

### Association
- has_many :users_groups
- has_many  :groups,  through:  :users_groups
- has_many :chats




## chats テーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group id|integer|null: false, foreign_key: true|
|chat|text||
|image|text| |

### Association
- belongs_to :user
- belongs_to :group




## group テーブル
|Column|Type|Options|
|------|----|-------|
|name|integer|null: false|

### Association
- has_many :users_groups
- has_many :users,  through:  :users_groups
- has_many :chats





## users_groups テーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user