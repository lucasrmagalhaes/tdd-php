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