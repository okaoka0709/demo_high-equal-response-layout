# high-equal-response-layout
等高響應式佈局

類似 google 相簿、flickr 的相片呈現套件，支持 RWD (主要是希望手機翻轉螢幕時不要破版)，特色如下：

1. 每行內的圖片高度相同
2. 各行高度相似
3. 各行圖片切齊頭尾
4. 圖片自動分配歸屬行
5. 圖片等比例縮放

使用規則如下：

1. 建立一個類別 HerlNode，方法存在類別原型 HerlNode.prototype.herl
2. new 一個 HerlNode 物件時，需傳入一個節點
3. HerlNode 物件呼叫 herl 方法時，傳入一個設定物件 (目前只能設定高度 height)
4. 必須使用 window.onload，等圖片加載完成
5. no jQuery

範例：

    window.onload = function(){
		var box = new HerlNode(document.querySelector('.box')); //建立一個 HerlNode 物件
		box.herl({'height': 180}); //設定高度
	}
