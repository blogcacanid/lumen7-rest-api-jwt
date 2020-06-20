# lumen7-rest-api-jwt
Rest API Dengan JSON Web Token Lumen 7

> https://blog.cacan.id/rest-api-dengan-json-web-token-lumen-7

![000](https://user-images.githubusercontent.com/51890752/85202218-0cee4c80-b32f-11ea-910b-73e4330919d5.jpg)


# Cara Penggunaan:

## Clone dari GitHub:
git clone https://github.com/blogcacanid/lumen7-rest-api-jwt.git

## Lalu masuk ke direktori project:
cd lumen7-rest-api-jwt

## Selanjutnya jalankan perintah berikut secara berurutan:
- composer install
- cp .env.example .env
- php artisan key:generate

## Testing
Jalankan Lumen 7 dengan menggunakan perintah berikut:
- php -S localhost:8000 -t public

Lalu buka browser dan ketikkan URL http://localhost:8000

Untuk menjalankan Lumen 7 pada port tertentu, misalnya port 9090 anda bisa menjalankannya dengan mengetikkan perintah berikut:
php -S localhost:9090 -t public


### Testing via Postman
Selanjutnya kita akan testing menggunakan Postman.

#### Register
Pertama-tama kita daftarkan user baru terlebih dahulu agar kita bisa melakukan login.
Buka postman lalu pilih method POST kemudian ketikkkan URL http://localhost:8000/api/auth/register
Kemudian pilih tab Body. Lalu pada radiobox pilih raw dan typenya pilih JSON. Selanjutnya pada bagian textbox inputkan data registrasinya seperti berikut:
{
"name": "Rony",
"email": "rony@rony.com",
"password": "qwertyui",
"password_confirmation": "qwertyui"
}
Selanjutnya klik tombol Send


![002](https://user-images.githubusercontent.com/51890752/85202230-24c5d080-b32f-11ea-9e4a-5c8e05a2c9ec.jpg)


#### Login
Setelah registrasi berhasil selanjutnya kita coba untuk login dengan user yang sudah kita registrasikan tersebut.
Buka postman lalu pilih method POST kemudian ketikkkan URL http://localhost:8000/api/auth/login
Kemudian pilih tab Body. Lalu pada radiobox pilih raw raw dan typenya pilih JSON. Selanjutnya pada bagian textbox inputkan data email dan password untuk login:
{
"email": "rony@rony.com",
"password": "qwertyui"
}
Selanjutnya klik tombol Send

![003](https://user-images.githubusercontent.com/51890752/85202244-31e2bf80-b32f-11ea-90d9-ff0c2b0bfe83.jpg)

Jika login berhasil, maka kita akan mendapatkan access token. Access Token tersebut nanti akan kita gunakan untuk proses selanjutnya. 

##### Profile
Selanjutnya kita akan mencoba mengakses link Profile.
Link profile ini hanya bisa diakses dengan menggunakan token.
Buka postman lalu pilih method GET kemudian ketikkkan URL http://localhost:8000/api/auth/profile
Kemudian pilih tab Authorization. Lalu pada combo TYPE pilih Bearear Token. Selanjutnya pada textbox Token isi dengan data access token yang didapat pada saat login sebelumnya.
Selanjutnya klik tombol Send
![004](https://user-images.githubusercontent.com/51890752/85202248-3c04be00-b32f-11ea-8bb6-b426373ac256.jpg)


# Lumen PHP Framework

[![Build Status](https://travis-ci.org/laravel/lumen-framework.svg)](https://travis-ci.org/laravel/lumen-framework)
[![Total Downloads](https://poser.pugx.org/laravel/lumen-framework/d/total.svg)](https://packagist.org/packages/laravel/lumen-framework)
[![Latest Stable Version](https://poser.pugx.org/laravel/lumen-framework/v/stable.svg)](https://packagist.org/packages/laravel/lumen-framework)
[![License](https://poser.pugx.org/laravel/lumen-framework/license.svg)](https://packagist.org/packages/laravel/lumen-framework)

Laravel Lumen is a stunningly fast PHP micro-framework for building web applications with expressive, elegant syntax. We believe development must be an enjoyable, creative experience to be truly fulfilling. Lumen attempts to take the pain out of development by easing common tasks used in the majority of web projects, such as routing, database abstraction, queueing, and caching.

## Official Documentation

Documentation for the framework can be found on the [Lumen website](https://lumen.laravel.com/docs).

## Contributing

Thank you for considering contributing to Lumen! The contribution guide can be found in the [Laravel documentation](https://laravel.com/docs/contributions).

## Security Vulnerabilities

If you discover a security vulnerability within Lumen, please send an e-mail to Taylor Otwell at taylor@laravel.com. All security vulnerabilities will be promptly addressed.

## License

The Lumen framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
