---
layout: post
title:  "Интеграция Post Affiliate Pro "
date:   2018-01-22 09:00:00 +0300
categories: papro
---

# Введение #
Для начала работы необходимо подключить вендорный класс `PapApi.class.php`

Эти и многие другие примеры можно найти [здесь][papro-docs]

# Login #

- `$this->server` - сервер, на котором установлен papro
- `$login` - логин мерчанта
- `$pass` - пароль мерчанта

{% highlight php %}
$session = new \Pap_Api_Session($this->server);

if (!$session->login($login, $pass)) {
    die("Cannot login. Message: ".$session->getMessage());
}
$this->session = $session;

return $session;
{% endhighlight %}

[papro-docs]: https://support.qualityunit.com/
