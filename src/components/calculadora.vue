<template>
    <div class="calculadora">
        <input v-model.numero="numero1" type="number" placeholder="Número 1" @input="calcular">
        <select v-model="operacao" @change="calcular">
            <option value="+">+</option>
            <option value="-">-</option>
            <option value="*">*</option>
            <option value="/">/</option>
        </select>
        <input v-model.numero="numero2" type="number" placeholder="Número 2" @input="calcular">
        <div class="resultado">Resultado: {{ Resultado }}</div>
    </div>
</template>
  
<script>
  export default {
    data() {
        return {
            numero1: 0,
            numero2: 0,
            operacao: '+',
            Resultado: 0
        };
    },
    methods: {
      calcular() {
        switch (this.operacao) {
            case '+':
                this.Resultado = this.numero1 + this.numero2;
                break;
            case '-':
                this.Resultado = this.numero1 - this.numero2;
                break;
            case '*':
                this.Resultado = this.numero1 * this.numero2;
                break;
            case '/':
                this.Resultado = this.numero1 / this.numero2;
                break;
            default:
                this.Resultado = 0;
        }
      }
    }
  };
</script>
<style scoped>
    .calculadora {
        display: flex;
        flex-direction: column;
        align-items: center;
        margin-top: 50px;
    }
    
    input[type="number"], select {
        margin-bottom: 10px;
    }
    
    .resultado {
        margin-top: 10px;
        font-weight: bold;
    }
</style>  