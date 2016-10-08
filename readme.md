angular mvc

$digest: ciclo renderizado, renderiza solo los cambios
$apply: ciclo renderizado, renderiza todo! (no usar relentiza el sistema)

Angular: implementa patron observador (observer), puede tener diferentes nombres dependiendo el leguaje

$watcher: hacen referencia la patron observador
$scope: ambito de angular

el patron observador enlaza a la vista con el modelo
el $scope enlaza al controlador con el modelo

angular: alta coecion bajo acoplamiento, esto permite de manera facil la injecxion de dependencia.

$scopo... no es el modelo!



como injectar un modelo de verdad, es la mejor opcion para desarrollo movile, en navegadores de escritorio no interesa porque hay mas recursos.

//doble seteo
var vm= $scope.model = {
	params1 : "",
	params2 : ""
};

o

$scope.model={
	param1 : "",
	param2 : ""
}

var vm = $scope.model;

Los watcher u observadores son muy pesados, verificar antes de usar.

angular es de un solo hilo.

=======================================================================================================================

Directivas --> web compenent
Services --> con singleton
provider --> el provider puede ser un factory o un service (es la base de ambos).
factories --> sin singeleton

services es similar a fatories

es mejor usar un service que un $rootscope, tambien hay otras soluciones (el $rootscope no desaparese hasta que se cierra el navegador, no usarlo nunca!!)

warningup--> angular se inicia

manualbootstraping --> se inicia angular de manera manual

//Para ambientes dev/QA/prod usar lo siguiente:
.config: solo se pueden injectar providers!
ejemplo: .config($APIProviders) .config($API[Provider])

puedo tener muchos config

DI = dependenci injector


.run: en este momento ya existe angular, en este momento ya tenemos la carcasa

directiva:
<login></login>

deberia renderizar el login en pantalla.

podria tener un proyecto completo dentro de una directiva.

existen directivas de tipo elemento, de tipo atributo y de clase/comentario

simpre se debe crear un $scope aunque sea vacio
