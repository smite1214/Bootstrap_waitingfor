## Bootstrap Waitingfor Dialog
修改了一個使用Bootstrap做的dialog.? (原本GitHub : https://github.com/ehpc/bootstrap-waitingfor )
這個dialog可以用來做message box或waitingfor box
## Install
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap-theme.css">
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>
<script src="https://code.jquery.com/jquery-31.1.1.js "></script>
<script src="bootstrap-waitingfor.js"></script>
## How to use
1. 開啟一個waitfor dialog
	progressType設為false代表隱藏progress bar, image則是這個dialog所要顯示的圖片.

	function waitDialog() {
		var setting = {
			progressType: false,
			image: "http://blog.teamtreehouse.com/wp-content/uploads/2015/05/InternetSlowdown_Day.gif",
		};
	waitingDialog.show("wait a minute", setting);
	}

2. 關閉dialog
	waitingDialog.hide();

3. 可在開啟dialog之後做以下這些修改

	更改字串
	waitingDialog.message("success");

	更改圖片
	waitingDialog.image("http://www.freeiconspng.com/uploads/success-icon-28.png");

	啟用”cancel” button, user可以按”cancel”來關閉dialog.
	waitingDialog.cancel(true);

## Example
function waitDialog() {
	var setting = {
		progressType: false,
		image: "http://blog.teamtreehouse.com/wp-content/uploads/2015/05/InternetSlowdown_Day.gif",
	};

	waitingDialog.show("wait a minute", setting);
}

function waitSuccess() {
	waitingDialog.message("success");
	waitingDialog.image("http://www.freeiconspng.com/uploads/success-icon-28.png");
	setTimeout(function () {
		waitingDialog.hide();
		// do something
	}, 3000);
}

function waitFail(message) {
	waitingDialog.message(message);
	waitingDialog.image("https://elearningindustry.com/wp-content/uploads/2014/07/Top-10-Reasons-Why-LMS-Implementation-Fail.png");
	waitingDialog.cancel(true);
}

function failDialog(message) {
	var setting = {
		progressType: false,
		image: "https://elearningindustry.com/wp-content/uploads/2014/07/Top-10-Reasons-Why-LMS-Implementation-Fail.png",
		cancel: true
	};
	waitingDialog.show(message, setting);
}

