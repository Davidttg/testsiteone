---
title: "The Code"
date: 2018-12-15T15:55:34+13:00
draft: false
categories: [Coding, Api]
tags: [floor, csharp]
---

## Init the code

We start with `public void` we don't wish to alarm people

```csharp
var fileDialog = new System.Windows.Forms.OpenFileDialog();
	fileDialog.Filter = "Image files (*.jpg)|*.jpg|All files (*.*)|*.*";
	var result = fileDialog.ShowDialog();
	switch (result)
	{
		case System.Windows.Forms.DialogResult.OK:
			var file = fileDialog.FileName;
			TxtImgFile.Text = file;
			TxtImgFile.ToolTip = file;
			break;
		case System.Windows.Forms.DialogResult.Cancel:
		default:
			TxtImgFile.Text = null;
			TxtImgFile.ToolTip = null;
			break;
	}
```

### Testing the code

```javascript
function uuid() {
	function randomDigit() {
		if (crypto && crypto.getRandomValues) {
			var rands = new Uint8Array(1);
			crypto.getRandomValues(rands);
			return (rands[0] % 16).toString(16);
		} else {
			return ((Math.random() * 16) | 0).toString(16);
		}
	}
	var crypto = window.crypto || window.msCrypto;
	return 'xxxxxxxx-xxxx-4xxx-8xxx-xxxxxxxxxxxx'.replace(/x/g, randomDigit);
}
```

We need to include some other stuff but you get the idea
