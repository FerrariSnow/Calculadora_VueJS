<script setup>
import { reactive } from "vue";

const estado = reactive({
    primeiroValor: 0,
    segundoValor: 0,
    resultado: 0,
    operador: "+",
});

function alteraValor1(evento) {
    estado.primeiroValor = evento.target.value;
    calcula();
}

function alteraValor2(evento) {
    estado.segundoValor = evento.target.value;
    calcula();
}

function alteraOperador(evento) {
    estado.operador = evento.target.value;
    calcula();
}

function calcula() {
    switch (estado.operador) {
        case "+":
            estado.resultado =
                Number(estado.primeiroValor) + Number(estado.segundoValor);
            break;
        case "-":
            estado.resultado =
                Number(estado.primeiroValor) - Number(estado.segundoValor);
            break;
        case "*":
            estado.resultado =
                Number(estado.primeiroValor) * Number(estado.segundoValor);
            break;
        case "/":
            estado.resultado =
                Number(estado.primeiroValor) / Number(estado.segundoValor);
            break;
        default:
            break;
    }
}
</script>

<template>
    <h1 class="container text-center mt-5">Calculadora em VueJS</h1>
    <div class="container">
        <header class="p-5 mb-2 mt-5 bg-light rounded-3 row">
            <span class="h1 m-2 container col-3 text-center">
                {{ estado.primeiroValor }}
            </span>
            <span class="h1 m-2 container col-1 text-center">
                {{ estado.operador }}
            </span>
            <span class="h1 m-2 container col-3 text-center">
                {{ estado.segundoValor }}
            </span>
            <span class="h1 m-2 container col-1 text-center">=</span>
            <span class="h1 m-2 container col-3 text-center">
                {{ estado.resultado }}
            </span>
        </header>
        <p class="container text-center h4">
            Digite abaixo o primeiro valor, selecione a operação desejada e após
            digite o segundo valor:
        </p>
        <div class="container d-flex justify-content-center">
            <input
                type="number"
                @keyup="alteraValor1"
                class="m-1 text-center"
            />
            <select @change="alteraOperador" class="m-1 text-center">
                <option value="+">+</option>
                <option value="-">-</option>
                <option value="*">*</option>
                <option value="/">/</option>
            </select>
            <input
                type="number"
                @keyup="alteraValor2"
                class="m-1 text-center"
            />
        </div>
    </div>
</template>

<style scoped></style>
