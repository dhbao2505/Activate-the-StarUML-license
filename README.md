
# StarUML
Download: [StarUML](https://staruml.io/)

# Activate License StarUML
1. Mở **Command Prompt (Run as administrator)**, gõ lệnh: ```cd C:\Program Files\StarUML\resources```
2. Cài đặt công cụ asar: ```npm install -g asar```
3. Giải nén StarUML: ```asar extract app.asar app```
4. Mở **Visual Studio Code** vào đường dẫn ```C:\Program Files\StarUML\resources\app\src\engine\```, chỉnh sửa tệp ```license-manager.js``` ở dòng 131 (**Ctrl + S -> Retry as Administrator**):
```py
checkLicenseValidity () {
    this.validate().then(() => {
      setStatus(this, true)
    }, () => {
    //===> Cambiar false por true
      setStatus(this, true)
      //===> Comentar Dialog
      // UnregisteredDialog.showDialog()
    })
  }
```
5. Đóng gói lại StarUML: ``` asar pack app app.asar```
6. Mở **StarUML**, vào **Help -> Enter License Key** xuất hiện thông báo ```"You already have a valid license."```. Kích hoạt thành công!

#### Nguồn: [StarUml 3.](https://gist.github.com/jjvillavicencio/4e3615a8219bb1a17c81c4541c6c317d)
