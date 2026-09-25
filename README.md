[act-6-obj.js](https://github.com/user-attachments/files/32634182/act-6-obj.js)
//Datos y metodos de un obj
//Ficha de menu
//los datos son distintos a proposito. Compara la FORMA, no el contenido
const producto = {
    id: "p-07",
    nombre:"Agua de jamaica",
    precio: 15,
    categoria:"bebida",
    disponible:true,

    //Metodos
    resumen(){
        return this.nombre + " - $ " + this.precio + "(" + this.categoria + ")"
    },

    estaDisponible(){
        return this.disponible;
    }
};


console.log("paso 1 - imprimiendo el producto");
console.log(producto);

//paso 2 - tres formas de leer
console.log("-----PASO 2 -----");
const campo = "nombre";
console.log(producto.nombre);
console.log(producto["nombre"]);
console.log(producto[campo]);


console.log("-----PASO 3 -----");
console.log(producto.resumen());
console.log(producto.estaDisponible());

// ----- PASO 4 E1 usuario ----- 
const usuario = {
    id:"u-03",
    nombre:"juanito pistolas",
    correo:"juanto@cbtis258.edu.mx",
    telefono:8173589527,
    rol:"alumno"
};


// ----- PASO 5 -----
const pedido ={
    folio:"PR-0118",
    cliente: usuario,
    producto: producto,
    cantidad: 3,
    estado:"pendiente"
}



console.log("----- PASO 5 -----")
console.log(pedido.cliente.nombre);
console.log(pedido.producto.precio);
console.log(pedido.cliente.telefono);

// PASO 6 - Desestructuración
console.log("----- PASO 6 -----");
const{nombre, precio} = producto;
console.log(nombre, precio);

const{cantidad,nota = "sin nota"} = pedido;
console.log(cantidad, nota);
console.log(Axel daniel jimenez de león)




