#PHP编码规范

0.文件夹

文件夹的名字使用全小写，尽量使用一个单词或者复数形式，多个单词时可以使用多个单词的缩写

1.文件名

文件中只包含一个类的定义时，文件名使用和类名一样的大驼峰命名；文件是脚本形式（直接拿来运行的脚本），文件名使用全小写，尽量一个单词。

2.类名

类名使用大驼峰命名

3.方法名

方法名使用动宾结构的小驼峰命名

4.方法的可见权限

方法的可见性，请使用最严格的可见性，能private,优先private,然后才是protected和public

5.常量和变量命名

常量的命名请使用全大写，对于多个单词的，请使用下划线连接单词

变量和属性的命名,如果是一个单词请使用全小写，如果是多个单词请使用小驼峰命名。对于类的private 属性，请使用'_'为前缀

6.代码的排版

``` php

// CActiveRecord.php文件

class CActiveRecord extends CModel
{

    const BELOGNS_TO='CBelongsToRelation';
    const STAT='CStatRelation';

    public static $db;
    private static $_models = array();

    public $_public = false;
    private $_related = array();
    private $_c;
    private $_pk;

    public function __construct()
    {
    
    }

    public function init()
    {
    
    }

    public function cache($duration,$dependency=null,$queryCount=1)
    {
        $this->getDbConnetion()->cache();
        return $this;
    }

    public function methodWithForeach()
    {
        foreach()
        {
        
        }
    }
    
    public function methodWithIfElse()
    {
        if()
        {
        
        }
        else
        {
        
        }



        if()
        {
        
        }
        elseif()
        {
        
        }
        else
        {
        
        }
    }
        
    public function methodWithSwitch()
    {
        switch()
        {
            case E_WARNING:
                $type = 'PHP warning';
                break;
            default:
                $type = 'PHP error';
        }
    
    }


    public function methodWithWhile()
    {
        while()
        {
            //dosomething
        }

        while($this->strlen($bytes)<$length &&
             ($byte=$this->methodDoSomething())!==false &&
             ++$i<3)
        {
           //dosomething 
        } 
    
    }

    protected function getSomething()
    {
    
    }


    private function initSomething()
    {
    
    }


}


```

7.附录

a.对于字符串，能使用单引号，优先使用单引号，必须使用双引号才使用双引号

b.禁止sql的字符拼接

c.优先使用foreach,如果必须要使用for,请将上线或下线的求值表达式放在for的外面，最后如果$i++和++$i是一样的意义，请使用$i++


