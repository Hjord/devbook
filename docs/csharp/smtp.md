## Send mail with SMTP 

Google SMTP settings:

- Host: `smtp.google.com`
- Port: `587`
- Remember `EnableSsl = true`

### Example
```csharp
MailAdress sender = new MailAdress(mailFrom, mailFromName);
MailAdress receiver = new MailAdress(mailTo);

MailMessage mail = new MailMessage(sender, receiver)
                {
                    Subject = "Subject",
                    Body = "Body text"
                };
                
SmtpClient client = new SmtpClient
                {
                    Port = port,
                    EnableSsl = true,
                    DeliveryMethod = SmtpDeliveryMethod.Network,
                    Credentials = new System.Net.NetworkCredential(smtpUsername, smtpPassword),
                    Host = smtpHost
                };
client.Send(mail);
```

- `smtpUsername` your gmail.
- `smtpPassword` your gmail password

[Google App Password](https://myaccount.google.com/apppasswords) can be used instead of gmail password.


