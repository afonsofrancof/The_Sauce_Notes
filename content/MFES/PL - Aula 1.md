🌫 18 Setembro 2023 -  #MFES

## Ficha 1

> [!note]
> As resoluções dos exercícios aqui contidos podem conter erros. Se detetares um problema (e se o souberes resolver) por favor contacta-nos.



> [!help]+ Ex 1 (Configuração de produtos)
> Certos produtos, como é o caso dos automóveis, são altamente personalizáveis, mas podem haver dependências entre as configurações. Os clientes podem não estar cientes de todas essas dependências, e poderão escolher opções de configuração inconsistentes.
> Como são muitas configurações e muitas dependências, podemos usar um SAT solver para verificar se o cliente escolhe opções de configuração consistentes. Para isso, podemos seguir os seguintes passos:
> 
> 1. Codificar as dependências entre configurações como uma formula proposicional $\psi$
> 2. Codificar as opções selecionadas pelo cliente como uma fórmula proposicional $\phi$.
> 3. Usar o SAT solver para verificar se $\psi \land \phi$ não é contraditório.
> 
> Considere agora a seguinte dependência entre as configurações disponíveis para a personalização de um automóvel:
> 
> *"O ar condicionado Thermotronic comfort requer uma bateria de alta capacidade, exceto quando combinado com motores a gasolina de 3,2 litros."*
> 
> Será que um cliente pode escolher o ar condicionado Thermotronic comfort, uma bateria de pequena capacidade e não escolher o motor de 3,2 litros? Como poderia responder a esta pergunta com a ajuda de um SAT solver?
> 
>  > [!tip]- Resolução
>  > Legenda de variáveis utilizadas:
>  > A - ar condicionado
>  > B - bateria alta capacidade
>  > C - motor 3,2 L
>  >
>  >$A \land \neg B \implies G \equiv \neg (A \land \neg B) \lor G \equiv \neg A \lor B \lor G$
>  >
>  >$(\neg A \lor B \lor G) \land A \land \neg B \land \neg G$       ----- SAT?
>  >
>  


> [!help]+ Ex 3 (Configuração de computadores)
> Uma loja de eletrónica permite aos seus clientes personalizar o seu computador, escolhendo entre dois modelos de motherboards e dois modelos de monitor. Cada computador tem que ter obrigatoriamente uma única motherboard, um único CPU, uma única placa gráfica e uma única memória RAM. O computador poderá ou não ter um monitor. A personalização do computador deverá obedecer às regras:
> 1. A motherboard MB1 quando combinada com a placa gráfica PG1, obriga à utilização da RAM1;
> 2. A placa gráfica PG1 precisa do CPU1, exceto quando combinada com a memória RAM2;
> 3.  O CPU2 só pode estar instalado na motherboard MB2;
> 4.  O monitor MON1 para poder funcionar precisa da placa gráfca PG1 e da memória RAM2.
>
>Codifique este problema em lógica proposicional. Assinale claramente o que denota cada variável proposicional que introduzir e escreva um conjunto de fórmulas proposicionais adequado à sua modelação.
>   
>  > [!hint]- Resolução
>  > Legenda de variáveis utilizadas:
>  > $CPU_1; CPU_2; RAM_1; RAM_2; MB_1; MB_2; PG_1; PG_2; MON_1; MON_2$
>  > 
>  > Problema modelado:
>  > 1. $CPU_1 \lor CPU_2$
>  > 2. $CPU_1 \implies \neg CPU_2$
>  > 3. $RAM_1 \lor RAM_2$
>  > 4. $RAM_1 \implies \neg RAM_2$
>  > 5. $MB_1 \lor MB_2$
>  > 6. $MB_1 \implies \neg MB_2$
>  > 7. $PG_1 \lor PG_2$
>  > 8. $PG_1 \implies \neg PG_2$
>  >    
>  > 9. $MB_1 \land PG_1 \implies RAM_1$
>  > 10. $PG_1 \implies CPU_1 \lor RAM_2 \equiv PG_1 \land \neg RAM_2 \implies CPU_1$
>  > 11. $CPU_2 \implies MB_2$
>  > 12. $MON_1 \implies PG_1 \land RAM_2$
>  
>  Indique, apenas por palavras, como poderia usar um SAT solver para testar as consistências deste conjunto de regras.
>  
>  Indique, apenas por palavras, como usaria um SAT solver para se pronuncias quanto à velocidade das seguintes afirmações:
>  (a) O monitor MON1 só poderá ser usado com uma motherboard MB1.
> > [!hint]- Resolução
> > ??? $T \models MON_1 \implies MB_1$
> > $T, \neg (MON_1 \implies MB_1) UNSAT$
> > > [!info] $T \models F$ sse  $T, \neg F UNSAT$
> 
> (b) Um cliente pode personalizar o seu computador da seguinte forma: uma motherboard MB2, o CPU1, a placa gráfica PG2 e a memória RAM1.
> >[!hint]- Resolução
> >$T, MB_2 \land CPU_1 \land PG_2 \land RAM_1$  ---- SAT?

> [!help]+ Ex 2 (Distribuição de Gabinetes)
> Considere que temos 3 gabinetes e  queremos distribuir 4 pessoas (Ana=1, Nuno=2, Pedro=3 e Maria=4) por esses gabinetes.  Para codificar este problema em lógica proposicional, , vamos ter um conjunto de variáveis proposicionais $x_{p,g}$ com a seguinte semântica:
> $x_{p,g}$ é verdade sse a pessoa $p$ ocupa o gabinete $g$, com $p=1..4$ e $g=1..3$
> 
> Considere que forem estipuladas as seguintes regras de ocupação de gabinetes:
> 1. Cada pessoa ocupa um único gabinete.
> 2. O Nuno e o Pedro não podem partilhar gabinete.
> 3. Se a Ana ficar sozinha num gabinete, então o Pedro também terá que ficar sozinho num gabinete.
> 4. Cada gabinete só pode acomodar, no máximo, 2 pessoas.
>    
> Escreve um conjunto de fórumlas proposicionais adequado à modelação destas regras.
> 
> >[!tip]- Resolução
> >
> >**Cada pessoa ocupa só um único gabinete.**
> > 1. para cada pessoa p = 1..4
> > 2. pelo menos um gabinete:    $x_{p1} \lor x_{p2} \lor x_{p3}$
> > 3. no máximo 1 gabinete:   $x_{p1} \implies \neg x_{p2} \land x_{p3} \equiv x_{p1} \implies \neg (x_{p2} \lor x_{p3} ) \equiv x_{p2} \implies \neg x_{p3}$
> > 4. 
