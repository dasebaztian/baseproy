# Justificación Diagrama Entidad-Relación
## Tablas
### Candidato
Se crea la identidad candidato para poder identificar a cada persona que quiere, quiso o esta actualmente participando en un empleo ofrecido por un empleador, además este cuenta con atributos que describen su perfil profesional.

### Empleador
Aquí se guardan unos datos para poder identificar al empleador dentro de la plataforma

### Empleo
Aquí se guardan datos relevantes para poder identificar al empleo y hacer la relación con las demás entidades.

### Habilidades
Aquí se van a guardar las habilidades de cada candidato, se ponen los atributos que describen a cada tipo de habilidad cómo multivalorados para evitar tener redudancia en la información.

### Accesos
Aquí se va a guardar la información de acceso de los candidatos y los empleadores.

## Relaciones

### Relación de candidato-habilidades (Tiene)
Se crea esta relación para evitar la redundancia en la tabla de candidato.

### Relacion candidato-acceso (Tiene)
Es de 1 a uno ya que un acceso solo le corresponde a un candidato.

### Relacion empleador-acceso (Tiene)
Es de 1 a uno ya que un acceso solo le corresponde a un empleador.

### Relación candidato-empleo (Trabaja)
Esta relación cumple la función de relacionar un candidato con el empleo, una vez que el candidato se postuló al empleo y el empleador lo aceptó. Esta relación guarda atributos importantes para verificar si se ha comprobado el pago y las calificaciónes de los involucrados.

### Relación candidato-empleo (Aplica)
Esta relación funciona para guarda todas las postulaciones de varios candidatos a varios empleos, por lo que es de muchos a muchos. Además aquí se guarda un elemento que permite verificar si ha sido aceptado el candidato por el empleador, lo que activaria el trigger que guardaria la información en la relación Trabaja.
