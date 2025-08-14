Introduccion

Un monitor es un mecanismo de sincronizacion. 
Tiene como caracteristicas:
    - Exclusion mutua implicita: no es necesario usar lock o mutex explicitos.
    - Variables de condicion: permiten a los hilos esperar a ser notificados de que una condicion se cumple (metodos: wait(), signal(), notify()).
    - Encapsulacion.
Funcionamiento:
    1. Cuando un hilo entra a un metodo del monitor, adquiere implicitamente un lock interno.
    2. Si otro hilo intenta ejecutar un metodo del metodo mientras el primero no ha salido, queda bloqueado.
    3. Dentro del monitor, si un hilo necesita esperar a que ocurra un evento, llama a wait(), liberando el lock y queda a la espera.
    4. Otro hilo puede llamar a signal() o notify() para despertar a uno o mas hilos en espera.