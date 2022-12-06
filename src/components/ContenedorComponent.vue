<template>

    <div>

      <div class="row pt-3 ps-3 ">

        <div class="col-6 animate__animated animate__fadeIn">
          <TablasComponent
          :datos_tabla="usuarios" 
          :cabeceras="labelheader_usuarios"
          :props_tabla="propiedades_tabla_usuario"
          :titulo_tabla="titulo"
          :col="columnas"
          tipo="usuarios"
        />
        </div>

        <div class="col-6 animate__animated animate__fadeInDownBig">
          <TablasComponent
          :datos_tabla="heroes" 
          :cabeceras="labelheader_heroes"
          :props_tabla="propiedades_tabla_heroes"
          titulo_tabla="Personajes de Marvel"
          :col="columnas"
          tipo="heroes"
        />
        </div>
        
      </div>
      
      <div class="row pt-3 ps-3">

        <div class="col-6 animate__animated animate__fadeInUp">
  
          <TablasComponent
          :datos_tabla="autos" 
                        :cabeceras="labelheader_autos"
                        :props_tabla="propiedades_tabla_autos"
                        :col="columnas_autos"
                        tipo="autos"
                        :estilo_objeto="cabeceraauto"
          />
        </div>

      </div>
    </div>
    

</template>

<script>
import TablasComponent from '@/components/TablasComponent'
export default {
  name: "ContenedorComponent",
  components: {
    TablasComponent
  },
  data() {
    return {
       /* array de usuarios para la primera tabla */
       usuarios:[
            {
                avatar: require("../assets/img/avatar1.png"),
                nombre:"Ariel Bernardo",
                rol:"Administrador",
                estado: true
            },
            {
                avatar: require("../assets/img/avatar2.png"),
                nombre:"Noelia Gonzalez",
                rol:"Editor",
                estado: true
            },
            {
                avatar:require("../assets/img/avatar3.png"),
                nombre:"Laura Gomez",
                rol:"Usuario Comun",
                estado: false
            },
            {
                avatar:require("../assets/img/avatar4.png"),
                nombre:"Juan Gabriel Maquez",
                rol:"Usuario Comun",
                estado: false
            },
            {
                avatar:require("../assets/img/avatar5.png"),
                nombre:"Juan Gabriel Maquez",
                rol:"Usuario Comun",
                estado: true
            },
        ],
        /* propiedades tabla usuario */
        propiedades_tabla_usuario:{
            table_strip:'table-striped',
            table_hover:'table-hover',
            header_th:'table-info',
            table_fondo:'',//table-dark
            table_texto:'text-secondary',
            table_align:'text-center',
            header_bgcolor:'bg-danger',
            header_textcolor:'text-white',
            texttransform:'text-uppercase', //text-lowercase text-capitalize
            heder_textweight:'fw-bold'
        },
        /* label de cabecera de usuarios */
        labelheader_usuarios:['#','Avatar','Nombre','Rol','Estado'],
        /* titulo para la tabla */
        titulo:'Usuarios del Sistema',
        /* Cantidad de columnas para el titulo coldspan para usuario y personajes */
        columnas:5,
        /* array de heroes para la primera tabla */
        heroes:[
            {
                avatar:require("../assets/img/marvel1.jpg"),
                nombre:"Jennifer Walters",
                rol:"She-Hulk",
                estado: true
            },
            {
                avatar:require("../assets/img/marvel2.png"),
                nombre:"Steve Grant Rogers",
                rol:"Capitan America",
                estado: false
            },
            {
                avatar:require("../assets/img/avatar3.png"),
                nombre:"Tony Stark",
                rol:"Iron Man",
                estado: false
            }
        ],
        /* propiedades tabla usuario */
        propiedades_tabla_heroes:{
            table_strip:'table-striped',
            table_hover:'table-hover',
            header_th:'table-light',
            table_fondo:'table-dark',//table-dark
            table_texto:'text-white',
            table_align:'text-center',
            header_bgcolor:'bg-dark',
            header_textcolor:'text-white',
            texttransform:'text-capitalize', //text-lowercase text-capitalize
            heder_textweight:'fw-bold'
        },
         /* label de cabecera de heroes */
        labelheader_heroes:['cant','Avatar','Nombre','Personaje','Está vivo?'],
        /* array de Autos para la primera tabla */
        autos:[
            {
                avatar:require("../assets/img/auto1.png"),
                nombre:"Porche mod.2008",
                estado: false
            },
            {
                avatar:require("../assets/img/auto2.png"),
                nombre:"Chevrolet Camaro",
                estado: true
            },
            {
                avatar:require("../assets/img/auto3.png"),
                nombre:"PapaMovil",
                estado: true
            },
            {
                avatar:require("../assets/img/auto4.png"),
                nombre:"Auto Volador",
                estado: false
            }
        ],
        /* propiedades tabla autos */
        propiedades_tabla_autos:{
            table_strip:'table-striped',
            table_hover:'',
            header_th:'table-light',
            table_fondo:'table-success',//table-dark
            table_texto:'text-danger',
            table_align:'text-center',
            header_bgcolor:'bg-success',
            header_textcolor:'text-white',
            texttransform:'text-capitalize', //text-lowercase text-capitalize
            heder_textweight:'fw-bold'
        },
        /* label de cabecera de autos */
        labelheader_autos:[' - ','Foto','Auto','Puede Circular?'],
        /* Cantidad de columnas para el titulo coldspan */
        columnas_autos:4,
        /* color horrible  para la cabecera de auto */
        cabeceraauto:{
            color: '#FF0000',
            background:'#0000FF'
        }
    };
  },
  methods: {},
  created(){
    console.log(this.titulo)
    console.log("desde contenedor",this.usuarios)
  }
};
</script>

<style lang="scss" scoped></style>
