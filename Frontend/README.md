## Ariel Eduardo Borbon Izaguirre 252116

¿qué diferencia hay entre un signal y un computed, y cuál se parece a useState y cuál a useMemo?
- un signal (seria como el useState), es un contenedor para leer y escribir, tiene un estado y expone los metodos set y update para actualizarlos, si el valor cambio se notifica a angular y se actualiza lo que cambio

- computed (useMemo) es un valor derivado de solamente lectura que depende de otros signals, los guarda en cache y solo se ejecuta cuando uno de los signals de los que depende cambia


¿qué pasa si el filtro hace new Catalogo() en lugar de inject(Catalogo)?
- si en el filtro categoria se hace new Catalogo() matas al patron singleton

- con inject(Catalogo) angular se asegura que el componente app como FiltroCategoria usen exactamente la misma instancia en memoria para que se comparta todo

- si se usa new Catalogo(), el filtro creara otra instancia del servicio aparte, si el usuario presiona un boton, el filtro cambiara categorias en su instancia, pero en app estara viendo la instancia original, por lo que la pantalla quedara igual y no habra filtrado