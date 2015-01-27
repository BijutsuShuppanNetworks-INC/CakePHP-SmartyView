Cakephp-SmartyView
==================

CakePHP用Smarty設定プラグイン
- CakePHP 2.0以上
- Smarty 2.6/3.1

## インストール
app/Plugin以下にディレクトリ名「SmartyView」で設置

    git clone git://github.com/BijutsuShuppanNetworks-INC/CakePHP-SmartyView.git SmartyView


## 使い方

### Smarty本体のインストール
Smarty本体をapp/Vender以下にディレクトリ名「smarty」で設置

### Smarty用一時ディレクトリ作成
下記ディレクトリを作成
- tmp/smarty/cache
- tmp/smarty/compile

### プラグイン読み込み
app/Config/bootstrap.phpで「SmartyView」プラグインを読み込む記述の追加

    CakePlugin::load('SmartyView');

### Viewクラス指定
app/Controller/AppController.phpでViewクラスに「SmartyView」を使用する記述の追加

    class AppController extends Controller {   

        ...      
    
        public $viewClass = 'SmartyView.Smarty';

        ...
    }

### tplファイルの用意
app/View以下にSmartyテンプレートファイルを拡張子「tpl」で用意する