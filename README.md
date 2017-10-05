# LaravelTinkering

index.php -> Front Controller


//Cruddy by design CRUD -> Create Update Retrieve Delete
//Route::post
//Route::put
//Route::delete

Per a veure les rutes actives al nostre projecte de laravel executarem la següent línia dins el directori de projecte:

    php artisan route:list

Exemple de nova ruta al fitxer ``routes/web.php``:
    
    Route::get('home', function (){
       echo "Hola sóc la HOME";
    });
    
Imprimeix el missatge ``Hola sóc la HOME``


Per crear un nou controlador des de la terminal:

    php artisan make:controller nom_controller
    
Amb ``-r`` ens crea el CRUD automaticament

    php artisan make:controller -r nom_controller
   
Amb ``-m`` també ens generara el model

    php artisan make:controller -m nom_model -r nom_controller
    
Quan tinguem el fitxer de migracions creat i preparat executarem 

    php artisan migrate

per a que es creïn totes les taules especificades al fitxer de migració

En cas de voler executar una línia de codi independent utilitzarem

    php artisan tinker

Podrem resetejar totes les bases de dades amb la comanda:

    php artisan migrate:fresh