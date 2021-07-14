# sample-ajax
受賞中のリソースの置き場

ajaxのgetを行うための天ぷら
## jQuery 側の　json オブジェクトの準備
```javascript
formData={};
```
{}は空のjsonオブジェクト
```javascript
formData["param1"] = "テスト";
```
formDataのプロパティは　formData("プロパティ文字列")　に値をセットして作成される
formDataのプロパティは　formData.プロパティ文字列　と書くこともできます
```javascript
formData.param1 = "テスト";
```
##jQuery側からサーバへデータを送る
```javascript
data: formData
```
```javascript
{
  "param1":"テスト"
}
```
http://localhost/app/form-action-json.php?param1=%E3%83%86%E3%82%B9%E3%83%88&_=162624087476
と言うフォーマットにjQueryに加工されてサーバのphpが呼び出される
## phpでデータを受け取る
QueryStiring と呼ばれる?以降の文字列が$_GETにセットされてtphpに入る
```
param1=%E3%83%86%E3%82%B9%E3%83%88&_=1626240874763
```
<b>$_GET</b>["param1"]に"テスト"がセットされてスーパーグローバル変数として利用可能となる
