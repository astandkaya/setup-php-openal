# setup-php-openal

## setup

### 呪文
```
sudo apt update
sudo apt install php \
	php-cli \
	php-pear \
	php-dev \
	libalut0 \
	libalut-dev \
	libopenal1
```

### OpenALのモジュールをビルドする
```
phpize
./configure --with-openal=../openal-soft
make
sudo make install
```

### phpのiniファイルに追加
```
extension=openal
```

## example

php-openalに同梱されているサンプルを実行する
```
cp -r ./php-openal/examples examples
cd examlpes
composer install
php example.php
```
