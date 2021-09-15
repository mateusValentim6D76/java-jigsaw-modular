# MODELO DE PROJETO JIGSAW

### Exemplo de modularização de um projeto Java a partir da versão 9.


Atualmente, os modificadores de acesso Java desempenham muito bem seu papel no encapsulamento das classes. Porém, isso ocorre somente quando as classes envolvidas estão no mesmo pacote. Se uma classe precisa ser acessada por outra classe localizada em um pacote diferente, ela precisa necessariamente ser pública. Além de reduzir a segurança, essa limitação contribui em muito para o JAR Hell. A ideia no Projeto Jigsaw é que os módulos sirvam como uma camada adicional de abstração, acima do nível de package, permitindo que se declare quais são os pacotes que serão exportados para módulos que dependam do módulo que está sendo desenvolvido. Com isso, os pacotes que não estiverem declarados como exportados ficarão visíveis somente por classes que estejam dentro do mesmo módulo. Quando analisamos esse objetivo mais detalhadamente, fica claro que ganhamos além de segurança, desempenho, já que o escopo para a busca de classes no tempo de execução será reduzido somente às classes que são exportadas.

