

```csharp
MailMessage mail = new MailMessage(new MailAddress(mailFrom, mailFromName), new MailAddress(mailTo))
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

