---
layout: page
title: Introdução
nav_order: 1
---

# Aula 1 - Introdução

{: .no_toc .mb-2 }

Apresentando o curso.
{: .fs-6 .fw-300 }

{: .no_toc .text-delta }
Resultados Esperados

1. Entender um pouco de onde veio a ciência de dados
1. Receber as tarefas de configuração do ambiente
1. Ficar motivado!


```python
#In: 
# Imports
import babypandas as bpd
import numpy as np

import plotly.express as px
import matplotlib.pyplot as plt
plt.style.use('ggplot')
```

## Fundamentos de Ciência de Dados - 2024.1

### Bem-vindo ao curso de Ciência de Dados (UFMG)! 👋
- Hoje terermos uma visita guiada à ciência de dados.
- Nosso curso foi desenvolvido pela UC Berkeley em 2015 (data8.org).
- Em 2017 criamos a matéria de Introdução à Ciência de Dados (DCC212).
  - Vocês vão ver essa matéria
  - Porém o data8 era muito simples para o quarto período
- Voltamos com a ideia de ter o data8 no primeiro período no curso de Ciência de Dados
- Nos baseamos na abordagem de sucesso da UCSD (data10.com)
  - Também adaptada de Berkeley
- **Objetivo:** Aprenda programação e estatísticas suficientes para fazer ciência de dados.
  - Estatísticas sem muita matemática, principalmente simulação.
  - Estabelece as bases para todos os outros cursos do curso.

### Agenda

- Pessoal do curso.
- O que é ciência de dados?
- Como será esse curso?
- Demonstração com base na literatura.

## Equipe do curso

### Professor: Flavio Vinicius Diniz de Figueiredo (DCC)
- BSc em Ciência da Computação pela UFCG
- Mestrado e Doutorado em Ciência da Computação pela UFMG
  - Estudos parciais na Carnegie Mellon University e University of Brittish Columbia
- Já ensinou mais de 20 turmas de Introdução à Ciência de Dados (4o Período)
- Membro da comissão que fundou o curso
  - Em particula
### Professor: Uriel Moreira Silva (DEST)
- BS em Matemática e Ciência da Computação pela Loyola Maryland, PhD em Matemática (combinatória) pela UCSD 🔱.
- Ensino na UCSD: Matemática ➡️ CSE ➡️ DSC.
- 9ª vez ensinando DSC 10!
- Também ensine o DSC 40A com frequência.
- Interesses externos: artesanato, jogos de tabuleiro, caminhadas, panificação 🎂.

### TAs, Tutores e Mascote

Além disso, temos vários outros membros da equipe do curso que estão aqui para apoiá-lo nas discussões, no horário comercial e online.

- **2 Garaduate Tas**: Dayan Stockard e Dasha Varkus.
- **17 professores de graduação**: Gabriel Cha, Eric Chen, Charlie Gillet, Vanessa Hu, Dylan Lee, Anthony Li, Jasmine Lo, Linda Long, Aishani Mohapatra, Harshita Saha, Abel Seyoum, Selim Shaalan, Yutian (Skylar) Shi , Tony Ta, Zairan Xiang, Diego Zavalza e Luran (Lauren) Zhang,
- **1 mascote panda de pelúcia**: Bebê Panda. 🐼

Saiba mais sobre eles em [dsc10.com/staff](https://dsc10.com/staff).

## O que é “ciência de dados”? 🤔

<center><img src='images/what-is-ds.png' width=1250>Todo mundo parece ter sua própria definição de ciência de dados.</center>

### O que é "ciência de dados"?

A ciência de dados trata de **tirar conclusões úteis a partir de dados usando computação**. Ao longo do trimestre, abordaremos vários aspectos da ciência de dados:

- Primeiras 4 semanas: use Python para **explorar** dados.
- Muita visualização 📈📊 e “manipulação de dados”, utilizando ferramentas padrão da indústria.

- Próximas 4 semanas: use dados para **inferir** sobre uma população, dada apenas uma amostra.
- Confie fortemente na simulação, em vez de fórmulas.

- Últimas duas semanas: use dados do passado para **prever** o que pode acontecer no futuro.
- Um gostinho de aprendizado de máquina 🤖.

### A ciência de dados é mais relevante do que nunca 🤧

Passamos os últimos três anos analisando gráficos como este:

<center><img src='images/covid.jpg' width=75%></center>

### Também pode ser divertido!

<center><img src='images/rapper_vocab.jpg' width=75%></center>

Do artigo de [The Pudding](https://pudding.cool/) em [The Pudding](https://pudding.cool/).

## Logística do curso

### Site do curso

O site do curso é o seu balcão único para todas as coisas relacionadas ao curso.

<center><h3><a href="https://dsc10.com">dsc10.com</a></h3></center>

É aqui que serão postadas palestras, trabalhos de casa, laboratórios, discussões e todos os outros conteúdos. Verifique com frequência e **leia o [syllabus](https://dsc10.com/syllabus)**!

### Como configurar

- **EdStem**: fórum de perguntas e respostas. Todos os anúncios serão feitos aqui. Você deveria ter recebido um convite por e-mail; caso contrário, há um link no plano de estudos.
- **Gradescope**: onde você enviará todas as tarefas para avaliação automática e onde ficarão todas as suas notas. Você deveria ter sido adicionado automaticamente; entre em contato conosco se não.
- **DataHub**: Onde você acessará e executará todo o código desta classe. Acesse em [datahub.ucsd.edu](https://datahub.ucsd.edu). Mais na quarta-feira.
- **Não** usaremos o Canvas para nada!

Além disso, você também deve preencher um [Beginning of Quarter Survey](https://forms.gle/EpXSJitSUFtBiNgN9).

### Palestra

- As palestras serão presenciais e gravadas para visualização posterior.
- Poderá assistir a qualquer uma das 3 turmas teóricas, desde que haja vaga para os alunos oficialmente inscritos nessa turma.
- A participação nunca será exigida, mas é incentivada através de **crédito extra**.
- As gravações podem ser encontradas em [podcast.ucsd.edu](https://podcast.ucsd.edu).
- Os slides/código da aula serão vinculados ao site do curso, tanto em formato de código "executável" quanto em arquivo HTML (✏️), que você pode salvar como PDF e anotar em seu tablet.
- Tentaremos tornar as palestras envolventes. **Traga seu laptop ou tablet**, se tiver.

### Verificação de conceito ✅ – Resposta em [cc.dsc10.com](http://cc.dsc10.com)

**Quantos dos seguintes alimentos se qualificam como sanduíche?**

<center><img src='images/foods.png' width=30%></center>

UMA.0
B. 1
C. 2
D.3
E. 4             

_(Sempre usaremos o mesmo link para verificações de conceito, então você deve marcá-lo._)



### Discussão

- As seções de discussão foram elaboradas para que você pratique as **ideias conceituais** do curso.
- Todos os trabalhos desta aula serão feitos no computador através de código, mas os exames são em papel e presenciais.
- Para cada discussão, preparamos um conjunto de problemas, **composto de problemas de exames antigos** (ver [practice.dsc10.com](https://practice.dsc10.com)).
- Os conjuntos de problemas são publicados online, portanto traga um computador ou tablet para acessá-los. Mas, assim como nos exames, você responderá aos problemas **no papel**.
- Os conjuntos de problemas para discussão não são enviados a lugar nenhum.
- A participação não é obrigatória, porém **crédito extra** é fornecido pela participação.
- Se você comparecer, deverá comparecer à seção de discussão à qual foi designado.
- Assim como as palestras, as discussões serão podcastadas.

### Cronograma de Discussão

Cada aluno é designado para uma discussão específica da seguinte maneira. Você pode solicitar uma alteração de horário em [Beginning of Quarter Survey](https://forms.gle/EpXSJitSUFtBiNgN9). <span style="color:red"><b>🚨 Ignore a discussão e o tempo de laboratório listados na programação do seu curso.</b></span>

<center><img src='images/discussion.jpg' width=90%></center>

### Laboratórios

- Os laboratórios referem-se a **tarefas de laboratório**, que são uma parte obrigatória do curso e ajudam você a desenvolver fluência em Python e no trabalho com dados.
- Ao trabalhar nos laboratórios, você poderá executar **testes de autoavaliação** que informam se suas respostas estão corretas.
- Para laboratórios, se você passar em todos os testes do autonivelador, obterá 100\%!
- Você deve enviar laboratórios individualmente, mas pode discutir ideias com outras pessoas (sem compartilhamento de código).
- Os laboratórios geralmente acontecem aos **sábados às 23h59** no Gradescope. O primeiro laboratório (previsto para sábado, 14 de janeiro) terá instruções de envio.

### Trabalhos de casa e projetos

- As tarefas semanais de lição de casa baseiam-se nas habilidades que você desenvolve nos laboratórios.
- Uma diferença fundamental entre trabalhos de casa e laboratórios é que **passar nos testes de autoavaliação não garante uma pontuação perfeita!**
- Nos trabalhos de casa, temos “testes ocultos” que só são executados após o envio do trabalho.
- Os testes que lhe são disponibilizados no próprio trabalho apenas verificam se a sua resposta é razoável/no caminho certo.
- Novamente, você mesmo deve fazer as tarefas de casa, mas pode discutir ideias com outros alunos (sem compartilhar código).
- Os trabalhos de casa geralmente são entregues às **terças-feiras às 23h59** e enviados ao Gradescope.
- No **Projeto Intermediário** e no **Projeto Final**, você se aprofundará em um conjunto de dados! Os projetos são mais longos do que os trabalhos de casa, por isso damos-lhe mais tempo para trabalhar neles.
- Projetos deste trimestre: Restaurantes 🍔 e Great British Bake Off Great British Bake Off 👩‍🍳🍰.
- Você pode trabalhar em projetos com parceiros, seguindo estes [project partner guidelines](https://dsc10.com/project-partners). Vocês dois devem contribuir ativamente em **todas as partes** do projeto.

### Exames

Teremos dois exames neste trimestre.
- **Exame de meio de semestre**: sexta-feira, 10 de fevereiro, no horário agendado da aula.
- **Exame Final**: Sábado, 18 de março, das 15h às 18h.
- Ambos os exames serão realizados presencialmente e em papel. Deixe-nos saber se você tiver um conflito no [Beginning of Quarter Survey](https://forms.gle/EpXSJitSUFtBiNgN9).

### Leituras e recursos

- Faremos leituras de duas fontes. As leituras de cada palestra serão publicadas na página inicial do curso.
- [Computational and Inferential Thinking (CIT)](https://inferencialthinking.com), o livro criado para a versão deste curso em Berkeley.
- [`babypandas` notes](https://notes.dsc10.com), escrito especificamente para a primeira parte do DSC 10.
- A guia [Resources](https://dsc10.com/resources) do site do curso contém links para recursos úteis que você deseja usar ao longo do curso (por exemplo, folha de referência do DSC 10, tutoriais de programação, vídeos complementares).
- A guia [Debugging](https://dsc10.com/debugging) do site do curso contém respostas para muitos problemas técnicos comuns.

### Uma semana típica no DSC 10

| Domingo | Segunda-feira | Terça-feira | Quarta-feira | Quinta-feira | Sexta-feira | Sábado |
|: -- :|: -- :|: -- :|: -- :|: -- :|: -- :|: -- :|
| Nada! 😎 | Palestra | | Palestra | | Palestra | |
| | | | Discussão | | | |
| | | **HW devido** | | | | **Laboratório previsto** |

Consulte [Syllabus](https://dsc10.com/syllabus) para obter mais detalhes.

### Primeira tarefa
- O laboratório 0 será entregue **Sábado, 14 de janeiro às 23h59**.
- Será lançado ainda hoje
- <span style='color:red'><b>🚨 Importante: comece cedo e envie com frequência</b>.</span>

### Conseguindo ajuda
Este é um curso difícil e rápido, mas estamos aqui para ajudá-lo – veja como:

- **Horário de expediente (OH)**.
- Remoto e presencial durante toda a semana.
- Veja a programação e o link do Zoom no [Calendar 📆](https://dsc10.com/calendar).
- **EdStem**.
- Poste aqui qualquer dúvida logística ou conceitual (não envie por e-mail).
- Nenhum código ou soluções em postagens públicas. Essas postagens devem ser privadas para instrutores + funcionários.
- Caso contrário, poste publicamente (anonimamente, se desejar).
- <span style="color:red;"><b>🚨 Importante: use isso a seu favor!</b></span>

### Oportunidade: bootcamp Python

Diversity in Data Science, uma organização estudantil, está realizando um bootcamp Python de uma semana especificamente **para alunos do DSC 10 sem experiência anterior em programação**. O bootcamp é **esta semana**. Inscreva-se [here](https://docs.google.com/forms/d/e/1FAIpQLSdlRXdN6hzlC8IWGA8iuABDseRFkX22m2nATTQRJvkg_DTyPg/viewform).


<center><img src='images/bootcamp.png' width=40%></center>

### Conselhos de alunos anteriores

Ao final de cada trimestre, solicitamos aos alunos do DSC 10 que dêem conselhos aos futuros alunos do curso. Aqui estão algumas respostas:

> "Vá para o horário de expediente! Arranje um parceiro para o projeto mesmo que não queira. Se você não entende algum assunto tente o seguinte: vá para o horário de expediente, pergunte no [EdStem], confira as [leituras] , veja as notas da aula. Comece as tarefas mais cedo, tente terminar 2 dias antes para verificar seu trabalho.

> "Eu aconselharia que participasse das discussões e do horário de expediente sempre que possível, pois muitas vezes me descobri aprendendo coisas novas mesmo quando não vinha com uma pergunta pronta."

> "NÃO fique para trás nas palestras. Torna-se muito difícil acompanhar os conceitos. Vá para a seção de discussão! Ouvir um conceito explicado uma vez pode ser difícil de entender, então a seção de discussão foi extremamente útil."

> "Vá para o horário de expediente! É muito importante dar voz à voz. Converse com o professor após as aulas, compareça ao horário de expediente, poste suas dúvidas e faça uma pergunta."

### Colaboração

#### Fazer perguntas é altamente recomendável!
- Discuta todas as questões entre si (exceto exames).
- Envie tarefas de laboratório individualmente, mas você pode trabalhar com outras pessoas (sem compartilhamento de código).
- Envie trabalhos de casa individualmente, mas você pode discutir estratégias de resolução de problemas com outras pessoas (sem compartilhamento de código).
- Apresentar projetos individualmente ou em pares utilizando programação em pares.

#### Os limites da colaboração:
- Não compartilhem soluções entre si nem olhem o código de alguém.
- Os parceiros do projecto devem contribuir para todas as partes do projecto. Não divida o projeto.
- Violações de integridade acadêmica geralmente resultam em reprovação no curso.

### Estamos aqui para ajudá-lo!

Independentemente da sua formação, você pode ter sucesso neste curso. **Nenhuma experiência anterior em programação ou estatística será assumida!**

Assista no YouTube: [We’re All Data Scientists | Rebecca Nugent | TEDxCMU](https://www.youtube.com/watch?v=YMnqPTLoj7o).

### Recursos do campus

Serviços de Aconselhamento e Psicologia (CAPS) é uma unidade do campus que oferece “aconselhamento de curto prazo para questões acadêmicas, profissionais e pessoais e também oferece serviços de psiquiatria para circunstâncias em que a medicação pode ajudar no aconselhamento”.
Se você ou alguém que você conhece precisar de cuidados de saúde mental, entre em contato com o CAPS.

<center><h3><a href="https://caps.ucsd.edu/">caps.ucsd.edu</a></h3></center>

## Demonstração

### _Pequenas Mulheres_ (1868)

- _Little Women_, de Louisa May Alcott, é um romance que acompanha a vida de quatro irmãs – Meg, Jo, Beth e Amy.
- Utilizando as ferramentas desta aula, aprenderemos (um pouco) sobre o enredo do livro, sem precisar lê-lo.
- Não se preocupe com nada deste código – cobriremos as peças necessárias nas próximas semanas. Sente-se e relaxe!


```python
#In: 
# Read in 'lw.txt' to a variable called "little_women_text"
little_women_text = open('data/lw.txt').read()
```


```python
#In: 
# See the first three thousand characters
little_women_text[:3000]
```




    'The Project Gutenberg EBook of Little Women, by Louisa May Alcott\n\nThis eBook is for the use of anyone anywhere at no cost and with\nalmost no restrictions whatsoever.  You may copy it, give it away or\nre-use it under the terms of the Project Gutenberg License included\nwith this eBook or online at www.gutenberg.net\n\n\nTitle: Little Women\n\nAuthor: Louisa May Alcott\n\nPosting Date: September 13, 2008 [EBook #514]\nRelease Date: May, 1996\n[This file last updated on August 19, 2010]\n\nLanguage: English\n\n\n*** START OF THIS PROJECT GUTENBERG EBOOK LITTLE WOMEN ***\n\n\n\n\nLITTLE WOMEN\n\n\nby\n\nLouisa May Alcott\n\n\n\n\nCONTENTS\n\n\nPART 1\n\n          ONE  PLAYING PILGRIMS\n          TWO  A MERRY CHRISTMAS\n        THREE  THE LAURENCE BOY\n         FOUR  BURDENS\n         FIVE  BEING NEIGHBORLY\n          SIX  BETH FINDS THE PALACE BEAUTIFUL\n        SEVEN  AMY\'S VALLEY OF HUMILIATION\n        EIGHT  JO MEETS APOLLYON\n         NINE  MEG GOES TO VANITY FAIR\n          TEN  THE P.C. AND P.O.\n       ELEVEN  EXPERIMENTS\n       TWELVE  CAMP LAURENCE\n     THIRTEEN  CASTLES IN THE AIR\n     FOURTEEN  SECRETS\n      FIFTEEN  A TELEGRAM\n      SIXTEEN  LETTERS\n    SEVENTEEN  LITTLE FAITHFUL\n     EIGHTEEN  DARK DAYS\n     NINETEEN  AMY\'S WILL\n       TWENTY  CONFIDENTIAL\n   TWENTY-ONE  LAURIE MAKES MISCHIEF, AND JO MAKES PEACE\n   TWENTY-TWO  PLEASANT MEADOWS\n TWENTY-THREE  AUNT MARCH SETTLES THE QUESTION\n\n\nPART 2\n\n  TWENTY-FOUR  GOSSIP\n  TWENTY-FIVE  THE FIRST WEDDING\n   TWENTY-SIX  ARTISTIC ATTEMPTS\n TWENTY-SEVEN  LITERARY LESSONS\n TWENTY-EIGHT  DOMESTIC EXPERIENCES\n  TWENTY-NINE  CALLS\n       THIRTY  CONSEQUENCES\n   THIRTY-ONE  OUR FOREIGN CORRESPONDENT\n   THIRTY-TWO  TENDER TROUBLES\n THIRTY-THREE  JO\'S JOURNAL\n  THIRTY-FOUR  FRIEND\n  THIRTY-FIVE  HEARTACHE\n   THIRTY-SIX  BETH\'S SECRET\n THIRTY-SEVEN  NEW IMPRESSIONS\n THIRTY-EIGHT  ON THE SHELF\n  THIRTY-NINE  LAZY LAURENCE\n        FORTY  THE VALLEY OF THE SHADOW\n    FORTY-ONE  LEARNING TO FORGET\n    FORTY-TWO  ALL ALONE\n  FORTY-THREE  SURPRISES\n   FORTY-FOUR  MY LORD AND LADY\n   FORTY-FIVE  DAISY AND DEMI\n    FORTY-SIX  UNDER THE UMBRELLA\n  FORTY-SEVEN  HARVEST TIME\n\n\n\nCHAPTER ONE\n\nPLAYING PILGRIMS\n\n"Christmas won\'t be Christmas without any presents," grumbled Jo, lying\non the rug.\n\n"It\'s so dreadful to be poor!" sighed Meg, looking down at her old\ndress.\n\n"I don\'t think it\'s fair for some girls to have plenty of pretty\nthings, and other girls nothing at all," added little Amy, with an\ninjured sniff.\n\n"We\'ve got Father and Mother, and each other," said Beth contentedly\nfrom her corner.\n\nThe four young faces on which the firelight shone brightened at the\ncheerful words, but darkened again as Jo said sadly, "We haven\'t got\nFather, and shall not have him for a long time." She didn\'t say\n"perhaps never," but each silently added it, thinking of Father far\naway, where the fighting was.\n\nNobody spoke for a minute; then Meg said in an altered tone, "You know\nthe reason Mother proposed not having any presents this Christmas was\nbecause it is going to b'




```python
#In: 
# Print the first three thousand characters
print(little_women_text[:3000])
```

    The Project Gutenberg EBook of Little Women, by Louisa May Alcott
    
    This eBook is for the use of anyone anywhere at no cost and with
    almost no restrictions whatsoever.  You may copy it, give it away or
    re-use it under the terms of the Project Gutenberg License included
    with this eBook or online at www.gutenberg.net
    
    
    Title: Little Women
    
    Author: Louisa May Alcott
    
    Posting Date: September 13, 2008 [EBook #514]
    Release Date: May, 1996
    [This file last updated on August 19, 2010]
    
    Language: English
    
    
    *** START OF THIS PROJECT GUTENBERG EBOOK LITTLE WOMEN ***
    
    
    
    
    LITTLE WOMEN
    
    
    by
    
    Louisa May Alcott
    
    
    
    
    CONTENTS
    
    
    PART 1
    
              ONE  PLAYING PILGRIMS
              TWO  A MERRY CHRISTMAS
            THREE  THE LAURENCE BOY
             FOUR  BURDENS
             FIVE  BEING NEIGHBORLY
              SIX  BETH FINDS THE PALACE BEAUTIFUL
            SEVEN  AMY'S VALLEY OF HUMILIATION
            EIGHT  JO MEETS APOLLYON
             NINE  MEG GOES TO VANITY FAIR
              TEN  THE P.C. AND P.O.
           ELEVEN  EXPERIMENTS
           TWELVE  CAMP LAURENCE
         THIRTEEN  CASTLES IN THE AIR
         FOURTEEN  SECRETS
          FIFTEEN  A TELEGRAM
          SIXTEEN  LETTERS
        SEVENTEEN  LITTLE FAITHFUL
         EIGHTEEN  DARK DAYS
         NINETEEN  AMY'S WILL
           TWENTY  CONFIDENTIAL
       TWENTY-ONE  LAURIE MAKES MISCHIEF, AND JO MAKES PEACE
       TWENTY-TWO  PLEASANT MEADOWS
     TWENTY-THREE  AUNT MARCH SETTLES THE QUESTION
    
    
    PART 2
    
      TWENTY-FOUR  GOSSIP
      TWENTY-FIVE  THE FIRST WEDDING
       TWENTY-SIX  ARTISTIC ATTEMPTS
     TWENTY-SEVEN  LITERARY LESSONS
     TWENTY-EIGHT  DOMESTIC EXPERIENCES
      TWENTY-NINE  CALLS
           THIRTY  CONSEQUENCES
       THIRTY-ONE  OUR FOREIGN CORRESPONDENT
       THIRTY-TWO  TENDER TROUBLES
     THIRTY-THREE  JO'S JOURNAL
      THIRTY-FOUR  FRIEND
      THIRTY-FIVE  HEARTACHE
       THIRTY-SIX  BETH'S SECRET
     THIRTY-SEVEN  NEW IMPRESSIONS
     THIRTY-EIGHT  ON THE SHELF
      THIRTY-NINE  LAZY LAURENCE
            FORTY  THE VALLEY OF THE SHADOW
        FORTY-ONE  LEARNING TO FORGET
        FORTY-TWO  ALL ALONE
      FORTY-THREE  SURPRISES
       FORTY-FOUR  MY LORD AND LADY
       FORTY-FIVE  DAISY AND DEMI
        FORTY-SIX  UNDER THE UMBRELLA
      FORTY-SEVEN  HARVEST TIME
    
    
    
    CHAPTER ONE
    
    PLAYING PILGRIMS
    
    "Christmas won't be Christmas without any presents," grumbled Jo, lying
    on the rug.
    
    "It's so dreadful to be poor!" sighed Meg, looking down at her old
    dress.
    
    "I don't think it's fair for some girls to have plenty of pretty
    things, and other girls nothing at all," added little Amy, with an
    injured sniff.
    
    "We've got Father and Mother, and each other," said Beth contentedly
    from her corner.
    
    The four young faces on which the firelight shone brightened at the
    cheerful words, but darkened again as Jo said sadly, "We haven't got
    Father, and shall not have him for a long time." She didn't say
    "perhaps never," but each silently added it, thinking of Father far
    away, where the fighting was.
    
    Nobody spoke for a minute; then Meg said in an altered tone, "You know
    the reason Mother proposed not having any presents this Christmas was
    because it is going to b



```python
#In: 
# Create a variable "chapters" by splitting the text on 'CHAPTER '
chapters = little_women_text.split('CHAPTER ') 

# Create a DataFrame with one column -- the chapters
bpd.DataFrame().assign(chapters=chapters)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>chapters</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>The Project Gutenberg EBook of Little Women, b...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>ONE\n\nPLAYING PILGRIMS\n\n"Christmas won't be...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>TWO\n\nA MERRY CHRISTMAS\n\nJo was the first t...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>THREE\n\nTHE LAURENCE BOY\n\n"Jo!  Jo!  Where ...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>FOUR\n\nBURDENS\n\n"Oh, dear, how hard it does...</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
    </tr>
    <tr>
      <th>43</th>
      <td>FORTY-THREE\n\nSURPRISES\n\nJo was alone in th...</td>
    </tr>
    <tr>
      <th>44</th>
      <td>FORTY-FOUR\n\nMY LORD AND LADY\n\n"Please, Mad...</td>
    </tr>
    <tr>
      <th>45</th>
      <td>FORTY-FIVE\n\nDAISY AND DEMI\n\nI cannot feel ...</td>
    </tr>
    <tr>
      <th>46</th>
      <td>FORTY-SIX\n\nUNDER THE UMBRELLA\n\nWhile Lauri...</td>
    </tr>
    <tr>
      <th>47</th>
      <td>FORTY-SEVEN\n\nHARVEST TIME\n\nFor a year Jo a...</td>
    </tr>
  </tbody>
</table>
<p>48 rows × 1 columns</p>
</div>




```python
#In: 
# Counts of names in the chapters of Little Women

counts = bpd.DataFrame().assign(
    Amy=np.char.count(chapters, 'Amy'),
    Beth=np.char.count(chapters, 'Beth'),
    Jo=np.char.count(chapters, 'Jo'),
    Meg=np.char.count(chapters, 'Meg'),
    Laurie=np.char.count(chapters, 'Laurie'),
)
counts
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Amy</th>
      <th>Beth</th>
      <th>Jo</th>
      <th>Meg</th>
      <th>Laurie</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>23</td>
      <td>26</td>
      <td>44</td>
      <td>26</td>
      <td>0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>13</td>
      <td>12</td>
      <td>21</td>
      <td>20</td>
      <td>0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2</td>
      <td>2</td>
      <td>62</td>
      <td>36</td>
      <td>16</td>
    </tr>
    <tr>
      <th>4</th>
      <td>14</td>
      <td>18</td>
      <td>34</td>
      <td>17</td>
      <td>0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>43</th>
      <td>31</td>
      <td>8</td>
      <td>61</td>
      <td>3</td>
      <td>29</td>
    </tr>
    <tr>
      <th>44</th>
      <td>13</td>
      <td>0</td>
      <td>9</td>
      <td>0</td>
      <td>10</td>
    </tr>
    <tr>
      <th>45</th>
      <td>1</td>
      <td>2</td>
      <td>6</td>
      <td>2</td>
      <td>0</td>
    </tr>
    <tr>
      <th>46</th>
      <td>2</td>
      <td>1</td>
      <td>56</td>
      <td>4</td>
      <td>2</td>
    </tr>
    <tr>
      <th>47</th>
      <td>10</td>
      <td>3</td>
      <td>37</td>
      <td>6</td>
      <td>13</td>
    </tr>
  </tbody>
</table>
<p>48 rows × 5 columns</p>
</div>




```python
#In: 
# Cumulative number of times each name appears

cumulative_counts = bpd.DataFrame().assign(
    Amy=np.cumsum(counts.get('Amy')),
    Beth=np.cumsum(counts.get('Beth')),
    Jo=np.cumsum(counts.get('Jo')),
    Meg=np.cumsum(counts.get('Meg')),
    Laurie=np.cumsum(counts.get('Laurie')),
    Chapter=np.arange(1, 49, 1)
)

cumulative_counts.plot(x='Chapter', figsize=(10, 5))

plt.title('Cumulative Number of Times Each Name Appears', y=1.08);
```


    
![png](01-Introducao_files/01-Introducao_43_0.png)
    



```python
#In: 
# Interactive version of the previous plot

cumulative_counts_df = cumulative_counts.drop(columns=['Chapter']).to_df().melt().rename(columns={'variable': 'name', 'value': 'count'})
cumulative_counts_df = cumulative_counts_df.assign(chapter = list(range(1, 49)) * 5)
px.line(cumulative_counts_df, x='chapter', y='count', color='name', width=900, height=600, title='Cumulative Number of Times Each Name Appears')
```


        <script type="text/javascript">
        window.PlotlyConfig = {MathJaxConfig: 'local'};
        if (window.MathJax && window.MathJax.Hub && window.MathJax.Hub.Config) {window.MathJax.Hub.Config({SVG: {font: "STIX-Web"}});}
        if (typeof require !== 'undefined') {
        require.undef("plotly");
        define('plotly', function(require, exports, module) {
            /**
* plotly.js v2.29.1
* Copyright 2012-2024, Plotly, Inc.
* All rights reserved.
* Licensed under the MIT license
*/
/*! For license information please see plotly.min.js.LICENSE.txt */
        });
        require(['plotly'], function(Plotly) {
            window._Plotly = Plotly;
        });
        }
        </script>




<div>                            <div id="113da3fa-69be-4a1b-be85-ff4eec7aa311" class="plotly-graph-div" style="height:600px; width:900px;"></div>            <script type="text/javascript">                require(["plotly"], function(Plotly) {                    window.PLOTLYENV=window.PLOTLYENV || {};                                    if (document.getElementById("113da3fa-69be-4a1b-be85-ff4eec7aa311")) {                    Plotly.newPlot(                        "113da3fa-69be-4a1b-be85-ff4eec7aa311",                        [{"hovertemplate":"name=Amy\u003cbr\u003echapter=%{x}\u003cbr\u003ecount=%{y}\u003cextra\u003e\u003c\u002fextra\u003e","legendgroup":"Amy","line":{"color":"#636efa","dash":"solid"},"marker":{"symbol":"circle"},"mode":"lines","name":"Amy","orientation":"v","showlegend":true,"x":[1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36,37,38,39,40,41,42,43,44,45,46,47,48],"xaxis":"x","y":[0,23,36,38,52,58,64,91,139,142,147,164,175,183,189,197,204,223,226,256,265,267,276,283,298,305,342,345,348,394,451,456,463,468,468,468,471,502,502,547,548,581,588,619,632,633,635,645],"yaxis":"y","type":"scatter"},{"hovertemplate":"name=Beth\u003cbr\u003echapter=%{x}\u003cbr\u003ecount=%{y}\u003cextra\u003e\u003c\u002fextra\u003e","legendgroup":"Beth","line":{"color":"#EF553B","dash":"solid"},"marker":{"symbol":"circle"},"mode":"lines","name":"Beth","orientation":"v","showlegend":true,"x":[1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36,37,38,39,40,41,42,43,44,45,46,47,48],"xaxis":"x","y":[0,26,38,40,58,72,100,105,114,119,124,144,164,177,182,194,203,232,262,269,276,277,292,298,307,313,318,322,322,323,328,331,364,370,372,375,412,413,413,414,435,442,451,459,459,461,462,465],"yaxis":"y","type":"scatter"},{"hovertemplate":"name=Jo\u003cbr\u003echapter=%{x}\u003cbr\u003ecount=%{y}\u003cextra\u003e\u003c\u002fextra\u003e","legendgroup":"Jo","line":{"color":"#00cc96","dash":"solid"},"marker":{"symbol":"circle"},"mode":"lines","name":"Jo","orientation":"v","showlegend":true,"x":[1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36,37,38,39,40,41,42,43,44,45,46,47,48],"xaxis":"x","y":[0,44,65,127,161,216,229,238,309,330,342,384,444,468,516,542,555,584,619,624,653,720,737,788,824,836,853,881,950,999,1038,1045,1105,1107,1162,1204,1239,1244,1291,1306,1321,1338,1374,1435,1444,1450,1506,1543],"yaxis":"y","type":"scatter"},{"hovertemplate":"name=Meg\u003cbr\u003echapter=%{x}\u003cbr\u003ecount=%{y}\u003cextra\u003e\u003c\u002fextra\u003e","legendgroup":"Meg","line":{"color":"#ab63fa","dash":"solid"},"marker":{"symbol":"circle"},"mode":"lines","name":"Meg","orientation":"v","showlegend":true,"x":[1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36,37,38,39,40,41,42,43,44,45,46,47,48],"xaxis":"x","y":[0,26,46,82,99,112,117,122,138,209,213,237,278,299,320,338,353,374,388,389,414,445,454,510,539,554,559,561,613,615,615,616,619,620,620,622,625,625,665,666,667,667,670,673,673,675,679,685],"yaxis":"y","type":"scatter"},{"hovertemplate":"name=Laurie\u003cbr\u003echapter=%{x}\u003cbr\u003ecount=%{y}\u003cextra\u003e\u003c\u002fextra\u003e","legendgroup":"Laurie","line":{"color":"#FFA15A","dash":"solid"},"marker":{"symbol":"circle"},"mode":"lines","name":"Laurie","orientation":"v","showlegend":true,"x":[1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36,37,38,39,40,41,42,43,44,45,46,47,48],"xaxis":"x","y":[0,0,0,16,16,51,60,67,84,108,112,123,154,181,202,210,219,231,253,269,274,300,308,319,339,350,355,355,366,369,381,384,405,406,408,442,445,471,471,504,504,538,542,571,581,581,583,596],"yaxis":"y","type":"scatter"}],                        {"template":{"data":{"histogram2dcontour":[{"type":"histogram2dcontour","colorbar":{"outlinewidth":0,"ticks":""},"colorscale":[[0.0,"#0d0887"],[0.1111111111111111,"#46039f"],[0.2222222222222222,"#7201a8"],[0.3333333333333333,"#9c179e"],[0.4444444444444444,"#bd3786"],[0.5555555555555556,"#d8576b"],[0.6666666666666666,"#ed7953"],[0.7777777777777778,"#fb9f3a"],[0.8888888888888888,"#fdca26"],[1.0,"#f0f921"]]}],"choropleth":[{"type":"choropleth","colorbar":{"outlinewidth":0,"ticks":""}}],"histogram2d":[{"type":"histogram2d","colorbar":{"outlinewidth":0,"ticks":""},"colorscale":[[0.0,"#0d0887"],[0.1111111111111111,"#46039f"],[0.2222222222222222,"#7201a8"],[0.3333333333333333,"#9c179e"],[0.4444444444444444,"#bd3786"],[0.5555555555555556,"#d8576b"],[0.6666666666666666,"#ed7953"],[0.7777777777777778,"#fb9f3a"],[0.8888888888888888,"#fdca26"],[1.0,"#f0f921"]]}],"heatmap":[{"type":"heatmap","colorbar":{"outlinewidth":0,"ticks":""},"colorscale":[[0.0,"#0d0887"],[0.1111111111111111,"#46039f"],[0.2222222222222222,"#7201a8"],[0.3333333333333333,"#9c179e"],[0.4444444444444444,"#bd3786"],[0.5555555555555556,"#d8576b"],[0.6666666666666666,"#ed7953"],[0.7777777777777778,"#fb9f3a"],[0.8888888888888888,"#fdca26"],[1.0,"#f0f921"]]}],"heatmapgl":[{"type":"heatmapgl","colorbar":{"outlinewidth":0,"ticks":""},"colorscale":[[0.0,"#0d0887"],[0.1111111111111111,"#46039f"],[0.2222222222222222,"#7201a8"],[0.3333333333333333,"#9c179e"],[0.4444444444444444,"#bd3786"],[0.5555555555555556,"#d8576b"],[0.6666666666666666,"#ed7953"],[0.7777777777777778,"#fb9f3a"],[0.8888888888888888,"#fdca26"],[1.0,"#f0f921"]]}],"contourcarpet":[{"type":"contourcarpet","colorbar":{"outlinewidth":0,"ticks":""}}],"contour":[{"type":"contour","colorbar":{"outlinewidth":0,"ticks":""},"colorscale":[[0.0,"#0d0887"],[0.1111111111111111,"#46039f"],[0.2222222222222222,"#7201a8"],[0.3333333333333333,"#9c179e"],[0.4444444444444444,"#bd3786"],[0.5555555555555556,"#d8576b"],[0.6666666666666666,"#ed7953"],[0.7777777777777778,"#fb9f3a"],[0.8888888888888888,"#fdca26"],[1.0,"#f0f921"]]}],"surface":[{"type":"surface","colorbar":{"outlinewidth":0,"ticks":""},"colorscale":[[0.0,"#0d0887"],[0.1111111111111111,"#46039f"],[0.2222222222222222,"#7201a8"],[0.3333333333333333,"#9c179e"],[0.4444444444444444,"#bd3786"],[0.5555555555555556,"#d8576b"],[0.6666666666666666,"#ed7953"],[0.7777777777777778,"#fb9f3a"],[0.8888888888888888,"#fdca26"],[1.0,"#f0f921"]]}],"mesh3d":[{"type":"mesh3d","colorbar":{"outlinewidth":0,"ticks":""}}],"scatter":[{"fillpattern":{"fillmode":"overlay","size":10,"solidity":0.2},"type":"scatter"}],"parcoords":[{"type":"parcoords","line":{"colorbar":{"outlinewidth":0,"ticks":""}}}],"scatterpolargl":[{"type":"scatterpolargl","marker":{"colorbar":{"outlinewidth":0,"ticks":""}}}],"bar":[{"error_x":{"color":"#2a3f5f"},"error_y":{"color":"#2a3f5f"},"marker":{"line":{"color":"#E5ECF6","width":0.5},"pattern":{"fillmode":"overlay","size":10,"solidity":0.2}},"type":"bar"}],"scattergeo":[{"type":"scattergeo","marker":{"colorbar":{"outlinewidth":0,"ticks":""}}}],"scatterpolar":[{"type":"scatterpolar","marker":{"colorbar":{"outlinewidth":0,"ticks":""}}}],"histogram":[{"marker":{"pattern":{"fillmode":"overlay","size":10,"solidity":0.2}},"type":"histogram"}],"scattergl":[{"type":"scattergl","marker":{"colorbar":{"outlinewidth":0,"ticks":""}}}],"scatter3d":[{"type":"scatter3d","line":{"colorbar":{"outlinewidth":0,"ticks":""}},"marker":{"colorbar":{"outlinewidth":0,"ticks":""}}}],"scattermapbox":[{"type":"scattermapbox","marker":{"colorbar":{"outlinewidth":0,"ticks":""}}}],"scatterternary":[{"type":"scatterternary","marker":{"colorbar":{"outlinewidth":0,"ticks":""}}}],"scattercarpet":[{"type":"scattercarpet","marker":{"colorbar":{"outlinewidth":0,"ticks":""}}}],"carpet":[{"aaxis":{"endlinecolor":"#2a3f5f","gridcolor":"white","linecolor":"white","minorgridcolor":"white","startlinecolor":"#2a3f5f"},"baxis":{"endlinecolor":"#2a3f5f","gridcolor":"white","linecolor":"white","minorgridcolor":"white","startlinecolor":"#2a3f5f"},"type":"carpet"}],"table":[{"cells":{"fill":{"color":"#EBF0F8"},"line":{"color":"white"}},"header":{"fill":{"color":"#C8D4E3"},"line":{"color":"white"}},"type":"table"}],"barpolar":[{"marker":{"line":{"color":"#E5ECF6","width":0.5},"pattern":{"fillmode":"overlay","size":10,"solidity":0.2}},"type":"barpolar"}],"pie":[{"automargin":true,"type":"pie"}]},"layout":{"autotypenumbers":"strict","colorway":["#636efa","#EF553B","#00cc96","#ab63fa","#FFA15A","#19d3f3","#FF6692","#B6E880","#FF97FF","#FECB52"],"font":{"color":"#2a3f5f"},"hovermode":"closest","hoverlabel":{"align":"left"},"paper_bgcolor":"white","plot_bgcolor":"#E5ECF6","polar":{"bgcolor":"#E5ECF6","angularaxis":{"gridcolor":"white","linecolor":"white","ticks":""},"radialaxis":{"gridcolor":"white","linecolor":"white","ticks":""}},"ternary":{"bgcolor":"#E5ECF6","aaxis":{"gridcolor":"white","linecolor":"white","ticks":""},"baxis":{"gridcolor":"white","linecolor":"white","ticks":""},"caxis":{"gridcolor":"white","linecolor":"white","ticks":""}},"coloraxis":{"colorbar":{"outlinewidth":0,"ticks":""}},"colorscale":{"sequential":[[0.0,"#0d0887"],[0.1111111111111111,"#46039f"],[0.2222222222222222,"#7201a8"],[0.3333333333333333,"#9c179e"],[0.4444444444444444,"#bd3786"],[0.5555555555555556,"#d8576b"],[0.6666666666666666,"#ed7953"],[0.7777777777777778,"#fb9f3a"],[0.8888888888888888,"#fdca26"],[1.0,"#f0f921"]],"sequentialminus":[[0.0,"#0d0887"],[0.1111111111111111,"#46039f"],[0.2222222222222222,"#7201a8"],[0.3333333333333333,"#9c179e"],[0.4444444444444444,"#bd3786"],[0.5555555555555556,"#d8576b"],[0.6666666666666666,"#ed7953"],[0.7777777777777778,"#fb9f3a"],[0.8888888888888888,"#fdca26"],[1.0,"#f0f921"]],"diverging":[[0,"#8e0152"],[0.1,"#c51b7d"],[0.2,"#de77ae"],[0.3,"#f1b6da"],[0.4,"#fde0ef"],[0.5,"#f7f7f7"],[0.6,"#e6f5d0"],[0.7,"#b8e186"],[0.8,"#7fbc41"],[0.9,"#4d9221"],[1,"#276419"]]},"xaxis":{"gridcolor":"white","linecolor":"white","ticks":"","title":{"standoff":15},"zerolinecolor":"white","automargin":true,"zerolinewidth":2},"yaxis":{"gridcolor":"white","linecolor":"white","ticks":"","title":{"standoff":15},"zerolinecolor":"white","automargin":true,"zerolinewidth":2},"scene":{"xaxis":{"backgroundcolor":"#E5ECF6","gridcolor":"white","linecolor":"white","showbackground":true,"ticks":"","zerolinecolor":"white","gridwidth":2},"yaxis":{"backgroundcolor":"#E5ECF6","gridcolor":"white","linecolor":"white","showbackground":true,"ticks":"","zerolinecolor":"white","gridwidth":2},"zaxis":{"backgroundcolor":"#E5ECF6","gridcolor":"white","linecolor":"white","showbackground":true,"ticks":"","zerolinecolor":"white","gridwidth":2}},"shapedefaults":{"line":{"color":"#2a3f5f"}},"annotationdefaults":{"arrowcolor":"#2a3f5f","arrowhead":0,"arrowwidth":1},"geo":{"bgcolor":"white","landcolor":"#E5ECF6","subunitcolor":"white","showland":true,"showlakes":true,"lakecolor":"white"},"title":{"x":0.05},"mapbox":{"style":"light"}}},"xaxis":{"anchor":"y","domain":[0.0,1.0],"title":{"text":"chapter"}},"yaxis":{"anchor":"x","domain":[0.0,1.0],"title":{"text":"count"}},"legend":{"title":{"text":"name"},"tracegroupgap":0},"title":{"text":"Cumulative Number of Times Each Name Appears"},"height":600,"width":900},                        {"responsive": true}                    ).then(function(){

var gd = document.getElementById('113da3fa-69be-4a1b-be85-ff4eec7aa311');
var x = new MutationObserver(function (mutations, observer) {{
        var display = window.getComputedStyle(gd).display;
        if (!display || display === 'none') {{
            console.log([gd, 'removed!']);
            Plotly.purge(gd);
            observer.disconnect();
        }}
}});

// Listen for the removal of the full notebook cells
var notebookContainer = gd.closest('#notebook-container');
if (notebookContainer) {{
    x.observe(notebookContainer, {childList: true});
}}

// Listen for the clearing of the current output cell
var outputEl = gd.closest('.output');
if (outputEl) {{
    x.observe(outputEl, {childList: true});
}}

                        })                };                });            </script>        </div>


### Verificação de conceito ✅ – Resposta em [cc.dsc10.com](http://cc.dsc10.com)

No Capítulo 32, Jo se muda sozinha para Nova York. O relacionamento dela com qual irmã sofre mais com essa mudança distante?

A.Amy

B.Bete

C. Sim

### Verificação de conceito ✅ – Resposta em [cc.dsc10.com](http://cc.dsc10.com)

Laurie é um homem que no final se casa com uma das irmãs. Qual deles?


A.Amy

B.Bete

C. Jo

D. Eu

### Próxima vez

- Na quarta-feira começaremos a programar 💻 em Python 🐍.
- Fique atento ao anúncio via EdStem sobre se a aula de quarta-feira será remota ou presencial. De qualquer forma, as seções de discussão presencial começarão na quarta-feira!