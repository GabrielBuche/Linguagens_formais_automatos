# Atividade 1 LFA

1) Verifique  quais as linguagens  geradas a partir das seguintes gramaticas:
*a) G = ( {S, B}, {a, b, c}, { S -> aSc | bBc | ε, B -> bBc | bc }, { S })*

Produções:
S → a S c | b B c | ε
B → b B c | b c

*Resposta:*
S => aSc => aεc
S => aSc => aaScc => aaεcc
S => aSc => abBcc => abbcc 
....

*{ L(G) =  { w e T* | w = a^n, b^m, c^m+n | onde h, m pertence aos Naturais ^ m != 1 }}*

essa gramatica me gera uma palavra que pode ser vazia onde o quantidade de 'a' e 'b' somadas, é igual a quantidade de 'c'
contanto que a quantidade de 'b' seja direferente de 1


*b) G = ( { S, B }, {a}, {S-> aS1, S1 -> aS2, S2 -> aS3, S3 -> aS | a }, { S })*

*Produções*
S  -> aS1
S1 -> aS2
S2 -> aS3
S3 -> aS | a

*Resposta:* Essa gramatica me gera uma cadeia de 'a' onde nao pode ser vazio e sua quantidade precisa ser multiplo de 4.
 
 *{ L(G) =  { w e T* | w = a^n, b^m, c^m+n | onde h, m pertence aos Naturais ^ m != 1 }}*

exemplo:
S => aS1  => aaS2 => aaaS3 => aaaa
S => aS1  => aaS2 => aaaS3 => aaaaS => aaaaaS1 => aaaaaas2 => aaaaaaaS3 => aaaaaaaS => aaaaaaaa



c) G = ( { S, A, B, C}, { a, b, c }
{
    S -> ABCS | ε,
    AB -> BA
    BC -> CB,
    AC -> CA,
    CB -> BC,
    BA -> AB,
    A -> A,
    B -> b,
    C -> c,
},
{ S } )

*Resposta:* essa gramatica me gera palavras sobre alfabeto 'a, b, c' , onde a quantidade de 'a, b, c' sao iguais 
e iguais
obs: sempre vai ser de ordem 3n (ex: abcbca, bac...)

*L(G)= { w ∈{a,b,c}* | a quantidade de a, b e c em w é igual}.*

S => ABCS => abcS  = abc 
S => ABCS => ACBS => acbS => acb
S => ABCS => BACS => bacS => bac
S => ABCS => BACS => bacS => bacABCS => bacabcS => bacabc 
...


2) Deminstre se a palavra *aabba* pertence as duas gramaticas a seguir:

*a) G1 = ( { S, T }, { a,b }, { S -> aTa | bTb, T -> aT | bT | ε}, { S } )*

*Produçõe*
S -> ata | bTb
T -> aT | bT | ε

*Resposta:*  S => aTa => aaTa => aabTa => aabbTa => aabba
Portanto a palavra "aabba" pertence a gramatica


*b) G2 = ( { S, A, B }, { a, b }, { S -> aA | bB, A -> aA | bA | a, B -> aB | bB | b }, { S })*

*Produçõe*
S -> aA | bB
A -> aA | bA | a
B -> aB | bB | b

*Resposta:* S => aA => aaA => aabA => aabbA => aabba,
portanto a palvra pertence a gramatica

3) Desenvolva uma gramatica que gere numero naturais nao permitindo numero que comecem com zero.

*Resposta:*
G = {S, D, R}, { n = { 1, 2, 3, 4, 5, 6, 7, 8, 9 }}, { S -> 0 | D, D -> nR, R -> 0R | nR | ε }, { S }

S -> 0 | D 
D -> nR 
R -> 0R | nR  | ε
