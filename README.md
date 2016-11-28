## Bootstrap Waitingfor Dialog
�ק�F�@�Өϥ�Bootstrap����dialog.? (�쥻GitHub : https://github.com/ehpc/bootstrap-waitingfor )
�o��dialog�i�H�ΨӰ�message box��waitingfor box
## Install
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap-theme.css">
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>
<script src="https://code.jquery.com/jquery-31.1.1.js "></script>
<script src="bootstrap-waitingfor.js"></script>
## How to use
1. �}�Ҥ@��waitfor dialog
	progressType�]��false�N������progress bar, image�h�O�o��dialog�ҭn��ܪ��Ϥ�.

	function waitDialog() {
		var setting = {
			progressType: false,
			image: "http://blog.teamtreehouse.com/wp-content/uploads/2015/05/InternetSlowdown_Day.gif",
		};
	waitingDialog.show("wait a minute", setting);
	}

2. ����dialog
	waitingDialog.hide();

3. �i�b�}��dialog���ᰵ�H�U�o�ǭק�

	���r��
	waitingDialog.message("success");

	���Ϥ�
	waitingDialog.image("http://www.freeiconspng.com/uploads/success-icon-28.png");

	�ҥΡ�cancel�� button, user�i�H����cancel��������dialog.
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

