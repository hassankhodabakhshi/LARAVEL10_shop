1. Step-by-step tutorial on how to install Laravel 10 using xampp and Ubuntu
2. Sure! Here's a step-by-step tutorial on how to install Laravel 10 using XAMPP and Ubuntu:

Step 1: Install XAMPP
- Download XAMPP for Linux from the Apache Friends website (https://www.apachefriends.org/index.html).
- Open a terminal and navigate to the directory where the XAMPP installer is located.
- Run the following command to make the installer executable:
  ```
  chmod +x <xampp-installer>.run
  ```
  Replace `<xampp-installer>` with the actual name of the installer file.
- Run the installer using the following command:
  ```
  sudo ./<xampp-installer>.run
  ```
- Follow the on-screen instructions to complete the XAMPP installation.

Step 2: Install Composer
- Open a terminal and navigate to the directory where you want to install Composer.
- Run the following command to download and install Composer:
  ```
  php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
  php composer-setup.php
  php -r "unlink('composer-setup.php');"
  ```
- Move the `composer.phar` file to a globally accessible location by running the following command:
  ```
  sudo mv composer.phar /usr/local/bin/composer
  ```

Step 3: Install Laravel
- Open a terminal and navigate to the `htdocs` directory inside the XAMPP installation folder:
  ```
  cd /opt/lampp/htdocs
  ```
- Run the following command to create a new Laravel project:
  ```
  composer create-project --prefer-dist laravel/laravel <project-name>
  ```
  Replace `<project-name>` with the desired name for your Laravel project.
- Once the installation is completed, navigate to the project directory:
  ```
  cd <project-name>
  ```
  Replace `<project-name>` with the actual name of your Laravel project.

Step 4: Configure XAMPP
- Open a terminal and run the following command to start the XAMPP server:
  ```
  sudo /opt/lampp/lampp start
  ```
- Open your preferred web browser and visit `http://localhost/phpmyadmin`.
- Create a new database for your Laravel project.

Step 5: Configure Laravel
- Duplicate the `.env.example` file located in the root directory of your Laravel project and rename it to `.env`:
  ```
  cp .env.example .env
  ```
- Open the `.env` file and modify the following configurations:
  ```
  DB_DATABASE=<your-database-name>
  DB_USERNAME=root
  DB_PASSWORD=
  ```
  Replace `<your-database-name>` with the name of the database you created in Step 4.

Step 6: Run Laravel
- Open a terminal and navigate to your Laravel project directory if you're not already there.
- Run the following command to generate an application key:
  ```
  php artisan key:generate
  ```
- Finally, start the local development server by running the following command:
  ```
  php artisan serve
  ```
- Open your web browser and visit `http://localhost:8000` to see your Laravel application in action.

That's it! You have successfully installed Laravel 10 using XAMPP and Ubuntu. You can now start building your Laravel application.


1.  آموزش قدم به قدم نصب لاراول ۱۰ با استفاده از نرم افزار xampp in ubuntu
2.  نصب Laravel 10 را در Ubuntu با استفاده از نرم افزار XAMPP می‌توان به سادگی انجام داد. در ادامه، شما را قدم به قدم از نصب XAMPP تا ایجاد یک پروژه Laravel همراهی می‌کنم:

1. نصب XAMPP:
   - دستورات زیر را در ترمینال اجرا کنید تا بسته XAMPP را دانلود کنید:
    ```
    wget https://www.apachefriends.org/xampp-files/7.4.21/xampp-linux-x64-7.4.21-1-installer.run
    ```
   - سپس به بسته اجرایی دسترسی اجرا بدهید:
    ```
    chmod +x xampp-linux-x64-7.4.21-1-installer.run
    ```
   - در نهایت، بسته را نصب کنید:
    ```
    sudo ./xampp-linux-x64-7.4.21-1-installer.run
    ```
   - دستوراتی که می‌بینید را در طول نصب دنبال کنید و XAMPP را در مسیر پیش‌فرض نصب کنید.

2. راه‌اندازی XAMPP:
   - با اجرای دستور زیر، پنل کنترل XAMPP را باز کنید:
    ```
    sudo /opt/lampp/manager-linux-x64.run
    ```
   - در پنل کنترل، آپاچی و مای‌اس‌کیو‌ال را فعال کنید و سرویس‌ها را راه اندازی کنید.

3. نصب Composer:
   - دستورات زیر را در ترمینال اجرا کنید تا Composer را دانلود و نصب کنید:
    ```
    php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
    php composer-setup.php
    php -r "unlink('composer-setup.php');"
    ```
   - سپس Composer را به مسیر پیش‌فرض نصب کنید:
    ```
    sudo mv composer.phar /usr/local/bin/composer
    ```

4. ایجاد یک پروژه Laravel:
   - در ترمینال، دستور زیر را اجرا کنید تا پروژه Laravel جدیدی را ایجاد کنید:
    ```
    composer create-project --prefer-dist laravel/laravel myproject
    ```
   - پروژه Laravel جدید حالا در پوشه myproject ایجاد شده است.

5. اجرای پروژه Laravel:
   - با دستور زیر، به پوشه پروژه بروید:
    ```
    cd myproject
    ```
   - برای اجرای پروژه، سرویس‌های Apache و MySQL را اجرا کنید:
    ```
    sudo /opt/lampp/lampp start
    ```
   - سپس در مرورگر وب، به آدرس `http://localhost/myproject/public` بروید و صفحه خوش‌آمدگویی Laravel را ببینید.

به این ترتیب، شما Laravel 10 را در Ubuntu با استفاده از XAMPP نصب کردید و پروژه‌ای را ایجاد و اجرا کردید. اکنون می‌توانید با پروژه خود کار کنید و برنامه‌های Laravel خود را توسعه دهید.
