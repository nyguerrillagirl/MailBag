# MailBag Project

## Server Part

Basic Requirements
* MailBag will be in two parts: a server, which will act as a proxy and will be what communicates with a mail server somewhere, and the client, which will talk to our server to do its work.
*	MailBag server will communicate with an email server. The details on how to communicate will be stored in a file. The server will use the IMAP protocol for retrieving mail and SMTP for sending messages.
*	The MailBag server shall provide an API to the client that allows it to get a list of mailboxes for the account, a list of messages for a selected mailbox, and pertinent message details for display by the client. The user shall be allowed to delete and send messages. The server shall also provide for storage contacts and the associated add and delete functions for maintaining them.

Missing File:
At the root level there is a file named ServerInfo.ts with the information to access the
* SMTP server 
* IMAP server

The file format:
```
{
  "smtp" : {
    "host" : "my_smtp_server_address",
    "port" : 465,
    "auth" : {
      "user" : "my_smtp_username",
      "pass" : "my_smtp_password"
    }
  },
  "imap" : {
    "host" : "my_imap_server_address",
    "port" : 993,
    "auth" : {
      "user" : "my_imap_username",
      "pass" : "my_imap_password"
    }
  }
}
```