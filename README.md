# Ruby-on-rails-mis-notasgem install rails
Documentacion Oficial https://rubyonrails.org/
 <br/>
 
### Índice 
* [Instalar Ruby on Rails en ARCH](#install_ruby_on_rails)
* [Que es Ruby on Rails](#que_es_ruby_on_rails)
* [Iniciar proyecto](#init_project)
* [Como crear un controlador](#controller)


 <br/>
 
 


</br>

 <a name="install_ruby_on_rails"></a>
### **Como instalar Ruby on Rails en Linux ARCH**
Para instalar ruby on rails necesitamos como dependencias, instalar ruby y rvm. Pero para instalar rvm necesitamos instalar curl
```
sudo pacman -S curl
```


</br>

Instalamos rvm, este comando instalara rvm y configura bashrc para poder usar rvm
```
\curl -sSL https://get.rvm.io | bash
```

Para comenzar a usar RVM, debemos ejecutar source /usr/local/rvm/scripts/rvm para agregarlo al archivo /usr/local/rvm. usa el siguiente comando
```
source /usr/local/rvm/scripts/rvm
```

para que los cambios hagan efecto
```
rvm reload
```

```
rvm requirements
```

Para ver la lista de versiones de ruby
```
rvm list known
```

Vamos a instalar la version 3.0.3
```
rvm install ruby 3.0.3
```

Para saber la version de Ruby
```
ruby --version
```

Para saber la version de rvm
```
rvm version
```

</br>

Procedemos a instalar Rails
```
gem install rails
```

Hacemos algo muy importante, poner la version de ruby por defecto
```
rvm use 3.0    
```

</br>

 <a name="que_es_ruby_on_rails"></a>
### **Que es Ruby on rails**
Es un framework de Ruby para crear sistemas web, de tipo rest Full, estoy quiere decir que podemos hacer backend y Frontend al mismo tiempo, muy parecido como PHP (LARAVEL) y PYTHON (DJANGO)
</br>

 <a name="init_project"></a>
### **Iniciar Proyecto**
Para crear un proyecto, hacemos uso del comando rails, en este framewor usaremos rails para muchas cosas,  tipeamos el siguiente comando para crear el proyecto. Tambien es importante saber que Rails usa por defecto sqlite3. En rby no hay package.json esta el gemfile o archivo de gemas, donde estan las librerias instaladas en el proyecto.  

Rails crear 3 entornos de base de datos o mejor dicho 3 bases de datos para cada entorno. la db develoment que es para desarrollo, la db testing que es para pruebas y la db production, que es para produccion

```
rails new nombre_del_proyecto   
```

Para correr el servidor, podemos tiperar server o s
```
rails server  
```

Si queremos instalar una nueva gema, agregamos la gema al gemfile y para instalar copiamos este comando
```
bundle inestall
```
</br>


 <a name="controller"></a>
### **Como crear un Controlador**
Si deseamos crear un metodolo  (index) hacemos como se muestra en el comando, esto es opcional. La primera le tra del nombre del controlador en Mayuscula
```
rails generate controller name_controller name_method  
```

</br>

 <a name="model"></a>
### **Las Rutas**
Tenemos un archivo dentro config >> routes
cada vez que generamos un controlador se crea una ruta y una vista para esa ruta. a cada ruta le antecede el verbo HTTP que se relaciona con esa ruta.  
Ejemplo:  
get 'home/index'  
a esta ruta le antece el verbo HTTP GET, asi que es para obtener datos

</br>

 <a name="model"></a>
### **Como crear un Modelo**
Es importante crear el modelo con nombre singular, primera letra en mayuscula y el nombre en ingles
```
rails generate model name_model  
```

Pero tenemos la opcion de crear el modelo en el mismo comando, si no se pone el tipo de datos rails asume que es char
```
rails generate model name_model  title body:text visits_count:integer
```

Para crear la base de datos ejecutamos
```
rake db:create
```

Para levantar las tablas debemos correr las migraciones
```
rake db:migrate
```

Como ejecutar un rollback
```
rake db:rollback
```

</br>

**Consola de Rails**
Esta interesante, aqui podremos hacer varias cosas, por ejemplo queremos sabe la query para traernos todos los articulos de la tabla articulos, como por dar un ejemplo
```
rake console
```
```
Article.all
```
eso devolvera todos los articulos

</br>

</br>

### **Fuentes**
https://nextgentips.com/2021/11/02/how-to-install-ruby-on-rails-on-rocky-linux-8/
