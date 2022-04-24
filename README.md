<h3 align="center">PHP e TDD: testes com PHPUnit</h3>

---

*Gerar o autoload*
```
composer dump
```

*ou*

```
composer dupmpautoload
```

---

**Quais as vantagens desta abordagem sobre testar manualmente a funcionalidade?** <br>
Evitar erros humanos e agilizar o processo de testes da aplicação. Testar manualmente é um processo suscetível a erros. Podemos simplesmente nos esquecer de realizar determinada ação, validar os dados de forma errada, etc. Além disso, testes manuais são demorados. Com testes automatizados, nós ganhamos muita velocidade e confiabilidade em nosso processo.

---

[Arrange-Act-Assert](http://wiki.c2.com/?ArrangeActAssert) <br>
[Given-When-Then](https://martinfowler.com/bliki/GivenWhenThen.html)

---

[PHPUnit](https://phpunit.de/) <br>
[Documentação PT-BR](https://phpunit.readthedocs.io/pt_BR/latest/)

*Instalação*
```
composer require --dev phpunit/phpunit ^6.4
```

*Verificar a versão*
```
vendor/bin/phpunit --version
```

---

**Qual o principal tipo de teste automatizado o PHPUnit nos ajuda a escrever?** <br>
Testes de unidade. O PHPUnit já vem com tudo que é necessário para realizar testes de unidade. Testes de unidade testam a menor unidade possível de um código. Um bom exemplo disso é um método. Ou seja, um teste de unidade deve testar o mínimo de código possível por vez. Isso ficará mais claro durante o andamento do treinamento.

---

*Rodando o PHPUnit*
```
vendor/bin/phpunit tests
```

*Métodos estáticos utilizar* ```::self```
```
self::assertEquals();
```

*Adicionando cores no retorno dos testes*
```
vendor/bin/phpunit --colors tests
```

---

**Como podemos/devemos escrever um teste com o PHPUnit?** <br>
Cada método de teste, dentro da classe de teste, deve ter seu nome começando com test.

Dentro de uma classe de teste, podemos ter vários métodos. Estes métodos serão executados separadamente pelo PHPUnit. Os métodos que devem ser executados pelo PHPUnit devem começar com test. Por exemplo: testGaranteQueDoisMaisDoisSaoQuatro. Nomes bem descritivos são interessantes e você entenderá melhor o motivo durante o treinamento. Uma alternativa a iniciar o método com test é utilizar a anotação @test.

Precisamos ter uma classe que herde de PHPUnit\Framework\TestCase e tenha seu nome terminando em Test.

Uma classe que contenha testes de unidade, além de herdar da classe padrão do PHPUnit, deve ter seu nome terminado em Test. É uma convenção que a classe de teste tenha o nome da classe que ela vai testar, além do sufixo Test. Por exemplo: classe a testar: Avaliador; classe de teste: AvaliadorTest.

---

[PHPUnit - Asserções](https://phpunit.readthedocs.io/en/8.5/assertions.html)

---

**Quais técnicas são comuns para identificar o que testar?** <br>
Análise de valores de fronteira. <br>
Utilizando esta técnica, além de identificar as classes de equivalência, testamos os valores exatamente na borda de cada uma delas.

Classes de equivalência. <br>
Podemos identificar classes de equivalência para entender quais dados deverão ser utilizados para montar os cenários de teste.

[Análise de valor limite e Particionamento de Equivalência](http://testwarequality.blogspot.com/p/tenicas-de-teste.html)

---

**O que devemos testar quando tivermos listas (ou arrays) de dados?** <br>
O número de itens na lista e todo o seu conteúdo, se possível. <br>
Além de verificar o tamanho da lista, precisamos verificar o seu conteúdo. Claro que em listas muito grandes, isso se torna muito difícil e verboso, mas sempre que possível, devemos garantir que o conteúdo é o esperado, de acordo com a regra que o código deve atender.

---