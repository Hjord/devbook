## Send mail with SMTP

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

