 [Calculator project](Programing and language complier)


Report

1. Grammar for the calculator

Rule 0     S' -> statement
Rule 1     statement -> expr
Rule 2     expr -> NUMBER
Rule 3     expr -> LPAREN expr RPAREN
Rule 4     expr -> expr TIMES expr  [precedence=left, level=1]
Rule 5     expr -> expr PLUS expr  [precedence=left, level=2]


2. Type of the parser:

since the type of parser that we use in this case is bottom up parser.We have made the use of LR(0) parser with LR(0) items in this case. This can be noticed from the parsing states and states that is projected out in the "parser.out" file. 

3. Method of Translation and Integration of Parser and Translation:

step-1: Lexer Tokenization Process:

The initial step involves tokenization, where the lexer (named MyLexer) segments the input arithmetic expression into discrete tokens. Each token symbolizes a unique component of the expression, including numbers, operators, and parentheses.

step-2: Parsing Phase:

Following tokenization, the parser (termed MyParser) interprets these tokens according to the established grammar rules. It builds either a parse tree or an abstract syntax tree (AST), adhering to the grammar's structural specifications.

step-3: Evaluation During Parsing:

As the parser works through the input expression, it concurrently evaluates the expression. This assessment is woven into the parsing stage, leveraging the grammar rules for calculation.

step-4: Managing Operator Precedence and Associativity:

To correctly interpret expressions, the parser assigns precedence levels to operators through the precedence attribute. This organization guarantees that the parser accurately evaluates expressions in alignment with conventional arithmetic operation rules.

step-5: Result Compilation:

Upon concluding the parsing, the parser compiles a result from the evaluated expression. This outcome reflects the calculation specified in the input expression. Additionally, it produces postfix and prefix expressions, derived from the calculator_logic.py file.

step-5: Seamless Parser and Translator Integration:

The fusion of parser and translation is smoothly facilitated within the defined parsing rules in the parser class. These rules do more than just parse the input; they also translate (evaluate) the expression into a coherent result.

step-7: Output Delivery:

The evaluation's final result is then displayed, offering the user the calculated outcome of the arithmetic expression, including postfix and prefix expressions.







