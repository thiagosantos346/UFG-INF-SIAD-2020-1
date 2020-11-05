# Armazém de dados - Arquiteturas

## Contexto

### O que é um Armazém de dados :

Um data warehouse é projetado especificamente para análises de dados, que envolvem a leitura de grandes quantidades de dados para compreender relações e tendências entre os dados. Um banco de dados é usado para capturar e armazenar dados, como o registro de detalhes de uma transação.

1. Repositório central de informações, com objetivo facilitar analise para a tomar decisões mais eficazes.
2. Os dados transmitidos de sistemas transacionais, bancos de dados relacionais e de outras fontes para, de tempos em tempos, muito embora pode ser aplicadas outras formas de indicadores de transmissão dos dados.
3. Analistas de negócios, engenheiros de dados, cientistas de dados e gestores acessam as informações por meio de ferramentas de inteligência de negócios (BI), clientes SQL e outros aplicativos de análise.
4. Analise de dados são indispensáveis para que as organizações(publicas ou privadas) continuem competitivas.
5. Relatórios, painéis e análises para extrair insights dos dados, monitorar a performance dos negócios e apoiar a tomada de decisões, são umas possíveis formas de usar as informações provenientes dos armazém de dados.
6. Os armazém de dados alimentam, e otimiza e controlam a entrada e saída de dados para garantir eficiência na obtenção das informações.

### O que motiva a criação de um armazém de dados

#### Preservando registros passados

A evolução humana está intimamente ligada a escrita, endo em vista que descrever o momento atual, de forma que possa ser revisado no futuro, nos permite não só diminuir caminhos para solução de problemas já conhecidos, mas também de ver padrões que já se repetiram no passado.

1. Análise de dados históricos.
2. Tomada de decisão adequada.

#### Avaliação dos dados para melhor entender e aprimorar as operações corporativas

Faz parte da natureza organizacional, fazer planejamentos a médio e longo prazo, mas nem sempre é possível fazer isso enquanto a corrida está acontecendo, parar a todo momento para replanejar e validar informações, pode ser algo desgastante por isso se faz sentido armazenar essas informações do curto prazo de forma paralela e assim obter uma nova visão sobre o que é produzido em termos de dados.

1. Dados consolidados de várias fontes.
2. Qualidade, consistência e precisão de dados.
3. Separação do processamento analítico dos bancos de dados transacionais, o que melhora o desempenho dos dois sistemas.

### Como é construido um um armazém de dados

### Unificado

1. Unifica e integra todos os dados análogos de diferentes bancos de dados de uma maneira coletivamente aceitável, usando a modelagem de dados
2. Ele incorpora dados de diversas fontes.
3. Deve manter nomenclatura, layout e codificação consistentes para facilitar a análise eficaz dos dados.

### Variação de tempo

1. Armazena dados coletados ao longo de um amplo horizonte de tempo.
2. Os dados coletados são identificados com duração de tempo específica, para analises históricas.
3. A entrada de novos dados é irreversível, eles não podem ser reestruturados ou alterados.

### Não volatilidade

1. Os dados anteriores não são removidos quando novos dados são carregados no armazém de dados.
2. Os dados são apenas para leitura apenas.
3. Os dados estão em constante atualização.

## As Camadas

Uma arquitetura de data warehouse define a organização dos dados e a estrutura de armazenamento. Como os dados devem ser organizados e limpos para serem valiosos, uma arquitetura de data warehouse moderna se concentra na identificação da técnica mais eficaz de extrair informações de dados brutos na área de preparação e convertê-los em uma estrutura consumível simples usando um modelo dimensional que entrega negócios valiosos inteligência.

Ao projetar o data warehouse de uma empresa, há três tipos principais de arquitetura a serem levados em consideração.

### Camada única


### Contexto histórico

### Características

1. Produção de um conjunto denso de dados
2. Redução do volume de dados depositados.

### Vantagens

 1. Eliminar redundâncias

### Desvantagens

1. Não é adequada para empresas com requisitos de dados complexos e numerosos fluxos de dados.

### Aplicações

## Duas Camadas

### Três Camadas

### Contexto histórico

### Características

### Vantagens

### Desvantagens

### Aplicações

## Três Camadas

### Contexto histórico

### Características

### Vantagens

### Desvantagens

### Aplicações

## Referências

1.  [www.astera.com/pt/type/blog/data-warehouse-architecture](www.astera.com/pt/type/blog/data-warehouse-architecture) Acesso em 03-11-2020 23:26
2.  [aws.amazon.com/pt/data-warehouse/](https://aws.amazon.com/pt/data-warehouse/) Acesso em 03-11-2020 23:26
3.  