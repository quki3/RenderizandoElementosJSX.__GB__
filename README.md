

Renderizando Elementos
Los elementos son los bloques más pequeños de las aplicaciones de React. Un elemento
describe lo que quieres ver en la pantalla:

{/*PRIMERO??*/
{/*const element = <h1>Hello,word</h1>;*/} (mira el index.HTML en el espacio 17 mira tambien desde el browser mira los componentes y comprueva que estan vacios esa es la diferencia entre elementos y componentes)

A diferencia de los elementos del DOM de los navegadores, los elementos de React son objetos planos, y su creación es de bajo costo. React DOM se encarga de actualizar el DOM para igualar los elementos de React; NO confunda elementos con componentes;

Renderizando un elemento en el DOM
Digamos que hay un <div> en alguna parte de tu archivo HTML:

<div id="root"></div>
Lo llamamos un nodo “raíz” porque todo lo que esté dentro de él será manejado por React DOM.

Las aplicaciones construidas solamente con React usualmente tienen un único nodo raíz en el DOM. Dado el caso que estés integrando React en una aplicación existente, puedes tener tantos nodos raíz del DOM aislados como quieras.

Para renderizar un elemento de React en un nodo raíz del DOM, pasa ambos a 
ReactDOM.render():
{/*const element = <h1>Hello, world</h1>;ReactDOM.render(element, document.getElementById('rood'))*/}

si fuiste observador te diste cuenta que lo envolvi en un div esto es para que podamos agregar tantos elementos como quisieramos a nuestro UI(interfas de usuario)

Actualizando el elemento renderizado
Los elementos de React son inmutables. Una vez creas un elemento, no puedes cambiar sus hijos o atributos. Un elemento es como un fotograma solitario en una película: este representa la interfaz de usuario en cierto punto en el tiempo.

Con nuestro conocimiento hasta este punto, la única manera de actualizar la interfaz de usuario es creando un nuevo elemento, y pasarlo a ReactDOM.render().

Considera este ejemplo de un reloj en marcha:
{/*SEGUNDO??*/}
function tick() { 
  const element = (
    <div>
      <h1>Hello, world!</h1>
      <h2>It is {new Date().toLocaleTimeString()}.</h2>
    </div>
  );
  ReactDOM.render(element, document.getElementById('root'));
}

setInterval(tick, 1000);

!!!exelente terminaste!!!
