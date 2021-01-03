<template>
    <div>
        <div class="row">
            <div class="col-12">
                <h4 
                class="text-white"
                :class="[saldo <= 0 ? 'bg-danger' : 'bg-success' ]">Tu saldo es: L.{{saldo}}</h4>
            </div>
        </div>
        <div class="row">
            <div class="col-4">
                <h3
                :class="[estadoCuenta = true ? 'bg-success text-white' : 'bg-danger']"
                > Estado: {{estadoCuenta ? 'Activa' : 'Cerrada'}}</h3> 
            </div>
        </div>
        <h3>Tipo de cuenta: {{cuenta}}</h3>
        <!-- Servicios -->
        <div class="row">
            <div class="col-3">
                <div class="bg-danger text-white" v-for=" (item, index) in servicios" :key="index"> {{index + 1}} - {{item}}</div>
            </div>
            <div class="col-6">

            </div>
        </div>
        <!-- Botones -->
        <AccionBotons   

            class="btn btn-success m-2"
            textoBtn="Agregar Saldo"
            @accion="agregarSaldo"
            :desactivar="desactivar"
        />
        <AccionBotons
            class="btn btn-danger"
            textoBtn="Disminuir Saldo"
            @accion="disminuirSaldo"
            :desactivar="desactivar"
        />
    </div>
    
    
    
</template>

<script>
import AccionBotons from './AccionBotons'


export default {
    components: { AccionBotons },
    name: 'Cuenta',
    props: {

    },
    data(){
        return {
            cuenta:'Visa - Débito',
            saldo: 1000,
            servicios: ['Cuenta de ahorro', 'Ahorro retirable', 'Giros', 'Depositos'],
            estadoCuenta: true
        }
    },
    methods:{
        agregarSaldo(){
            this.saldo = this.saldo + 100
            this.desactivar = false
        },
        disminuirSaldo(){
            if (this.saldo === 0 ) {
                this.desactivar = true
                alert('Sin saldo en cuenta')
                return // salimos de condicional sin usar else
            }
            this.saldo = this.saldo - 100
        }
    }
}
</script>

styl
