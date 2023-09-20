20 Setembro 2023 - #RAS

> [!note]
> As resoluções dos exercícios aqui contidos podem conter erros. Se detetares um problema (e se o souberes resolver) por favor contacta-nos.


>[!help]+ Ex. 1
>Defina se os seguintes requisitos são funcionais ou não funcionais:
>1. Ter a possibilidade de exportar o ficheiro a que se refere a Portaria n. 321-A/2007, de 26 de março;
>2. Possuir um sistema que permita identificar a gravação do registo de faturas ou documentos equivalentes e talões de venda, através de um algoritmo de cifra assimétrica e de uma chave privada de conhecimento exclusivo do produtor do programa;
>3. Possuir um controlo de acesso ao sistema informática, obrigando a uma autenticação de cada utilizador;
>4. Não dispor de qualquer função que, no local, ou remotamente, permita alterar, direta ou indiretamente, a informação de natureza fiscal, sem gerar evidência agregada à informação geral.
>   
>   >[!hint]- Resolução
>   >1. requisito funcional: define uma feature do sistema
>   >2. *secção inicial* -> requisito funcional: garantir a integridade dos dados; *secção da encriptação simétrica* -> requisito não funcional : é um requisito tecnológico
>   >3. requisito funcional: defina uma feature do sistema; requisito não funcional :  é um requisito de segurança
>   >4. não requisito: não define uma feature (é uma "não-feature") e não se qualifica a requisito não-funcional


>[!help]+ Ex 3.1 (Naveda and Seidman, 2006, pp. 39–40)
> Which is the type of elements less appropriate to be included in a requirements document?
>1. design restrictions
>2. product delievery constraints
>3. funcionalities to make available
>4. performance characteristics
>   
>>[!hint]- Resolução
>>Option 2 is the less appropriate.
>>
>>- Option 1 contains non-requirements but has to do with the development of the software, thus it's important to be included in the requirement phase.
>>- Option 2 has nothing to do with the development at all and contains restrictive directives.
>>- Option 3. is a functional requirement.
>>- Option 4. is a non-functional requirement.


>[!help]+ Ex. 3.2 (Naveda and Seidman, 2006, pp. 33–34)
>Which is the type of requirements that should not be included in a requirements document?
>
>1. functional requirements
>2. maintenance requirements
>3. project requirements
>4. performance requirements
>   
>>[!hint]- Resolução
>>Option 3. should not be included.
>>
>>- Option 1. is essential.
>>- Option 2. pertains to the directives that will define how the system will be maintained and managed in the future.
>>- Option 3. defines the circumstances around the project: it touches budget, the team members, other departments (than the development team), etc. It is too encompassing and it is not always about the development of the system. *The requirements document should be in the project documents*, not the other way around.
>>- Option 4. is a non-functional requirement, therefore  its inclusion is necessary.


>[!help]+ Ex. 3.3 (Naveda and Seidman, 2006, pp. 41–42)
>Which is the element that must be included in a requirements document?
>
>1. acceptance/validation procedures
>2. delivery plans
>3. quality attributes
>4. activities to guarantee the quality
>   
>>[!hint]- Resolução
>>Option 3. is a must.
>>
>>1. Option 1. pertains to the testing procedures.
>>2. Option 2. pertains to the expected plans of the delivery of the software (aka versions: version alpha, version beta,...).
>>3. Option 3. is a synonym for non-functional requirements.
>>4. Option 4. means the indicated protocol which regulates the quality of the product.


>[!help]+ Ex. 3.4 (Naveda and Seidman, 2006, pp. 57–58)
>Which of the following arguments is the most solid/strong to justify the specification of the non-functional requirements of a system?
>
>1. The non-functional requirements should only be considered in development contexts subject to tight restrictions (resources, budget, or deadlines).
>2. The non-functional requirements are only external characteristics of the system and can be obtained later.
>3. If a functionality is present in the system, the non-functional requirements determine how usable and useful it is.
>4. The non-functional requirements take less time to specify than the functional requirements.
>   
>>[!hint]- Resolução
>>Option 3. is the best justification.
>>
>>Non-functional requirements are, colloquially, an enumeration of restrictions to the functional requirements being defined by a developing system.
>>Non-functional requirements are the buffer of quality of the product - these cannot be defined later. Their determination may take even more time than the definition of functional requirements since, sometimes, they can be even more implicit than their counterpart. Their determination should also be independent of resources or budgets; otherwise, there can/will be consequences on the quality of the software.


>[!help]+ Ex. 3.5
>Consider the following requirement: *The system should be easy to use for trained persons.* 
>
>Classify this requirement with respect to its type. 
>1. Functional
>2. Non-functional
>
>Is this requirement verifiable? Justify.
>   
>>[!hint]- Resolução
>>Option 2., since it defines no feature.
>>
>>In terms of verifiability:
>>What is a trained person? That is debatable. Is it a person with 1h of experience, 3h, 5h? This needs to be defined. Also, what is easy? Is it defined by the number of errors this person commits (commit less than 3 errors in this determined feature - this is considered "easy")? Use correctly 80% of the software and it's "easy" and intuitive for the tester? This also needs defining.
>

