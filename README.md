# Modelos e Documentações de Qualidade

## **Objetivos**

- O objetivo deste documento é preservar os procedimentos e estratégias que garantem a qualidade do produto do **[Nome do Produto]**.
- O time de **[Nome do Produto]** inteiro é responsável pela qualidade do **[Nome do Produto]** (App mobile).

## **Escopo de Testes**

O tipo de teste que atuamos atualmente para garantir a qualidade do produto são:

| **Tipo de Teste**        | **Responsável**               | **Aplicação**         |
| ------------------------ | ----------------------------- | --------------------- |
| Testes Unitários          | Desenvolvimento               | **[Nome do Produto]**  |
| Testes de Integração      | Qualidade / Desenvolvimento    | **[Nome do Produto]**  |
| Testes E2E               | Qualidade                     | **[Nome do Produto]**  |
| Testes Manuais            | Qualidade / Desenvolvimento    | **[Nome do Produto]**  |
| Testes de Performance     | Qualidade / Desenvolvimento    | **[Nome do Produto]**  |
| Teste de Regressão        | Qualidade / Desenvolvimento    | **[Nome do Produto]**  |

## **Ambiente de Testes**

- Utilizamos os ambientes dinâmicos (staging) para validações e testes do **CRM**.
    - Segue a [documentação para criação dos ambientes](#) para mais informações.

## **Ferramentas que Utilizamos**

Abaixo estão as ferramentas que podemos utilizar para testes e/ou garantir a qualidade do nosso produto:

| **Ferramenta**        | **Descrição**                                             | **Responsável**               |
| --------------------- | -------------------------------------------------------- | ----------------------------- |
| Navegador e Celular   | Execução dos testes para CRM e APP                        | Qualidade / Desenvolvimento    |
| Jira                  | Mapeamento/acompanhamento de bugs e métricas via dashboard | Qualidade / Desenvolvimento    |
| Confluence            | Mapeamento com todos os documentos do time                | Qualidade / Desenvolvimento    |
| Postman               | Testes via API                                            | Qualidade / Desenvolvimento    |
| TestFlight            | Liberação de versões para beta testing                    | Qualidade / Desenvolvimento    |
| VsCode                | Editor utilizado para desenvolvimento de automação de testes | Qualidade                   |
| Cypress               | Framework de testes utilizados para desenvolvimento de testes E2E automatizados | Qualidade                   |
| New Relic             | Monitoramento de request                                  | Qualidade / Desenvolvimento    |
| Elastic               | Análise de Log, Análise de Dados no CRM                   | Qualidade / Desenvolvimento    |

## **Técnicas de Teste**

Deve ser utilizado os templates abaixo conforme as necessidades da tarefa.

### **Templates de Testes**

#### **Template de Teste de Aceitação ou Funcional**
- **Objetivo**: Validar se novas funcionalidades atendem aos critérios de aceitação dos stakeholders.
- **Quando Utilizar**: Antes da entrega para garantir que o produto atende às expectativas.
- **Como Utilizar**: 
  - Defina cenários de teste com base nos critérios de aceitação.
  - Registre o resultado esperado e execute o teste.
  - Documente o resultado real e qualquer problema encontrado.

| **Cenário de Teste**      | **Descrição**                                                                 | **Resultado Esperado**                                          | **Resultado Real**      |
| ------------------------- | ----------------------------------------------------------------------------- | --------------------------------------------------------------- | ----------------------- |
| Cenário Positivo 1         | Implementar a funcionalidade de envio de email automático ao proprietário após mudança de status do imóvel. | O email deve ser enviado automaticamente quando o status é atualizado. | [Ex: Email enviado corretamente após atualização do status.] |
| Cenário Positivo 2         | Adicionar funcionalidade de exportação de lista de imóveis em Excel.          | A lista deve ser exportada em formato Excel sem erros.           | [Ex: Exportação realizada com sucesso] |
| Cenário Negativo 1         | Tentar enviar um email automático sem ter configurado um servidor de email.   | O sistema deve exibir uma mensagem de erro e o email não deve ser enviado. | [Resultado observado]    |
| Cenário Negativo 2         | Tentar exportar uma lista de imóveis quando não há imóveis cadastrados.       | O sistema deve exibir uma mensagem de erro e não gerar o arquivo Excel. | [Resultado observado]    |

#### **Template de Teste Exploratório**
- **Objetivo**: Identificar falhas inesperadas e oportunidades de melhoria.
- **Quando Utilizar**: Durante o desenvolvimento inicial ou após novas implementações.
- **Como Utilizar**: 
  - Defina cenários de teste com base em áreas não cobertas por testes automatizados.
  - Registre o resultado esperado e execute o teste.
  - Documente o resultado real e compare com o esperado.

| **Cenário de Teste**       | **Resultado Esperado**                                          | **Resultado Real**           |
| -------------------------- | -------------------------------------------------------------- | ---------------------------- |
| Adicionar novo imóvel       | O imóvel deve ser adicionado com sucesso e aparecer na lista.  | [Ex: Imóvel adicionado corretamente.] |
| Editar detalhes de imóvel   | As mudanças devem ser salvas e refletidas corretamente.        | [Ex: Detalhes editados com sucesso.] |

#### **Template de Teste de Compatibilidade**
- **Objetivo**: Garantir que o CRM funcione em diferentes navegadores, sistemas e dispositivos.
- **Quando Utilizar**: Antes de um lançamento ou atualizações em plataformas.
- **Como Utilizar**: 
  - Defina cenários de teste com combinações de plataformas.
  - Registre o resultado esperado e execute o teste.
  - Documente o resultado real e compare com o esperado.

| **Cenário de Teste**        | **Resultado Esperado**                                          | **Resultado Real**           |
| --------------------------- | -------------------------------------------------------------- | ---------------------------- |
| Acessar página no Safari     | A página deve ser carregada corretamente no Safari.            | [Ex: Página carregada corretamente.] |
| Usar CRM em tablet Android   | O imóvel deve ser adicionado sem problemas.                    | [Ex: Problemas de layout.]    |

#### **Template de Teste de Usabilidade**
- **Objetivo**: Avaliar a facilidade de uso e a experiência do usuário.
- **Quando Utilizar**: Durante a fase de design da interface ou após feedback de usuários.
- **Como Utilizar**: 
  - Defina cenários de teste com tarefas comuns.
  - Registre o resultado esperado e execute o teste.
  - Documente o resultado real e qualquer dificuldade encontrada.

| **Cenário de Teste**        | **Resultado Esperado**                                          | **Resultado Real**           |
| --------------------------- | -------------------------------------------------------------- | ---------------------------- |
| Editar contato de proprietário | O usuário deve conseguir acessar e editar as informações de contato em menos de 2 minutos. | [Ex: Usuário editou em 1 minuto.] |
| Filtrar imóveis por status   | Os imóveis devem ser filtrados corretamente.                   | [Ex: Filtros funcionaram corretamente.] |

#### **Template de Teste de Performance**
- **Objetivo**: Avaliar a capacidade do CRM sob cargas pesadas e identificar gargalos.
- **Quando Utilizar**: Antes de lançamentos importantes ou alterações que impactem a performance.
- **Como Utilizar**: 
  - Defina cenários simulando cargas pesadas.
  - Registre o resultado esperado e execute com ferramentas de desempenho.
  - Documente o resultado real e compare com o esperado.

| **Cenário de Teste**        | **Resultado Esperado**                                          | **Resultado Real**           |
| --------------------------- | -------------------------------------------------------------- | ---------------------------- |
| Simular 500 corretores       | O sistema deve responder em menos de 5 segundos.               | [Ex: Sistema demorou 7 segundos.] |
| Gerar relatório de imóveis   | O relatório deve ser gerado em menos de 10 segundos.           | [Ex: Relatório gerado em 8 segundos.] |

#### **Template de Teste de Regressão**
- **Objetivo**: Verificar se funcionalidades principais continuam funcionando após modificações.
- **Quando Utilizar**: Sempre que houver alterações que possam impactar funcionalidades existentes.
- **Como Utilizar**: 
  - Defina cenários de funcionalidades críticas.
  - Registre o resultado esperado e execute o teste.
  - Documente o resultado real e qualquer problema encontrado.

| **Cenário de Teste**        | **Resultado Esperado**                                          | **Resultado Real**           |
| --------------------------- | -------------------------------------------------------------- | ---------------------------- |
| Adicionar um lead            | O lead deve ser adicionado e vinculado corretamente.           | [Ex: Lead adicionado com sucesso.] |
| Atualizar status de imóvel   | O status deve ser atualizado corretamente.                     | [Ex: Status atualizado corretamente.] |

#### **Template de Teste de Integração**
- **Objetivo**: Verificar a integração entre diferentes módulos do CRM.
- **Quando Utilizar**: Quando novas funcionalidades envolvem interações entre diferentes partes do sistema.
- **Como Utilizar**: 
  - Defina cenários de interação entre módulos.
  - Registre o resultado esperado e execute o teste.
  - Documente o resultado real e qualquer problema encontrado.

| **Cenário de Teste**        | **Resultado Esperado**                                          | **Resultado Real**           |
| --------------------------- | -------------------------------------------------------------- | ---------------------------- |
| Atualizar status no dashboard| O dashboard deve refletir corretamente a mudança de status.    | [Ex: Dashboard atualizado corretamente.] |
| Sincronizar com contabilidade| Os dados devem ser transferidos corretamente.                  | [Ex: Sincronização realizada com sucesso.] |

