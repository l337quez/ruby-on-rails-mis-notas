# Ruby-on-rails-mis-notasgem install rails

 <br/>
 
### Índice 
* [Instalar Ruby on Rails en ARCH](#install_ruby_on_rails)
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

 <a name="init_project"></a>
### **Iniciar Proyecto**
Para crear un proyecto, hacemos uso del comando rails, en este framewor usaremos rails para muchas cosas,  tipeamos el siguiente comando para crear el proyecto
```
rails new nombre_del_proyecto   
```

Para correr el servidor, podemos tiperar server o s
```
rails server  
```
</br>


 <a name="controller"></a>
### **Como crear un Controlador**



</br>

### **Fuentes**
https://nextgentips.com/2021/11/02/how-to-install-ruby-on-rails-on-rocky-linux-8/
