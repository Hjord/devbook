# FTP

There are several ways to handle FTP in .NET

- WebClient
- FtpWebRequest


### Download from FTP

```csharp
using (WebClient client = new WebClient())
{
	client.Credentials = new NetworkCredential(ftpUsername, ftpPassword);
        client.DownloadFile(ftpLocation, localLocation);
}
´``

## Upload to FTP

```csharp
using (WebClient client = new WebClient())
{ 

	client.Credentials = new NetworkCredential(ftpUsername, ftpPassword);
	client.UploadFile(ftpLocation, "STOR", localLocation);

} 
```


- "STOR" ???
