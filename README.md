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


1.  آموزش قدم به قدم نصب لاراول ۱۰ با استفاده از زمپ در اوبنتو
2. نصب Laravel 10 با استفاده از ZAMPP در Ubuntu را می توان در چند مرحله جداگانه انجام داد. دقت داشته باشید که ZAMPP یک نرم افزار برای اجرای سرور وب است که شامل Apache، MySQL و PHP است.

1. نصب ZAMPP:
   - ابتدا باید ZAMPP را از وبسایت رسمی Apache Friends دریافت کنید.
   - فایل دانلود شده را با استفاده از دستور زیر در محل دلخواه خود استخراج کنید:
     ```
     tar xvfz xampp-linux-x64-7.4.23-0-installer.run.tar.gz -C /opt
     ```
   - سپس به پوشه نصب ZAMPP بروید:
     ```
     cd /opt/lampp
     ```
   - برای اجرای ZAMPP، دستور زیر را وارد کنید:
     ```
     sudo ./xampp start
     ```

2. نصب Composer:
   - برای نصب پکیج ها و وابستگی های Laravel، نیاز به نصب Composer داریم.
   - برای نصب Composer، دستورات زیر را به ترتیب اجرا کنید:
     ```
     cd ~
     curl -sS https://getcomposer.org/installer -o composer-setup.php
     sudo php composer-setup.php --install-dir=/usr/local/bin --filename=composer
     ```

3. ساخت پروژه Laravel:
   - برای ساخت پروژه Laravel جدید، از دستور زیر استفاده می کنیم:
     ```
     composer create-project --prefer-dist laravel/laravel project-name
     ```
     در این دستور، `project-name` نام پروژه مورد نظر شما است. می توانید هر نامی را برای پروژه انتخاب کنید.

4. اجرای پروژه Laravel:
   - به پوشه پروژه خود بروید:
     ```
     cd project-name
     ```
   - برای اجرای پروژه، از دستور زیر استفاده کنید:
     ```
     php artisan serve
     ```

بعد از اجرای این دستور، سرور توسعه Laravel روی پورت 8000 راه اندازی می شود و می توانید پروژه Laravel خود را در مرورگر با استفاده از آدرس `http://localhost:8000` مشاهده کنید.

با اجرای این مراحل، شما Laravel 10 را با استفاده از ZAMPP در Ubuntu نصب کرده و یک پروژه جدید ایجاد کرده اید.
