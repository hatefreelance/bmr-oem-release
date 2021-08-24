# Описание процесса и требований для релиза проектов BMA и OEM

## Требования к софту сервера

### 1. Проект BMA

Под этот сайт, а также другие небольшие корп. сайты клиента ставится отдельный сервер.
Требуется развернуть проект в 2-х экземплярах: 
dev.businessmediarussia.ru - дев
businessmediarussia.ru - продакшн

- [ОС CentOS 8](https://www.centos.org/download/)
- [Composer](https://getcomposer.org/).
- [Nginx](https://www.nginx.com/).
- [Mysql 5.7+](https://www.mysql.com/).
- [PHP 7.4.x](https://www.php.net/downloads.php#v7.4.16).

#### Стэк LEMP
Для простоты поддержки проекта в будущем ставим это все на LEMP стэк с панелькой управления [aapanel](https://www.aapanel.com/)
После установки aapanel директория создаваемых сайтов будет устанавливаться в /www/wwwroot.
Это позволит проще развернуть на этом окружении другие корп. сайты клиента.

#### Необходимые расширения PHP
- FileInfo
- GD Library (>=2.0) или Imagick PHP extension (>=6.5.7)
- BCMath PHP Extension
- Ctype PHP Extension
- Fileinfo PHP Extension
- JSON PHP Extension
- Mbstring PHP Extension
- OpenSSL PHP Extension
- PDO PHP Extension
- Tokenizer PHP Extension
- XML PHP Extension

Wiki по деплою самого проекта [здесь](https://github.com/Codeband-Digital/laravel-projects-wiki)

### 2. Проекты OEM Конфигуратор и Интерфейс Организаторов
Оба проекта работают на [1C-Битрикс](https://www.1c-bitrix.ru/) версии 20.х, редакция "Малый Бизнес".
Для них будет создаваться отдельный сервер.

Окружение и софт можно ставить аналогичные проекту, описанному в пункте 1.
Перенос сайта осуществляется с помощью встроенной системы бэкапов Битрикс силами разработчиков.

