# produtodigital
     A dor escolhida e por que ela vale um negócio;     O tamanho de mercado e o Business Model Canvas;     A tese que o MVP testa, e o que ficou manual de propósito;     O mega prompt e as correções que você pediu depois;     O endereço da aplicação publicada.

# MEGA PROMPT — MVP DO E-BOOK SORRISO DE MENINA

## 1. Contexto do projeto

Crie uma aplicação web responsiva para comercializar o e-book **Sorriso de Menina**, de autoria de **Marcio Antonio Gonçalves dos Santos**.

O projeto faz parte do desafio DIO “Meu Negócio com IA”. O objetivo é lançar um MVP simples, funcional e seguro para validar a venda direta de um produto digital.

- **Produto:** e-book Sorriso de Menina.
- **Autor:** Marcio Antonio Gonçalves dos Santos.
- **Preço oficial:** R$ 19,90.
- **Público inicial:** pais, mães, responsáveis e familiares interessados em histórias com significado para compartilhar com crianças.
- **Objetivo comercial:** vender o e-book e gerar renda.
- **Tecnologia:** Lovable Cloud para backend, autenticação e armazenamento de dados, usando os recursos nativos disponíveis.
- **Idioma da interface:** português brasileiro.
- **Moeda:** real brasileiro (BRL).

Não crie uma loja genérica. Crie uma página de vendas específica para esta obra literária.

## 2. Identidade e conteúdo

O título deve ser exatamente **Sorriso de Menina**.

O nome do autor deve aparecer como:

**Marcio Antonio Gonçalves dos Santos**

Não utilizar o nome “Eliza” em nenhum lugar da interface.

A obra apresenta a história de Sorriso, uma menina de 11 anos que vive com os pais em situação de rua em Curitiba e mantém o sonho de estudar e construir um futuro. A narrativa aborda sonhos, educação, dignidade, solidariedade e vulnerabilidade social.

Use uma comunicação humana, respeitosa e acolhedora. Não explore o sofrimento da personagem de forma sensacionalista e não prometa resultados educacionais ou emocionais garantidos.

Não invente depoimentos, avaliações, prêmios, números de vendas, credenciais ou recomendações.

Utilize a capa e o arquivo original do e-book somente quando forem fornecidos pelo proprietário. Não gere uma capa substituta como se fosse a capa oficial.

## 3. Página pública de vendas

Crie uma landing page moderna, elegante, acessível e responsiva, com boa experiência em celulares.

### Seção principal

Exibir:
- Capa oficial do livro, quando disponibilizada.
- Título: Sorriso de Menina.
- Autor: Marcio Antonio Gonçalves dos Santos.
- Frase de apresentação: “Uma história sobre sonhos, dignidade e esperança.”
- Preço destacado: R$ 19,90.
- Botão principal: “Quero meu e-book”.
- Botão secundário: “Conheça a história”.

### Seção sobre o livro

Criar uma sinopse fiel à obra, apresentando Sorriso e seus sonhos de estudar e construir um futuro diferente.

Destacar que a leitura pode abrir espaço para conversas em família sobre educação, empatia e solidariedade, sem prometer resultados garantidos.

### Seção de detalhes

Exibir apenas informações confirmadas. Se formato, número de páginas, compatibilidade ou condições de entrega ainda não estiverem configurados, permitir que o administrador os preencha antes da publicação.

### Perguntas frequentes

Incluir perguntas sobre:
- O que é o e-book?
- Qual é o preço?
- Como funciona a compra?
- Como o arquivo será entregue?
- Com quem falar em caso de dúvida?

Não afirmar que o pagamento está integrado nem que a entrega é automática se isso ainda não tiver sido implementado.

### Chamada final

Repetir o preço de R$ 19,90 e o botão de compra.

Incluir rodapé com identificação do autor, contato comercial configurável e política de privacidade.

## 4. Fluxo de compra do MVP

Na primeira versão, permitir fechamento manual da venda.

Ao clicar em “Quero meu e-book”:
1. Mostrar as opções de contato e compra configuradas pelo administrador.
2. Permitir que o interessado informe nome, e-mail opcional e WhatsApp opcional, além de confirmar o interesse.
3. Registrar o lead no Lovable Cloud quando houver consentimento.
4. Se houver um número de WhatsApp comercial configurado, disponibilizar um link de contato com uma mensagem inicial contendo o título do livro e o preço de R$ 19,90.
5. Registrar o pedido no painel administrativo quando criado pelo fluxo implementado.
6. Permitir que o administrador marque o pedido como “Aguardando pagamento”, “Pago”, “Entregue”, “Cancelado” ou “Reembolsado”.
7. Entregar o arquivo somente depois da confirmação legítima do pagamento.

Não simular pagamentos, comprovantes, pedidos pagos ou entregas concluídas.

Não criar integração fictícia com Stripe, Mercado Pago ou outro provedor. Deixar a estrutura preparada para uma futura integração real, caso seja necessária.

## 5. Formulário de interessados

Criar um formulário com:
- Nome.
- E-mail opcional.
- WhatsApp opcional.
- Campo opcional: “Como conheceu o livro?”
- Consentimento explícito para receber contato sobre a compra.

Validar os dados, mostrar mensagens claras de sucesso ou erro e prevenir envios duplicados em sequência.

Solicitar somente os dados necessários. Não tornar o consentimento obrigatório para publicidade futura como condição para uma pessoa consultar a página.

## 6. Área administrativa protegida

Criar uma área de administração com autenticação real.

O painel deve permitir:
- Visualizar total de leads.
- Visualizar pedidos registrados.
- Filtrar pedidos por status.
- Consultar data, valor e dados de contato necessários para a venda.
- Atualizar status do pedido.
- Registrar manualmente a confirmação de pagamento.
- Registrar a entrega do arquivo.
- Consultar a origem do lead, quando informada.
- Exportar dados apenas para administradores autorizados, se esse recurso for implementado com segurança.

Não permitir cadastro público como administrador.

Não confiar apenas em ocultar a URL do painel. Aplicar autenticação, autorização e regras de acesso no backend.

Criar um mecanismo seguro para definir o primeiro administrador, sem inserir senha fixa ou credenciais no código-fonte.

## 7. Lovable Cloud e modelo de dados

Utilizar Lovable Cloud para persistência de dados, autenticação e funções de backend quando disponíveis.

Não conectar Supabase externo, Firebase ou outro banco de dados independente.

Estruturar os dados necessários para:
- Leads.
- Pedidos.
- Status de pagamento e entrega.
- Configurações públicas da loja.
- Perfil e permissões administrativas.

Definir identificadores únicos, datas de criação e atualização, validação de dados e relações necessárias.

Não armazenar dados completos de cartão, senhas em texto simples ou informações financeiras desnecessárias.

O status “Pago” só pode ser alterado por um administrador autorizado ou por uma futura integração de pagamento verificada no servidor.

## 8. Proteção do e-book e segurança

O arquivo completo do e-book não deve ficar em uma pasta pública acessível por um link previsível.

Usar armazenamento privado e URLs temporárias ou outro mecanismo seguro de entrega, caso suportado pela configuração escolhida.

Verificar autorização no servidor antes de disponibilizar o arquivo.

Não incluir segredos, tokens, senhas, chaves privadas ou credenciais em arquivos públicos ou no frontend.

Aplicar regras de acesso para impedir que visitantes leiam dados de outros clientes ou modifiquem pedidos.

Validar todos os dados enviados pelo navegador no backend.

Implementar proteção contra spam e submissões abusivas quando suportado.

Criar política de privacidade com explicação clara sobre coleta, finalidade, retenção e contato para solicitações de titulares, conforme a LGPD.

## 9. Design e experiência do usuário

Usar uma identidade visual literária, acolhedora e profissional, com boa legibilidade e contraste.

Preferir fundo claro, tons suaves, tipografia elegante e espaços generosos.

Evitar aparência de marketplace genérico, excesso de animações e elementos que distraiam da compra.

Garantir:
- Layout adaptável a celulares, tablets e computadores.
- Botões acessíveis e com estados de carregamento.
- Formulários com rótulos claros.
- Mensagens de erro úteis.
- Estados vazios no painel administrativo.
- Navegação por teclado.
- Contraste e acessibilidade adequados.

Não utilizar imagens aleatórias como se fossem a capa real do livro.

## 10. Métricas de validação

Preparar o sistema para acompanhar:
- Visitas à página, quando houver uma ferramenta de análise configurada de forma adequada.
- Cliques no botão de compra.
- Leads registrados.
- Pedidos criados.
- Pedidos pagos.
- Pedidos entregues.
- Taxa de conversão de visita para lead.
- Taxa de conversão de pedido para venda.
- Origem declarada dos interessados.

Não inventar dados iniciais ou preencher o painel com vendas fictícias.

## 11. Critérios de conclusão

Considerar o MVP pronto para testes quando:
1. A página pública exibir título, autor e preço corretos.
2. O nome “Eliza” não aparecer em nenhuma parte do projeto.
3. O formulário validar e registrar os dados corretamente.
4. Os leads e pedidos forem armazenados no Lovable Cloud.
5. O painel administrativo exigir autenticação e autorização.
6. O fluxo de compra explicar claramente o procedimento manual.
7. Nenhum pedido for marcado automaticamente como pago sem confirmação.
8. O arquivo completo não estiver exposto publicamente.
9. A aplicação funcionar em dispositivos móveis e computadores.
10. Os estados de erro, carregamento e sucesso tiverem sido testados.

Antes de publicar, execute a revisão de segurança disponível na Lovable, corrija os problemas identificados e teste o fluxo completo com dados de teste.

Construa primeiro a versão funcional mínima. Não adicione assinaturas, marketplace, inteligência artificial conversacional, campanhas automatizadas ou integrações de pagamento complexas nesta etapa.

Ao terminar, apresente um resumo do que foi implementado, o que ainda depende de configuração manual e quais testes precisam ser concluídos antes da publicação.
