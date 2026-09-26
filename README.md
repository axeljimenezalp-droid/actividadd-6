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


//----- PASO 7 TOTAL -----
const total = producto.precio * pedido.cantidad;
pedido.total = total;

console.log("-----PASO 7-----")
console.log(pedido)


//----- PASO 8 COPIAR -----
console.log("-----PASO 8-----")
const copiaMala = producto;
copiaMala.precio = 999;
console.log(producto.precio);
//Va imprimir 999: copiaMala y producto apuntan al MISMO objeto
// la variable no guarda el objeto, guarda donde esta

producto.precio = 15;  // lo dejamos como estaba

const copiaBuena = {...producto};
copiaBuena.precio = 1000;
console.log(producto.precio); // 15 el original quedo intacto


// ----- PASO 9 -----
console.log("-----PASO 9-----")

const respuestaOk = {
    ok: true,
    data:pedido
};

const respuestaError = {
    ok: false,
    error: {
        mensaje:"elproducto no esta disponible",
        detalle:[]
    }
};


console.log(respuestaOk);
console.log(respuestaError);




