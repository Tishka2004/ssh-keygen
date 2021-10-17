### Настройка Git и GitHub

*Для начала создадим новый SSH ключ с кодовой фразой *

```bash
ssh-add -l
```

```bash
ssh-add -D
```

```bash
mkdir -p ~/.ssh
```

```bash
lsd -la ~/.ssh
```

```bash
ssh-keygen -o -a 100 -t ed25519 -f ~/.ssh/id_ed25519_github -C "vdodevko email trololo"
```

### Добавление SSH-ключа в ssh-agent

```bash
eval "$(ssh-agent -s)"
```

```bash
ssh-add ~/.ssh/id_ed25519_github
```

### Добавление нового ключа SSH в учетную запись GitHub

```bash
xclip -sel clip < ~/.ssh/id_ed25519_github.pub
```

*Заходим на страницу **[https://github.com/settings/keys](https://github.com/settings/keys)** и добавляем ключ из буфера обмена.*

*После добавления нового SSH-ключа в вашу учетную запись GitHub можно перенастроить любые локальные репозитории для использования SSH. Дополнительные сведения смотрите в разделе **[переключение удаленных URL-адресов с HTTPS на SSH.](https://help.github.com/articles/changing-a-remote-s-url/#switching-remote-urls-from-https-to-ssh)** Дальше следует протестировать SSH-соединение.*

### Тестирование SSH-соединения

```bash
ssh -T git@github.com
```

### Появится запрос ввода кодовой фразы и после неё установится соединение

```bash
Are you sure you want to continue connecting (yes/no)? yes

Hi! You've successfully authenticated,
but GitHub does not provide shell access.
```
