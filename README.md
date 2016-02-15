# high-equal-response-layout
等高響應式佈局

1. 使用 % 計算寬度，支援 RWD，手機翻轉時不至於破版
2. 最後一行不填滿
3. 使用 new HerlNode(節點) 建立一個 HerlNode 物件，方法存在 HerlNode.prototype.herl (herl.js)
4. HerlNode 物件方法 herl，可傳入一個物件設定值 (目前只能設定高度)
5. 必須使用 window.onload，等圖片加載完成
6. no jQuery

範例：

    window.onload = function(){
			var box = new HerlNode(document.querySelector('.box')); //建立一個 HerlNode 物件
			box.herl({'height': 180}); //設定高度
		}
