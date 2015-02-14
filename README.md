# SciJava Expression Parser (SJEP)

The SciJava Expression Parser is an infix-to-postfix (or infix-to-syntax-tree)
expression parser for mathematical expressions written in Java. It handles
(customizable) operators, functions, variables and constants in a similar way
to what the Java language itself supports.

## Rationale

Expression parsers are as old as the hills; what makes this one different?

* __No dependencies.__
* __Permissive BSD-2 license.__
* __[Available on Maven Central](http://search.maven.org/#search%7Cga%7C1%7Cg%3A%22org.scijava%22%20AND%20a%3A%22scijava-expression-parser%22).__
* __Separation of concerns.__ SJEP is a _parser_, not an _evaluator_. Once you
  have the postfix queue and/or syntax tree, what you do with it is your
  business (though there is a [toy evaluator in
  `src/test`](src/test/java/org/scijava/sjep/Evaluator.java), just for fun).
  In general, there is no assumption that your variables will consist of any
  particular data type, numerical or otherwise.
* __Clean, well-commented codebase with unit tests.__ 'Nuff said!

## License

The license is [BSD-2](http://imagej.net/BSD). See [LICENSE.txt](LICENSE.txt).

## History

The [ImageJ OPS](https://github.com/imagej/imagej-ops) project needed an
expression parser so that it could be more awesome. But not one limited to
primitive doubles, or one that conflated parsing with evaluation, or one
licensed in a restrictive way. Just a simple infix parser: a nice shunting yard
implementation, or maybe some lovely recursive descent. Something on GitHub,
with no dependencies, available on Maven Central. But surprisingly, there was
only tumbleweed. So SJEP was born, and all our problems are now over!
