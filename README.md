<h1 align="center">Desafio: Desenvolvedor Back-end</h1>

<p align="center">

<p align="center">
  <a href="#rocket-sobre-o-desafio">Sobre o desafio</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#calendar-entrega">Entrega</a>&nbsp;&nbsp;&nbsp;
</p>

# :rocket: Sobre o desafio
Para você já ir se aquecendo para o que está por vir, queremos propor um desafio para você.

Vamos supor uma aplicação que envia disparos de mensagens de SMS e registra esses disparos em um banco de dados. Queremos que você implemente um servidor que receberá atualizações de status dessas mensagens. A partir das regras de negócio definidas, você precisará construir uma API REST que realize a atualização das informações armazenadas em um banco de dados relacional e outra que busque os dados de mensagens no banco a partir do status da mensagem para exibir em um relatório.

**Atualização de status:** As mensagens de SMS são registradas no banco de dados e disparados por um sistema externo, que posteriormente envia uma requisição REST para atualizar o status da mensagem. Para isso, precisamos de uma API capaz de receber o ID do disparo e o status da mensagem e atualizar o registro no banco de dados.

**Relatórios de mensagens:** Para medir os resultados dos envios, temos uma aplicação que pesquisa os registros de disparo de acordo com o status da mensagem. Para que essa aplicação funcione corretamente, precisamos de uma rota receba um status e retorne todos os registros do banco de dados que foram marcados com esse status nas últimas 24 horas.

**Observações:** O desafio deve ser desenvolvido utilizando Javascript ou Typescript, sendo obrigatória a utilização de NodeJS.

## Regras de negócio
1. A atualização só pode ser realizada se a requisição para tal for válida. Para que uma requisição seja válida, o ID recebido deve ser puramente numérico e o status precisa ser válido (deve ser um dos seguintes: "ENVIADO", "RECEBIDO", "ERRO DE ENVIO").

2. Caso o registro a ser atualizado não seja encontrado no banco de dados o erro deve ser devidamente tratado e retornado na API.

3. A propriedade status estará inicialmente vazia.

## Dados
Para te ajudar a entender um pouco melhor, estamos disponibilizando um exemplo da entidade sms_messages, que possui as propriedades mínimas que a tabela do banco de dados deve conter. Sinta-se livre para adicionar mais propriedades caso julgue necessário.

<p align="center">
  <img  src="./assets/sms-database.png">
</p>

# :calendar: Entrega
Para entregar esse desafio, você deve criar um repositório no **GitHub** contendo a sua implementação junto com as informações necessárias para rodar o seu projeto.

Em seguida, basta enviar o link do repositório para o email **dev.gi@precato.com.br** com o assunto **"Desafio desenvolvedor back-end"**.

**Observações:** Não esqueça de deixar o repositório público para que possamos visualizar sua resolução. 😉
