# CT_RF06_Gestao_SifitBox.md

## Cenário 06: Gestão de Aulas Coletivas, Turmas e Modalidades SifitBox.

### Caso de Teste 01: Gerar aulas automaticamente a partir da grade semanal.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C06-CT01 | Validar a criação automática da agenda de aulas com base na parametrização prévia. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| Existirem turmas e horários configurados no módulo SifitBox.  |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos no menu "SifitBox"                            |
| **QUANDO** clicarmos no botão "Gerar Aulas"                        |
| **ENTÃO** o sistema deve criar as sessões de aula na grade de acordo com os dias e horários definidos |
| **E** as aulas geradas devem ser exibidas na listagem com limite de vagas disponível |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| A agenda deve ser preenchida com as aulas geradas sem conflitos de horários. |

---

### Caso de Teste 02: Cadastrar nova Categoria de CrossFit.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C06-CT02 | Inclusão de uma nova categoria de treino (ex: Endurance, Gymnastic). |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O utilizador deve ter permissão para gerir o módulo SifitBox.  |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que navegamos para a ecrã de "Categorias CrossFit"        |
| **E** clicamos no botão de adição de nova categoria                |
| **E** preenchemos o nome da categoria                              |
| **QUANDO** confirmarmos o salvamento                               |  
| **ENTÃO** a nova categoria deve ser exibida na lista               |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| A categoria deve ser persitida na base de dados e disponibilizada para associação nas aulas. |

---

### Caso de Teste 03: Filtrar aulas por período de datas.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C06-CT03 | Validar a consulta de aulas agendadas filtrando pelo intervalo de datas. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| Existirem aulas geradas na agenda em diferentes datas.       |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos no menu "SifitBox"                            |
| **E** informamos a data inicial e final no filtro de busca         |
| **QUANDO** clicarmos no botão "Buscar"                             |
| **ENTÃO** a grade de aulas deve ser atualizada listando apenas os horários compreendidos no período selecionado |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| Apenas as aulas pertencentes ao intervalo informado devem ser apresentadas. | 