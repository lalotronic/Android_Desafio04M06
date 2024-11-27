######  Desafío  - Consumo de API REST (II) #######

### Los requerimientos son los siguientes:

- Actualizar la clase `RepositoryImp` para poder trabajar con el endpoint y guardar los datos en
  Room.m
    - Para resolver este req. debemos modificar la función `getRemoteWeatherData()` en la
      clase `RepositoryImp` y permitir guardar en Room solamente cuando `ServiceResponse.Success`
      ocurra.
    - Podemos reutilizar la función `insertData(weatherDto: WeatherDto)` para guardar los datos
- Implementar la funcionalidad Pull To Refresh, siguiendo lo que se explica en el punto 6 de los
  requerimientos técnicos.
- Mostrar los datos usando `StateFlow` y usar el método `collect()` correctamente, es decir, cuando
  la base de datos tenga cambios, estos se deben mostrar en la vista automáticamente.
- Permitir al usuario cambiar entre Métrico a Imperial y viceversa (tal y como se explica en el
  punto 8)


#### Algunos leves cambios ####
-Se modificaron las funciones de conversiones de temperatura para que se mostraran con solo 2 
 decimales(con redondeo)
 
-Se agregaron mas codigos de estado http de manejo de errores: 400, 403 en WeatherRepositoryImp y 
 en Constants.
# Android_Desafio04M06
