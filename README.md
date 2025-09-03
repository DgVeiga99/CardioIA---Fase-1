# 📌 CardioIA – Fase 1: Batimentos de Dados  

Este repositório reúne os dados preparados para a **Fase 1 do Projeto CardioIA**, que inaugura nossa jornada de integração entre **tecnologia, ciência de dados e saúde cardiovascular**.  
A proposta é simular um ambiente hospitalar moderno em que dados clínicos são coletados, organizados e analisados com suporte de **Inteligência Artificial** para apoiar diagnósticos, triagens e previsões médicas.  

Aqui, estruturamos três tipos de dados fundamentais:  
1. **Numéricos** (IoT/variáveis clínicas de pacientes).  
2. **Textuais** (artigos e relatórios médicos).  
3. **Visuais** (imagens de exames de ECG).  

Essas informações representam a base de qualquer sistema inteligente aplicado à saúde, preparando terreno para as próximas fases de desenvolvimento em **NLP, visão computacional e modelos preditivos de machine learning**.  

---

## 🧮 Parte 1 – Dados Numéricos (IoT)  

📂 Local: [`/dataset`](./dataset)  
🔗 Link público: *[inserir link do Google Drive/OneDrive]*  

Foi criado um **dataset sintético de 300 pacientes**, que simula de forma fiel o que seria um **banco de dados de um hospital real**.  
Embora tenhamos buscado inicialmente dados oficiais (DATASUS, IBGE, Vigitel), optamos por **simular registros clínicos** devido às restrições legais da **LGPD/GDPR**. A simulação, porém, não é aleatória: aplicamos **regras clínicas baseadas em artigos científicos e diretrizes médicas**, de forma a garantir consistência e representatividade.  

### 🔹 Variáveis incluídas
- **Dados demográficos**: idade, sexo, peso, altura, IMC.  
- **Sinais vitais e exames básicos**: pressão arterial sistólica/diastólica, frequência cardíaca de repouso.  
- **Exames laboratoriais**: colesterol total, LDL, HDL, triglicerídeos.  
- **Histórico clínico**: presença de diabetes, tabagismo, sedentarismo, histórico familiar.  
- **Eventos anteriores**: infarto prévio.  
- **Sintomas**: dor torácica, palpitações, falta de ar, tontura, desmaio ou ausência de sintomas.  
- **Medicações**: anti-hipertensivos, estatinas, anticoagulantes, polimedicação ou nenhum.  

### 🔹 Relevância clínica e tecnológica
Na prática hospitalar, esses parâmetros são **a base do processo de triagem**. São os primeiros dados coletados em consultas de rotina ou emergenciais, e servem para:  
- **Classificação de risco**: identificar rapidamente se o paciente precisa de atendimento imediato.  
- **Predição de eventos**: modelos de IA podem detectar padrões sutis entre colesterol, pressão arterial e histórico familiar que indicam risco elevado de infarto ou AVC.  
- **Apoio à decisão médica**: algoritmos de aprendizado supervisionado podem sugerir condutas baseadas em milhares de registros, aumentando a assertividade clínica.  

Assim, mesmo sendo simulados, esses dados representam a espinha dorsal de qualquer sistema de inteligência artificial aplicado à cardiologia.  

---

## 📖 Parte 2 – Dados Textuais (NLP)  

📂 Local: [`/docs`](./docs)  
Contém artigos em `.txt`, convertidos de fontes acadêmicas como **Google Acadêmico, SciELO, BVS e SUS**.  

### 🔹 Fontes e Conteúdo
Os textos selecionados abordam:  
- **Sintomas clínicos de infarto**: dor no peito, palpitações, falta de ar, fadiga, entre outros.  
- **Estudos epidemiológicos**: prevalência de hipertensão, diabetes e dislipidemias na população brasileira.  
- **Revisões científicas**: atualizações sobre diagnóstico por ECG, uso de biomarcadores e intervenções terapêuticas.  
- **Análises históricas**: tendências de mortalidade cardiovascular ao longo das últimas décadas.  

### 🔹 Relevância clínica e tecnológica
O uso de textos médicos amplia a perspectiva da IA, pois complementa os dados numéricos com **conhecimento não estruturado**. Esses dados textuais permitem:  
- **Extração automática de sintomas e sinais** mencionados em laudos e artigos clínicos.  
- **Identificação de variáveis de maior impacto** (ex.: estatísticas que mostram que hipertensão e diabetes estão presentes em mais de 60% dos pacientes infartados).  
- **Classificação temática** (prevenção, diagnóstico, tratamento), possibilitando organizar bases de conhecimento em cardiologia.  
- **Treinamento de chatbots médicos** capazes de interpretar perguntas e fornecer respostas fundamentadas em literatura científica.  

Na prática clínica, grande parte do conhecimento está em **formato textual**. Incorporar NLP no CardioIA significa transformar esse vasto material em informação estruturada e acionável por sistemas de IA.  

---

## 🫀 Parte 3 – Dados Visuais (Visão Computacional)  

📂 Local: [`/images`](./images)  
🔗 Link público: *[inserir link do Google Drive/OneDrive]*  

As imagens foram coletadas da base pública **Mendeley Data**, reconhecida na comunidade científica. Essa base apresenta quatro tipos de pacientes:  

1. ECGs de **infarto do miocárdio**.  
2. ECGs com **batimentos anormais** (arritmias).  
3. ECGs de pacientes com **histórico de infarto**.  
4. ECGs de **pacientes normais (controle)**.  

### 🔹 Seleção Inicial
Para esta fase inicial, priorizamos **ECGs de infarto**, mas os demais grupos poderão ser incorporados em fases futuras, tornando o modelo mais robusto e versátil.  

### 🔹 Relevância clínica e tecnológica
O ECG é um dos exames mais importantes e acessíveis para diagnóstico rápido de infarto. No contexto da IA, as imagens podem ser usadas para treinar **redes neurais convolucionais (CNNs)**, que aprendem a identificar padrões como ondas **P, QRS e T** e reconhecer sinais de isquemia e necrose.  

No futuro, o uso de todas as categorias da base permitirá criar um **classificador multiclasse** (normal, arritmia, infarto, histórico de infarto), aumentando o poder preditivo do sistema.  

---

## ⚖️ Governança e Ética em Dados  

A utilização de dados em projetos de Inteligência Artificial na saúde exige um olhar cuidadoso para **questões éticas, legais e sociais**. A confidencialidade das informações de pacientes é protegida pela **LGPD (Lei Geral de Proteção de Dados)** e também por princípios internacionais como o **GDPR**, tornando inviável o uso direto de prontuários médicos sem anonimização e consentimento. Por isso, neste projeto, optamos pela construção de uma base **simulada, porém clinicamente fiel**, que nos permite explorar padrões e treinar modelos sem colocar em risco a privacidade de indivíduos.  

Além da proteção de dados, outro ponto central da governança em IA é a **prevenção de vieses algorítmicos**. Dados desbalanceados em termos de gênero, idade, etnia ou condição socioeconômica podem levar a modelos injustos, que oferecem diagnósticos mais precisos para certos grupos e menos confiáveis para outros. Esse risco é particularmente crítico em saúde, onde decisões enviesadas podem impactar vidas. Assim, a simulação aplicada neste projeto buscou equilibrar variáveis e representar um conjunto heterogêneo de pacientes, garantindo que os futuros algoritmos desenvolvidos possam oferecer resultados mais justos e robustos.  

Outro aspecto relevante é a **transparência**: é fundamental que todo o processo de coleta, geração e preparação dos dados seja documentado, de forma que qualquer avaliador, pesquisador ou profissional de saúde compreenda de onde vieram as informações, como foram tratadas e quais limitações existem. Esse compromisso com a rastreabilidade fortalece a **confiabilidade dos resultados** e cria bases sólidas para validações posteriores, tanto técnicas quanto éticas.  

Por fim, a governança em IA na saúde não se limita à proteção de dados e à transparência, mas também à **responsabilidade social**. A integração entre tecnologia e cardiologia precisa sempre respeitar o princípio da **beneficência**, garantindo que os algoritmos desenvolvidos tenham como objetivo ampliar o acesso à saúde, melhorar diagnósticos, otimizar recursos hospitalares e, principalmente, salvar vidas.  

---

## 📌 Conclusão  

A primeira fase do projeto CardioIA marca um passo fundamental para a consolidação de um ecossistema de dados voltado à saúde cardiovascular. A criação de um dataset numérico simulado, com variáveis clinicamente relevantes, representa o esforço de espelhar a realidade hospitalar dentro de um ambiente seguro e ético. Em paralelo, a seleção de artigos científicos transformados em dados textuais amplia a capacidade de análise, permitindo que a inteligência artificial aprenda a identificar sintomas, padrões e correlações de grande valor clínico. Por fim, a incorporação de imagens de ECG provenientes de bases públicas, como o Mendeley Data, abre caminho para que modelos de visão computacional possam reconhecer alterações cardíacas de forma automatizada e precisa.  

Essa integração entre diferentes tipos de dados — estruturados, textuais e visuais — mostra o potencial da IA para transformar a prática médica, oferecendo apoio à tomada de decisão, acelerando diagnósticos e reduzindo erros humanos. Mais do que um exercício acadêmico, esta fase inicial evidencia a importância da governança, da ética e da responsabilidade social no uso de tecnologias emergentes aplicadas à saúde. Trata-se do alicerce de um projeto que, nas próximas etapas, se expandirá em direção a modelos inteligentes de classificação de risco, chatbots médicos com NLP e redes neurais convolucionais para análise de exames, reforçando o compromisso de unir ciência, tecnologia e humanidade em prol da vida.  
