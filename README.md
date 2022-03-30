# gas-form-to-mail

▼ トリガーを追加\
![image](https://user-images.githubusercontent.com/1501327/160777236-18538538-df4c-4e27-9f53-40220735ff8b.png)

```javascript
function formMail( e ) {

  FormApp.getActiveForm();

  var itemResponses = e.response.getItemResponses();
  var email = e.response.getRespondentEmail();

  var mail_text = "";

  mail_text += "【メールアドレス】\n" + email + "\n";
  mail_text += "【内容1】\n" + itemResponses[0].getResponse() + "\n";
  mail_text += "【内容2】\n" + itemResponses[1].getResponse() + "\n";
  mail_text += "【内容3】\n" + itemResponses[2].getResponse() + "\n";
  mail_text += "【内容4】\n" + itemResponses[3].getResponse() + "\n";
  mail_text += "【内容5】\n" + itemResponses[4].getResponse() + "\n";
  mail_text += "【内容6】\n" + itemResponses[5].getResponse() + "\n";
  mail_text += "【内容7】\n" + itemResponses[6].getResponse() + "\n";
  mail_text += "【内容8】\n" + itemResponses[7].getResponse() + "\n";
  mail_text += "【内容9】\n" + itemResponses[8].getResponse() + "\n";
  mail_text += "【内容10】\n" + itemResponses[9].getResponse() + "\n";

  
  GmailApp.sendEmail(
    "メールアドレス",
    "件名",
    mail_text + "\n"

  );

}

```
