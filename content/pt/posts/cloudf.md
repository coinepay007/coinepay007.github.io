---
title: "Tutorial do Cloudflare: 10 funcionalidades essenciais para iniciantes"
slug: cloudf
date: 2026-11-03
draft: false
---
# Tutorial do Cloudflare: 10 funcionalidades essenciais para iniciantes

## 1. O que é o Cloudflare?

O Cloudflare é uma plataforma de serviços de Internet que ajuda os proprietários de sites a melhorar a velocidade, a segurança e a disponibilidade dos seus websites.

A plataforma oferece diversas ferramentas importantes:

- **Gerenciamento de DNS**: permite gerenciar registros DNS e direcionar os visitantes para o servidor correto.
- **CDN**: acelera o carregamento dos sites por meio de uma rede global de servidores.
- **SSL/TLS**: protege as conexões entre os visitantes e o site.
- **Proteção contra ataques DDoS**: ajuda a reduzir os riscos de ataques de negação de serviço distribuída.
- **WAF (Web Application Firewall)**: filtra solicitações potencialmente maliciosas.
- **Cache**: armazena temporariamente recursos do site para acelerar o carregamento.
- **Analytics**: permite acompanhar estatísticas de tráfego e segurança.
- **Workers**: executa código diretamente na rede do Cloudflare.
- **Pages**: permite publicar sites estáticos e aplicações front-end.

O Cloudflare oferece planos gratuitos e pagos. Os iniciantes podem começar pelo plano gratuito para conhecer as principais funcionalidades.

## 2. Como criar uma conta no Cloudflare e adicionar um site?

Antes de utilizar os recursos do Cloudflare, é necessário criar uma conta e adicionar o seu domínio.

### Etapa 1: Criar uma conta no Cloudflare

Acesse a página oficial de cadastro:

[https://dash.cloudflare.com/sign-up](https://dash.cloudflare.com/sign-up)

Informe seu endereço de e-mail e crie uma senha para registrar sua conta.

### Etapa 2: Adicionar seu site

Depois de entrar na conta, selecione a opção para adicionar um site ou domínio.

Digite o nome do seu domínio, por exemplo:

`example.com`

O Cloudflare analisará os registros DNS existentes e apresentará uma configuração inicial.

### Etapa 3: Verificar os registros DNS

Revise cuidadosamente os registros DNS importados.

Os principais tipos de registros são:

- **A**: associa um domínio a um endereço IPv4.
- **AAAA**: associa um domínio a um endereço IPv6.
- **CNAME**: aponta um domínio para outro nome de domínio.
- **MX**: define os servidores responsáveis pelo recebimento de e-mails.
- **TXT**: armazena informações de texto, utilizadas, por exemplo, em verificações e configurações de e-mail.

Verifique especialmente os registros relacionados ao serviço de e-mail para evitar interrupções no recebimento de mensagens.

### Etapa 4: Alterar os servidores de nomes

O Cloudflare fornecerá dois servidores de nomes (nameservers).

Entre no site da empresa onde você registrou seu domínio e substitua os servidores de nomes antigos pelos fornecidos pelo Cloudflare.

A propagação pode levar algum tempo. Quando a configuração for validada, o Cloudflare começará a gerenciar o tráfego do domínio de acordo com as configurações definidas.

## 3. As 10 funcionalidades essenciais do Cloudflare

### Funcionalidade 1: Gerenciamento de DNS

O gerenciamento de DNS é uma das funções mais importantes do Cloudflare.

Ele permite administrar os registros do domínio e determinar como os visitantes são direcionados ao servidor.

No painel do Cloudflare, abra a seção **DNS** para consultar e modificar os registros.

Você encontrará principalmente dois modos de proxy:

- **Proxied (nuvem laranja)**: o tráfego HTTP/HTTPS passa pela rede do Cloudflare. Isso permite utilizar os serviços de proxy, CDN e proteção disponíveis.
- **DNS Only (nuvem cinza)**: o Cloudflare fornece apenas a resolução DNS. O tráfego não passa pelo proxy da plataforma.

Para um site convencional, os registros A e CNAME utilizados pelo site geralmente podem ser configurados como Proxied.

Atenção: alguns serviços, especialmente os de e-mail, exigem configurações DNS específicas. Não altere esses registros sem verificar o funcionamento do serviço.

### Funcionalidade 2: CDN e aceleração do site

O Cloudflare possui uma rede global de distribuição de conteúdo (CDN).

Quando um visitante acessa seu site, determinados recursos podem ser entregues por um centro de dados do Cloudflare próximo à localização do visitante.

Isso pode reduzir a latência e melhorar a velocidade de carregamento.

Entre os recursos que normalmente podem ser armazenados em cache estão:

- Imagens.
- Arquivos CSS.
- Arquivos JavaScript.
- Fontes.
- Outros recursos estáticos.

Para ativar o proxy do Cloudflare, abra a seção DNS e verifique se os registros do site compatíveis estão configurados com a nuvem laranja.

Depois, você poderá configurar o cache e as regras correspondentes de acordo com as necessidades do site.

### Funcionalidade 3: SSL/TLS e criptografia HTTPS

O SSL/TLS ajuda a proteger as conexões entre os visitantes e seu site.

Um site configurado corretamente com HTTPS protege os dados transmitidos e transmite mais confiança aos visitantes.

No painel do Cloudflare, acesse:

**SSL/TLS → Overview**

Você encontrará diferentes modos de criptografia:

- **Off**: não há criptografia entre o Cloudflare e o visitante.
- **Flexible**: a conexão entre o visitante e o Cloudflare utiliza HTTPS, mas a conexão entre o Cloudflare e o servidor de origem utiliza HTTP.
- **Full**: a conexão entre o visitante, o Cloudflare e o servidor de origem é criptografada, mas o certificado do servidor de origem não é verificado de forma rigorosa.
- **Full (strict)**: a conexão é criptografada e o certificado do servidor de origem é validado.

Quando o servidor de origem possui um certificado válido e configurado corretamente, o modo **Full (strict)** geralmente é a opção recomendada.

Uma configuração SSL incorreta pode causar erros como 525 ou 526. Se esses erros aparecerem, verifique o certificado e as configurações do servidor de origem.

### Funcionalidade 4: Cache e Cache Rules

O cache permite armazenar temporariamente determinados recursos para que eles não precisem ser carregados novamente do servidor de origem a cada visita.

Isso pode melhorar o desempenho do site e reduzir a carga do servidor.

No Cloudflare, você pode utilizar as configurações de cache e as **Cache Rules** para definir quais recursos devem ser armazenados e em quais condições.

Se você atualizar arquivos ou imagens, mas os visitantes continuarem vendo a versão antiga, poderá limpar o cache.

Acesse:

**Caching → Configuration → Purge Cache**

Em seguida, escolha a opção de limpeza de cache adequada.

Atenção: evite armazenar em cache, sem uma configuração cuidadosa, páginas de login, carrinhos de compras, páginas pessoais e páginas que contenham informações de pagamento.

### Funcionalidade 5: Proteção contra DDoS e segurança do site

Os ataques DDoS tentam deixar um site indisponível enviando um grande volume de solicitações.

O Cloudflare oferece mecanismos de proteção destinados a identificar e mitigar diversos tipos de ataques DDoS.

Também é possível consultar os eventos de segurança no painel para entender quais solicitações foram bloqueadas ou sinalizadas.

Essa proteção ajuda a melhorar a disponibilidade do site, mas não garante proteção absoluta contra todas as ameaças.

Por isso, também é importante proteger o servidor de origem, as contas administrativas e as aplicações utilizadas pelo site.

### Funcionalidade 6: WAF (Web Application Firewall)

O WAF do Cloudflare permite filtrar solicitações HTTP que possam representar riscos para sua aplicação web.

Ele pode ajudar a identificar ou bloquear diferentes tipos de solicitações maliciosas, incluindo:

- Injeção de SQL.
- Ataques XSS (Cross-Site Scripting).
- Solicitações suspeitas.
- Algumas tentativas de exploração de vulnerabilidades.

O Cloudflare oferece regras gerenciadas e regras personalizadas.

As **Managed Rules** permitem utilizar conjuntos de regras predefinidos, enquanto as **Custom Rules** oferecem maior controle sobre as condições de filtragem.

As configurações devem ser adaptadas ao seu site. Regras muito rigorosas podem bloquear visitantes legítimos ou prejudicar determinadas funcionalidades.

### Funcionalidade 7: Redirect Rules e redirecionamentos

As Redirect Rules permitem redirecionar automaticamente os visitantes de uma URL para outra.

Esse recurso é útil quando você altera a estrutura do site, muda de domínio ou deseja padronizar os endereços das páginas.

Os dois tipos de redirecionamento mais comuns são:

- **301**: redirecionamento permanente.
- **302**: redirecionamento temporário.

Por exemplo, você pode redirecionar uma página antiga para um novo endereço, evitando erros 404 e facilitando a navegação.

Verifique sempre as condições dos redirecionamentos para evitar loops ou destinos incorretos.

### Funcionalidade 8: Analytics e estatísticas

O Cloudflare Analytics permite consultar diferentes informações relacionadas ao tráfego e à segurança do seu site.

Entre os dados disponíveis, você pode analisar:

- Número de solicitações.
- Volume de dados transferidos.
- Recursos entregues pelo cache.
- Eventos de segurança.
- Algumas tendências de tráfego.

Essas informações ajudam a entender como o site utiliza a rede do Cloudflare e a identificar possíveis problemas.

Atenção: o Cloudflare Analytics não substitui necessariamente o Google Analytics. Os dois serviços não medem exatamente os mesmos indicadores, e seus resultados podem apresentar diferenças.

### Funcionalidade 9: Cloudflare Workers

O Cloudflare Workers permite executar código na rede do Cloudflare sem precisar necessariamente administrar um servidor tradicional.

Esse recurso pode ser utilizado para:

- Criar APIs.
- Processar solicitações HTTP.
- Adicionar lógica personalizada.
- Modificar respostas.
- Desenvolver serviços distribuídos.

Assim, os desenvolvedores podem executar determinadas funções mais próximas dos usuários.

Os limites de utilização e os recursos disponíveis dependem do plano do Cloudflare e da configuração do serviço.

Documentação oficial:

[https://developers.cloudflare.com/workers/](https://developers.cloudflare.com/workers/)

### Funcionalidade 10: Cloudflare Pages

O Cloudflare Pages é uma plataforma que permite publicar sites estáticos e aplicações front-end.

Ele pode ser conectado a um repositório do GitHub para automatizar as implantações.

O processo geral é o seguinte:

1. Conecte sua conta do GitHub.
2. Selecione o repositório do projeto.
3. Configure o comando de compilação (Build command), se necessário.
4. Informe o diretório de saída (Build output directory).
5. Inicie a implantação.
6. Configure um domínio personalizado, se necessário.

O Cloudflare Pages é especialmente adequado para sites de documentação, blogs estáticos e projetos front-end.

Documentação oficial:

[https://developers.cloudflare.com/pages/](https://developers.cloudflare.com/pages/)

## 4. Configurações do Cloudflare recomendadas para iniciantes

Se você acabou de conectar seu site ao Cloudflare, é melhor começar com uma configuração simples.

Veja as etapas recomendadas:

1. Adicione seu domínio e confirme se os servidores de nomes estão configurados corretamente.
2. Verifique os registros DNS, especialmente os relacionados ao site e ao serviço de e-mail.
3. Configure SSL/TLS de acordo com o certificado instalado no servidor de origem.
4. Ative o proxy do Cloudflare para os registros do site compatíveis.
5. Configure o cache para recursos estáticos.
6. Revise as configurações de segurança e do WAF.
7. Acompanhe as estatísticas e os eventos de segurança.

Evite alterar muitas configurações ao mesmo tempo. Assim, será mais fácil identificar a causa caso algum problema apareça.

## 5. Problemas comuns do Cloudflare e como resolvê-los

### Problema 1: O site parou de funcionar depois de conectar ao Cloudflare

Possíveis causas:

- Os registros DNS estão incorretos.
- Os servidores de nomes ainda não foram propagados.
- O endereço IP do servidor de origem está errado.
- O servidor de origem está bloqueando conexões provenientes do Cloudflare.

Soluções:

1. Verifique os registros DNS.
2. Confirme se o endereço IP do servidor está correto.
3. Verifique as configurações do firewall do servidor.
4. Confira o status da conexão no painel do Cloudflare.

### Problema 2: Erro 522

O erro 522 geralmente indica que o Cloudflare não conseguiu estabelecer uma conexão com o servidor de origem dentro do tempo esperado.

Possíveis causas:

- O servidor está offline ou sobrecarregado.
- O firewall está bloqueando as conexões.
- O servidor não responde dentro do prazo esperado.
- Existe algum problema na configuração da rede.

Soluções:

- Verifique se o servidor de origem está funcionando.
- Revise as regras do firewall.
- Confirme se os endereços IP do Cloudflare não estão bloqueados.
- Entre em contato com seu provedor de hospedagem se o problema continuar.

### Problema 3: Erro 525

O erro 525 indica uma falha na negociação SSL entre o Cloudflare e o servidor de origem.

Soluções:

- Verifique se o certificado SSL do servidor está instalado corretamente.
- Confirme se o servidor oferece suporte a uma configuração TLS compatível.
- Revise as configurações de SSL/TLS do Cloudflare.
- Entre em contato com seu provedor de hospedagem, se necessário.

### Problema 4: As imagens ou os arquivos não são atualizados

Esse problema geralmente está relacionado ao cache.

Soluções:

1. Abra o painel do Cloudflare.
2. Acesse a seção Caching.
3. Selecione Purge Cache.
4. Limpe o cache correspondente.
5. Atualize o site e verifique o resultado.

### Problema 5: O plano gratuito é suficiente?

Para um site pessoal, um blog ou um pequeno site institucional, o plano gratuito do Cloudflare pode ser suficiente para começar.

Ele oferece acesso a várias funcionalidades essenciais, incluindo gerenciamento de DNS, proxy, CDN e determinados recursos de segurança.

Sites com necessidades mais avançadas podem considerar um plano pago, dependendo do volume de tráfego, dos requisitos de segurança e das funcionalidades necessárias.

## 6. Recursos oficiais do Cloudflare

Para aprofundar seus conhecimentos e consultar as instruções mais recentes, utilize os seguintes recursos oficiais:

- Site oficial: [https://www.cloudflare.com/](https://www.cloudflare.com/)
- Painel de controle: [https://dash.cloudflare.com/](https://dash.cloudflare.com/)
- Documentação para desenvolvedores: [https://developers.cloudflare.com/](https://developers.cloudflare.com/)
- Documentação de DNS: [https://developers.cloudflare.com/dns/](https://developers.cloudflare.com/dns/)
- Documentação de SSL/TLS: [https://developers.cloudflare.com/ssl/](https://developers.cloudflare.com/ssl/)
- Documentação do WAF: [https://developers.cloudflare.com/waf/](https://developers.cloudflare.com/waf/)
- Documentação do Workers: [https://developers.cloudflare.com/workers/](https://developers.cloudflare.com/workers/)
- Documentação do Pages: [https://developers.cloudflare.com/pages/](https://developers.cloudflare.com/pages/)

É recomendável consultar a documentação oficial antes de modificar configurações importantes do domínio ou do servidor.

## 7. Conclusão: O Cloudflare é adequado para iniciantes?

O Cloudflare oferece diversas ferramentas para melhorar o desempenho, a segurança e o gerenciamento de um site.

As dez funcionalidades apresentadas neste guia abrangem as principais necessidades dos iniciantes:

1. Gerenciamento de DNS.
2. CDN e aceleração do site.
3. SSL/TLS e HTTPS.
4. Cache e Cache Rules.
5. Proteção contra ataques DDoS.
6. WAF.
7. Redirect Rules.
8. Analytics.
9. Workers.
10. Pages.

Não é necessário dominar todas essas funcionalidades desde o início. Comece conectando seu domínio, verificando os registros DNS, configurando o HTTPS e ativando os recursos básicos. Depois, explore gradualmente as ferramentas mais avançadas.

Para usuários que também trabalham com pagamentos online ou serviços digitais, pode ser útil conhecer ferramentas independentes como CoinePay e TRXAPI.

**CoinePay — plataforma de cartão virtual**

Para conhecer uma solução de pagamento com cartão virtual destinada a determinados pagamentos online:

[https://www.coinepay.net/login?referrer=7PFFZMCH](https://www.coinepay.net/login?referrer=7PFFZMCH)

**TRXAPI — serviço de aluguel de energia TRON**

Para conhecer um serviço independente de aluguel de energia TRON:

[https://www.trxapi.io/energy.html?lang=zh-TW](https://www.trxapi.io/energy.html?lang=zh-TW)

Código de convite TRXAPI: **57YQDGFU**

Observação: CoinePay e TRXAPI são serviços independentes de terceiros. Eles não são produtos do Cloudflare nem parceiros oficialmente afiliados à plataforma.

## 8. Referências

- Cloudflare: [https://www.cloudflare.com/](https://www.cloudflare.com/)
- Documentação oficial: [https://developers.cloudflare.com/](https://developers.cloudflare.com/)
- DNS: [https://developers.cloudflare.com/dns/](https://developers.cloudflare.com/dns/)
- SSL/TLS: [https://developers.cloudflare.com/ssl/](https://developers.cloudflare.com/ssl/)
- WAF: [https://developers.cloudflare.com/waf/](https://developers.cloudflare.com/waf/)
- Analytics: [https://developers.cloudflare.com/analytics/](https://developers.cloudflare.com/analytics/)
- Workers: [https://developers.cloudflare.com/workers/](https://developers.cloudflare.com/workers/)
- Pages: [https://developers.cloudflare.com/pages/](https://developers.cloudflare.com/pages/)

