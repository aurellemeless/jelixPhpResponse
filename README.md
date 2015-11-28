# jelixPhpResponse
PHP response for Jelix frameworks, it allow you to use php code inside templates with the ".php" file extension.
Usage
--------------
First put the phpResponse class in your app responses directory '/responses/' 

like that '/responses/phpResponse.class.php'

Second declare the response in your app config file '/var/config/mainconfig.ini.php'

or in the entrypoint configuration file 'config/index/config.ini.php'

For Example :

```php
[responses]
html=myHtmlResponse
...
php=phpResponse
```
Create template in your module templates directory '/modules/your_module_name/templates/mytemplate.php' with the '.php' extension

use phpResponse in your controller
```php
<?php

class defaultCtrl extends jController {
    
    function index() {
        $rep = $this->getResponse('php');
        $rep->tplname = "mytemplate";
        $rep->assign('salut','<h1>  Mou kwaba ooh! </h1>');
        return $rep;
    }
    
}
```
Changelog
--------------
0.1 put in github
