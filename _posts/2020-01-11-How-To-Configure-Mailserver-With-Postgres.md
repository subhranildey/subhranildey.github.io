---

title: Mailserver with Postgres

published: true
---

## Mail stack:
 - Postfix (SMTP)
 - Dovecot (IMAP/POP3)
 - Roundcube (IMAP Client)
 - PostgreSQL (DB)

### [Click here to see Database ER Diagram](https://gitlab.com/yukthi-mail-v2-devs/yukthi-mail-v2/uploads/42479833b0e4ecc38f9c9467bbc109d6/ER-Diagram.png)

#### Install Requied Packages
 
 ```
 apt -y install dovecot-core dovecot-pop3d dovecot-imapd dovecot-pgsql dovecot-lmtpd
 apt -y install postfix postfix-pgsql
 apt -y install postgresql-11 postgresql-client-11
 apt -y install certbot
```

#### Clone the Repo & Initialise DB

```
 git clone git@gitlab.com:yukthi-mail-v2-devs/yukthi-mail-v2.git
 cd  yukthi-mail-v2/postgres
 sudo chown postgres:postgres init-user-db.sh
 sudo cp init-user-db.sh /var/lib/postgresql
 sh init-user-db.sh
```
* Use `dbdump.sql` to import database

### Configure SSL


 ```
 certbot certonly --standalone -d $(hostname -f)
```

### Because valid UNIX user and group id's are needed to store the mailboxes, those should be created as well.

```
groupadd -g 5000 vmail
useradd -m -d /var/vmail -s /bin/false -u 5000 -g vmail vmail
chown vmail:vmail /var/vmail/
chmod 2770 /var/vmail/
```

### Steps to setup Postfix & Dovecot

 * Update variables in `config.sh`

```
sh config.sh

```
