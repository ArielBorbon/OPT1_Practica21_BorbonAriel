## Ariel Eduardo Borbon Izaguirre 252116


¿qué pieza de React Router corresponde a router-outlet, a routerLink y a routerLinkActive?
- router-outlet = < Outlet/>
- routerLink = < Link to="...">
- routerLinkActive = < NavLink > (porque adentro trae isActive)


¿por qué la ruta comodín (**) va al final y la ruta vacía necesita pathMatch: 'full'?
- La ruta ** va al final porque el enrutador checa de arriba hacia abajo, si estuviera al inicio se cachara en todas las rutas de abajo
- la ruta vacia necesita pathMatch: 'full' porque todas las rutas empiezan vacias, si se evaluara por prefijo todas las navegaciones hicieran click con esta


¿dónde vive el valor de un campo en un formulario reactivo y en qué se diferencia del useState de React?
- Adentro de FormControl (el cual esta adentro de FormGroup), la diferencia con use State es que en angular para actualizar el valor actualiza el modelo del usuario de forma silenciosa sin renderizar todo el componente completo


¿qué regresa un validador propio cuando el valor es válido y cuando no, y cómo se relaciona con hasError?
- cuando es valido deberia ser null, sino deberia regresar el error (como duracionInvalida = true)
- se relaciona con hasError porque la key de este es el parametro que usa la vista para checar la falla (control.hasError('duracionInvalida'))


¿qué cambió en el servicio del catálogo y por qué ningún componente se enteró?
- nadie se entero por la encapsulacion, al manejarse con interfaces no importa de donde lleguen los datos mientras se cumpla esto, por lo que gracias a esto no paso nada 


¿por qué no hizo falta iniciar sesión para leer el catálogo?
-  porque GET /clases es publico, osea que no ocupas JWT para entrar, y pues es el comportamiento esperado, seria raro si en esta pagina o un sitio como amazon tuvieras que iniciar sesion para ver todo el catalogo de cosas