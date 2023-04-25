<script setup></script>

<template>
    <div class="container w-50 calc">
        <div class="container">
            <header class="p-5 mb-2 mt-5 bg-light rounded-3">
                <h1>VISOR</h1>
            </header>
        </div>
        <div class="container">
            <select name="operacao" id="operacao" class="m-2 text-center">
                <option value="standart">
                    - Selecione a operação desejada -
                </option>
                <option value="soma">+</option>
                <option value="menos">-</option>
                <option value="divide">/</option>
                <option value="multiplica">x</option>
            </select>
        </div>
        <div class="container text-center m-auto">
            <div class="row">
                <button type="button" class="btn btn-success col-4">CE</button>
                <button type="button" class="btn btn-outline-secondary col-4">
                    C
                </button>
                <button type="button" class="btn btn-outline-secondary col-4">
                    &larr;
                </button>
            </div>
            <div class="row">
                <button type="button" class="btn btn-outline-secondary col-4">
                    7
                </button>
                <button type="button" class="btn btn-outline-secondary col-4">
                    8
                </button>
                <button type="button" class="btn btn-outline-secondary col-4">
                    9
                </button>
            </div>
            <div class="row">
                <button type="button" class="btn btn-outline-secondary col-4">
                    4
                </button>
                <button type="button" class="btn btn-outline-secondary col-4">
                    5
                </button>
                <button type="button" class="btn btn-outline-secondary col-4">
                    6
                </button>
            </div>
            <div class="row">
                <button type="button" class="btn btn-outline-secondary col-4">
                    1
                </button>
                <button type="button" class="btn btn-outline-secondary col-4">
                    2
                </button>
                <button type="button" class="btn btn-outline-secondary col-4">
                    3
                </button>
            </div>
            <div class="row">
                <button type="button" class="btn btn-outline-secondary col-4">
                    ,
                </button>
                <button type="button" class="btn btn-outline-secondary col-4">
                    0
                </button>
                <button type="button" class="btn btn-danger col-4">=</button>
            </div>
        </div>
    </div>
</template>

<style scoped></style>
