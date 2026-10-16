create
Curso de Laravel Completo Creando una página web *3

composer create-project laravel/laravel ****
acceder a carpeta
cd ****
agregar 'active' en: Models/User
agregar active a DB_user 
 $table->boolean('active')->default(0);
php artisan migrate
verificar BD

stylos
composer require laravel/ui
    los paquetes
php artisan ui:auth     (autenticacion)Se agrega views/auth- y sus pack


php artisan ui bootstrap


npm install
npm run dev
***npm run build

 autenticacion
	    4)* auth:login:registro
			nos registramos 
			user:ergiosdev@gmail.com
			pass:obarrio2272
					*probar roles*
		cambiarcampoen BD/user/active-de 0 a 1
        en 
            App\Http\Controllers\Auth/loginController.php

                public function redirectPath()
    {
        if (\Auth::user()->active ===1)  {
            return '/home';//mas tarde en administrasor
        } else {
            \Auth::logout();
            return '/';
        }
    }
    

copiar conitnido de home a  welcome