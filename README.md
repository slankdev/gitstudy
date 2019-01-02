
# Git Study

Branch構造は以下のようになっている

- master:
	-	完全に動くものしか置かない
	- hotfixはここに直接入れる.
	- 子ブランチ
		- develop:
			- とりあえず動いた物をおく.
			- 定期的にmasterのhotfixをmasterから取り込む.
			- 定期的にmasterにPRする
			- masterに非mergedな機能のhotfixはここに直接する.
			- 子ブランチ
				- feature-a:
					- 機能Aを作る.
					- developにPRする前にhotfixを取り込む
				- feature-b:
					- 機能Bを作る.
					- developにPRする前にhotfixを取り込む

## 理想的なコミットツリー

頑張って以下の形を保ちたい. 誰もミスらなければ達成できる.
タイミングによって不都合でもなんとか修正する.

```
branc-name  -----old---new

master      ---- M1-------------------------M1.1------M2---
                   \                            \    /
develop              D1----------------D1.1------D1.2
                       \              /
feature-a                A1---A2---A3
```

## origin/develop で origin/master の hotfix を反映させる

```
```
