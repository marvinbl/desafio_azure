## desafio_azure

# Documentação: Prática com Azure Speech Studio e Language Studio

## Visão Geral
Esta documentação tem como objetivo registrar práticas e insights adquiridos no uso das ferramentas **Azure Speech Studio** e **Azure Language Studio**, com foco em análise de fala e processamento de linguagem natural (NLP). O propósito é desenvolver habilidades práticas na criação de soluções baseadas em inteligência artificial para voz e linguagem, organizando anotações em um repositório GitHub para referência futura e suporte a estudos.
- Para mais informações acesse **/images** aqui neste repositório

### Objetivos
- Praticar e aprofundar o uso do **Azure Speech Studio** e **Azure Language Studio**.
- Criar um repositório organizado contendo anotações, insights e exemplos práticos.
- Explorar funcionalidades como transcrição de fala em tempo real e análise de sentimentos em textos.

### Entregáveis
- Repositório GitHub com arquivos Markdown contendo anotações e resultados.
- Exemplos práticos de transcrição e análise de linguagem.
- Documentação clara para consulta futura e implementação em projetos.

## Configuração do Azure

### Pré-requisitos
- Conta Microsoft ativa.
- Acesso ao [Portal do Azure](https://portal.azure.com/).
- Informações de contato (endereço, número de celular) e cartão de crédito (necessário para validação, mas **não será cobrado**; o Azure oferece crédito de $200 e estorno automático para contas gratuitas).
- Período de acesso gratuito: **12 meses** (você será notificado por e-mail antes do término).

### Etapas de Configuração do Azure Language Studio
1. **Crie uma Conta Microsoft**:
   - Acesse [account.microsoft.com](https://account.microsoft.com/) e crie ou faça login em sua conta.
2. **Acesse o Azure Portal**:
   - Vá para [https://portal.azure.com/](https://portal.azure.com/).
3. **Crie um Recurso de Linguagem**:
   - No portal, pesquise por **"Language"** na barra de busca.
   - Nos resultados, em "Serviços", clique em **Language Service**.
   - Selecione **Criar** > **Language**.
4. **Configure o Recurso**:
   - **Grupo de Recursos**: Insira um nome (e.g., `meu-grupo-azure`).
   - **Região**: Escolha **Brazil South** (ou outra região disponível).
   - **Nome da Instância**: Use um nome no formato `letra-hífen-numérico` (e.g., `lang-service-001`).
   - **Preço**: Selecione a opção **Grátis** (Free F0).
   - Marque a caixa **Uso de IA Sustentável**.
5. **Finalize**:
   - Clique em **Examinar + Criar** e, após validação, em **Criar**.
   - Aguarde a criação do recurso (geralmente alguns minutos).

### Etapas de Configuração do Azure Speech Studio
1. **Acesse o Speech Studio**:
   - Vá para [https://speech.microsoft.com/portal](https://speech.microsoft.com/portal) e faça login com sua conta Microsoft.
   - Caso redirecionado, acesse [https://ai.azure.com/explore/models/aiservices/Azure-AI-Speech](https://ai.azure.com/explore/models/aiservices/Azure-AI-Speech).
2. **Crie um Recurso de Fala**:
   - Siga um processo semelhante ao do Language Studio:
     - No [Portal do Azure](https://portal.azure.com/), pesquise por **Speech**.
     - Clique em **Criar** > **Speech Service**.
     - Configure com **Grupo de Recursos**, **Região** (Brazil South), **Nome** (e.g., `speech-service-001`), e **Preço** (Free F0).
     - Confirme e crie o recurso.

## Uso do Azure Language Studio
1. **Acesse o Language Studio**:
   - Vá para [https://language.cognitive.azure.com/](https://language.cognitive.azure.com/) e faça login.
2. **Vincule o Recurso**:
   - No perfil, clique em **Inserir Recurso** e selecione o recurso de linguagem criado.
3. **Teste Funcionalidades**:
   - Experimente opções gratuitas, como:
     - **Análise de Sentimentos**: Identifique emoções em textos.
     - **Extração de Insights**: Extraia entidades ou frases-chave.
     - **Resumo de Texto**: Gere resumos automáticos.
   - Insira um texto, clique em **Run** e analise os resultados.

## Uso do Azure Speech Studio
1. **Acesse o Speech Studio**:
   - Use [https://speech.microsoft.com/portal](https://speech.microsoft.com/portal).
2. **Teste Funcionalidades**:
   - Experimente a **Transcrição em Tempo Real** (gratuita por 1 minuto).
   - Exemplo de resultado de transcrição (teste realizado):
     > "E aí, vocês já imaginam o que aconteceu, né? É, em 64 acontece o golpe civil-militar e esse três retiros também do fantasia eles feita e que ele vai falar um pouco do sentimento deste momento. Em poucos minutos o meu avião decolava rumo ao Pacífico. O Furtado vai constar o primeiro ato institucional da ditadura estabelecida no AI-1. Então ele vai ser convidado, né? A seguir a cheirar do país, então, em poucos minutos, o meu avião decolava rumo ao Pacífico. Sentir a certa angústia ao cortar o vínculo com o mundo que por tanto tempo dera sentido à minha vida. Dediquei anos a organizar a minha fantasia, na esperança de um dia transformá-la em instrumentos de ação a serviço do meu pobre e desvalido Nordeste. Agora esta fantasia estava desfeita. Desmoronara como uma estrela que se quis dizer."

3. **Análise do Resultado**:
   - A transcrição capturou o áudio com precisão, mas inclui alguns erros (e.g., "AI-1" como "ayu", "quis dizer" no final).
   - Sentimento identificado: **Angústia** e **nostalgia**, refletidos em frases como "certa angústia ao cortar o vínculo" e "fantasia estava desfeita".
   - Insights: O texto menciona eventos históricos (golpe de 1964, ato institucional) e temas de perda e esperança, relacionados ao Nordeste brasileiro.

## Estrutura do Repositório
Este repositório (`hi-world`) contém:
- Arquivos Markdown (e.g., `azure-notes.md`) com anotações e resultados.
- Opcional: Scripts Python para automação ou análise de resultados (a serem adicionados).
- Arquivo `.gitignore` para ignorar arquivos temporários (e.g., `__pycache__`, `.venv`).

### Exemplo de Estrutura
```
hi-world/
├── README.md
├── azure-notes.md
├── .gitignore
└── data/
    └── transcricao-exemplo.txt
```

## Próximos Passos
- **Aprofundar Testes**:
  - Testar outras funcionalidades do Language Studio, como extração de entidades ou tradução.
  - Explorar conversão de texto para fala no Speech Studio.
- **Automatizar com Python**:
  - Criar scripts para interagir com as APIs do Azure Speech e Language.
  - Exemplo: Usar a biblioteca `azure-cognitiveservices-speech` para transcrição programática.
- **Melhorar Documentação**:
  - Adicionar mais exemplos de transcrições e análises.
  - Organizar anotações em seções específicas (e.g., "Testes de Fala", "Testes de NLP").

## Notas
- **Acesso Gratuito**: O plano gratuito do Azure é limitado (e.g., 1 minuto de transcrição em tempo real). Considere o uso eficiente dos recursos.
- **GitHub Pages**: Para exibir esta documentação como uma página web, habilite o GitHub Pages no repositório (`Settings > Pages > Source: main, Folder: /root`).
- **Submódulos**: Se o submódulo `repo-remoto` contiver arquivos relacionados, mova-os para o repositório principal para simplificar (conforme discutido anteriormente).
