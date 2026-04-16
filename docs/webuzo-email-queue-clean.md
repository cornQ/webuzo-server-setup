## Cleaning Email Queue

### From panel

Go to **Webuzo Admin Panel > Email > Email Queue Manager**.

There you can:

- Select emails and click **Delete Selected**
- Or click **Delete All** to clear the whole queue

### From command line as root

Run the following CLI command for clearing the email queue.

```bash
webuzo --delete_email_queue
```

!!! danger 
    Deleting queue entries is irreversible and cannot be undone!

Running the following command will show how many messages are in the queue.

```bash
exim -bpc
```


