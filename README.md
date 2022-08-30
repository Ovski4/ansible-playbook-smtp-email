SMTP email
==========

This playbook will send an email via SMTP.

Usage example
-------------

### With ansible

```bash
ansible-playbook /var/smtp-email-playbook/main.yml \
    -e "smtp_user=user@gmail.com" \
    -e "smtp_password=fake_password" \
    -e "smtp_port=465" \
    -e "smtp_host=smtp.gmail.com" \
    -e "mail_to='User client <user.client@gmail.com>'" \
    -e "mail_subject=Hello" \
    -e "mail_body='Content of the email'"
```

### Using the ansible docker image with the docker-compose configuration

Update the `docker-compose.yml` file according to your needs, then run:

```
docker-compose run smtp-email
```
