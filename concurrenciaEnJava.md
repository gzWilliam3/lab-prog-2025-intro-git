Introduccion

Un monitor es un mecanismo de sincronizacion. 
Tiene como caracteristicas:
    - Exclusion mutua implicita: no es necesario usar lock o mutex explicitos.
    - Variables de condicion: permiten a los hilos esperar a ser notificados de que una condicion se cumple (metodos: wait(), signal(), notify()).
    - Encapsulacion.
    