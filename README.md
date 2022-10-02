# NgTest1

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 11.0.1.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.

## ------------------------------------- Anotations ---------------------------------------------

# Curso: Alura - Angular: testes automatizados com Jasmine e Karma.

---

# Aula 2. Lapidando nossos testes:

- new Set(): permite iterar dados dentro de looping através do .add(). Caso o valor de id gerado seja igual a outro valor já interado, este valor não será adicionado ao Set. Através do comparativo entre variavelSet.zie e o length definido no looping, podemos então garantir se os ids gerados são de fato únicos.
  \*\* [Referência](https://github.com/DeniseLuiz/testes-de-unidade-karma-jasmine/blob/master/src/app/shared/services/unique-id/unique-id.service.spec.ts): linha 28.

- .withContext: permite que, considerando que estejamos testando valores de um array, ao falhar o teste seja indicado em qual contexto (dentro de n possibilidades do array), o teste lançou a exceção.
  \*\*[Referência](https://github.com/DeniseLuiz/testes-de-unidade-karma-jasmine/blob/master/src/app/shared/services/unique-id/unique-id.service.spec.ts): linha 49.

- Diferença entre toBeTrue, toBe(true) e toBeTruthy

<p>toBeTrue: só considera tipos primitivos, ou seja só funciona com:

```
expect(true).toBeTrue();
```

- toBe: aceita tipos não primitivos e considera não somente o tipo, mas se também <strong>se o valor está anexado na mesma referência de memória dentro do programa</strong>. No caso:

```
expect(new Boolean (true)).toBe(new Boolean(true));
```

falharia, pois as variáveis não apontam para a mesma referência de memória.

- toBeTruthy: tipo de comparação mais genérica de todas, verifica somente se o valor é verdadeiro, sendo assim falharia nos tipos null, undefined e ''.</p>
