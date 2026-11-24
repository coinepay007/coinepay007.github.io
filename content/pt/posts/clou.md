---
title: Como Configurar o Cloudflare CDN (Guia 2027)
slug: clou
date: 2026-11-24
draft: false
---
Como Configurar o Cloudflare CDN (Guia 2027)

O Cloudflare CDN é uma solução popular para melhorar o desempenho de sites, reduzir o tempo de carregamento e adicionar uma camada extra de segurança. Por meio da rede global do Cloudflare, os proprietários de sites podem armazenar conteúdo estático em cache, proteger seus servidores e otimizar o acesso de visitantes de diferentes regiões.

Seja para um blog WordPress, um site empresarial, uma loja virtual ou um site hospedado em um VPS, configurar o Cloudflare CDN pode ser uma ótima maneira de melhorar o desempenho da sua página.

Neste guia, você vai aprender como configurar o Cloudflare CDN em 2027, conectar seu domínio, configurar registros DNS, ativar o proxy, ajustar as opções de cache e solucionar problemas comuns.

Se você também utiliza ferramentas de pagamento online para acessar serviços internacionais, pode conhecer o CoinePay como uma opção para pagamentos online.

👉 **CoinePay 官方入口：**  
[https://www.coinepay.net/register?referrer=RFGSSDZ9](https://www.coinepay.net/register?referrer=RFGSSDZ9)

Se você também utiliza a rede TRON para transferir USDT, pode conhecer o serviço de aluguel de energia TRON oferecido pela TRXAPI, que pode ajudar a reduzir o consumo de recursos TRX em determinadas transações compatíveis.

👉 **TRXAPI 官方入口：**  
[https://login.trxapi.io/energy](https://login.trxapi.io/energy)

## **O que é o Cloudflare CDN?**

O Cloudflare CDN é uma rede de distribuição de conteúdo que ajuda a disponibilizar os recursos de um site por meio de uma rede global de servidores. Em vez de cada visitante se conectar diretamente ao servidor de origem, o Cloudflare pode entregar conteúdo armazenado em cache a partir de um local mais próximo do visitante.

O Cloudflare também oferece outros serviços, incluindo gerenciamento de DNS, proteção contra ataques DDoS, filtragem de tráfego, suporte a SSL/TLS e diferentes opções de cache.

As principais vantagens do Cloudflare CDN incluem:

- Maior velocidade de carregamento para visitantes de diferentes regiões.
- Redução do consumo de largura de banda do servidor de origem.
- Proteção adicional contra determinados tipos de tráfego malicioso e ataques DDoS.
- Suporte à criptografia SSL/TLS.
- Gerenciamento flexível de DNS.
- Recursos de cache e otimização de sites.

O Cloudflare oferece planos gratuitos e pagos. Muitas funcionalidades básicas de CDN podem ser configuradas utilizando o plano Free.

## **O que você precisa antes de configurar o Cloudflare CDN**

Antes de conectar seu site ao Cloudflare, verifique se você possui:

- Um nome de domínio registrado.
- Um site ou servidor de hospedagem já funcionando.
- Acesso ao painel de gerenciamento do seu registrador de domínio.
- Acesso aos registros DNS do seu domínio.
- O endereço IP do servidor de hospedagem, se necessário.

Se seu domínio já estiver conectado a um site, verifique a configuração DNS existente antes de fazer alterações. Registros DNS incorretos podem deixar seu site, serviço de e-mail ou outros serviços indisponíveis.

## **Etapa 1: Criar uma conta no Cloudflare**

Primeiro, acesse o site oficial do Cloudflare:

[https://www.cloudflare.com/](https://www.cloudflare.com/)

Crie uma conta utilizando seu endereço de e-mail e uma senha.

Depois de concluir o cadastro, faça login no painel do Cloudflare. A partir daí, você poderá adicionar seu domínio e configurar DNS, segurança, cache e outros recursos.

## **Etapa 2: Adicionar seu domínio ao Cloudflare**

Depois de fazer login:

1. Abra o painel do Cloudflare.
2. Selecione a opção para adicionar ou conectar um domínio.
3. Digite seu domínio, por exemplo, [example.com](http://example.com).
4. Avance para a próxima etapa.
5. Escolha um plano.

Para a maioria dos sites pessoais, blogs e pequenos projetos, o plano Free é um bom ponto de partida.

O Cloudflare tentará identificar automaticamente os registros DNS existentes e importá-los para sua interface de gerenciamento DNS.

## **Etapa 3: Verificar os registros DNS**

Antes de ativar o Cloudflare, revise cuidadosamente seus registros DNS.

Os tipos mais comuns de registros DNS são:

- Registro A: aponta um domínio ou subdomínio para um endereço IPv4.
- Registro AAAA: aponta um domínio ou subdomínio para um endereço IPv6.
- Registro CNAME: aponta um domínio ou subdomínio para outro nome de host.
- Registro MX: define os servidores de e-mail do domínio.
- Registro TXT: utilizado para verificações, SPF, DKIM, DMARC e outras configurações.

Certifique-se de que os principais registros do seu site estejam corretos.

Por exemplo:

Registro A

Nome: @

Conteúdo: endereço IP do seu servidor

Registro CNAME

Nome: www

Conteúdo: seu domínio principal ou o nome de host fornecido pelo seu provedor de hospedagem.

Os registros exatos dependem da configuração do seu serviço de hospedagem.

Se você utiliza e-mail associado ao domínio, mantenha corretamente configurados os registros MX, TXT e outros registros relacionados ao serviço de e-mail. O proxy do Cloudflare não faz proxy do tráfego convencional de e-mail. Por isso, esses registros geralmente devem permanecer no modo DNS Only.

## **Etapa 4: Ativar o proxy do Cloudflare**

Uma das etapas mais importantes da configuração do Cloudflare CDN é ativar o serviço de proxy.

Na seção de gerenciamento DNS, você encontrará uma opção de status do proxy para os registros compatíveis.

Proxied — Nuvem laranja

Quando a nuvem laranja está ativada, o tráfego dos registros compatíveis passa pela rede do Cloudflare. Isso permite utilizar os recursos correspondentes de CDN, segurança e proxy.

DNS Only — Nuvem cinza

Quando a nuvem cinza está ativada, o Cloudflare fornece apenas a resolução DNS, sem encaminhar o tráfego pela sua rede de proxy.

Para os principais registros do seu site, como o registro A do domínio e o registro A ou CNAME de www, ative a opção Proxied se sua configuração permitir.

Não ative o proxy automaticamente para todos os registros DNS. Alguns serviços, como e-mail e determinados registros de verificação ou serviços de terceiros, precisam permanecer no modo DNS Only.

## **Etapa 5: Alterar os nameservers do seu domínio**

Depois de verificar os registros DNS, o Cloudflare fornecerá dois nameservers para seu domínio.

Você deverá substituir os nameservers atuais pelos fornecidos pelo Cloudflare.

O processo geralmente funciona assim:

1. Faça login na conta do seu registrador de domínio.
2. Abra a página de gerenciamento do domínio.
3. Localize as configurações de nameservers.
4. Substitua os nameservers existentes pelos dois fornecidos pelo Cloudflare.
5. Salve as alterações.

A propagação das alterações nos nameservers pode levar algum tempo.

Durante esse período, a resolução DNS pode variar dependendo da rede e do cache DNS. Evite fazer alterações desnecessárias enquanto a ativação estiver em andamento.

Se o DNSSEC estiver ativado no seu domínio, verifique sua configuração antes de alterar os nameservers. Uma configuração incorreta do DNSSEC pode impedir a resolução do domínio.

## **Etapa 6: Configurar SSL/TLS**

O SSL/TLS é importante para proteger as conexões do seu site e evitar avisos de segurança no navegador.

No painel do Cloudflare:

1. Selecione seu domínio.
2. Abra a seção SSL/TLS.
3. Verifique o modo de criptografia.
4. Escolha o modo adequado à configuração SSL do seu servidor de origem.

O Cloudflare geralmente oferece os seguintes modos SSL/TLS:

Flexible

O modo Flexible criptografa a conexão entre os visitantes e o Cloudflare, mas a conexão entre o Cloudflare e seu servidor de origem não é criptografada.

Esse modo pode ser utilizado quando o servidor de origem não possui um certificado SSL, mas geralmente não é a configuração recomendada a longo prazo.

Full

O modo Full criptografa a conexão entre o Cloudflare e o servidor de origem. Seu servidor precisa oferecer suporte a HTTPS, mas o certificado não precisa necessariamente ser emitido por uma autoridade certificadora pública confiável.

Full (Strict)

O modo Full (Strict) criptografa a conexão e valida o certificado do servidor de origem. Seu servidor precisa ter um certificado válido que atenda aos requisitos do Cloudflare.

Para a maioria dos sites que já possuem HTTPS configurado corretamente, o modo Full (Strict) é recomendado.

Antes de ativá-lo, certifique-se de que seu servidor de origem possui um certificado SSL válido.

## **Etapa 7: Configurar o cache do Cloudflare**

O cache do Cloudflare permite armazenar determinados recursos do seu site na rede da plataforma. Dessa forma, esses recursos podem ser entregues aos visitantes sem precisar buscá-los repetidamente no servidor de origem.

Para configurar o cache:

1. Abra seu domínio no painel do Cloudflare.
2. Acesse as configurações de cache.
3. Verifique as opções disponíveis.
4. Ajuste o comportamento do cache de acordo com as necessidades do seu site.

Os recursos estáticos que normalmente podem ser armazenados em cache incluem:

- Imagens.
- Arquivos CSS.
- Arquivos JavaScript.
- Fontes.
- Páginas HTML estáticas, quando apropriado.

Conteúdos dinâmicos, páginas de login, carrinhos de compras, painéis de controle e conteúdos personalizados exigem uma configuração mais cuidadosa.

Em sites WordPress, evite armazenar indiscriminadamente em cache páginas que contenham informações de login, dados personalizados de usuários, informações do carrinho de compras ou funções administrativas.

Você pode utilizar as Cache Rules do Cloudflare para definir quais URLs devem ser armazenadas em cache e como esse comportamento será aplicado.

## **Etapa 8: Configurar as Cache Rules**

As Cache Rules permitem controlar o comportamento do cache para URLs ou condições específicas.

Por exemplo, você pode:

- Armazenar arquivos estáticos em cache por períodos mais longos.
- Excluir páginas administrativas do cache.
- Evitar o armazenamento em cache de páginas de login.
- Aplicar configurações diferentes de cache a determinados subdomínios.
- Controlar o comportamento do cache para tipos específicos de conteúdo.

Se você utiliza WordPress, considere excluir os seguintes caminhos do cache quando necessário:

- /wp-admin/
- /wp-login.php

Dependendo da configuração do seu site, também pode ser necessário excluir páginas dinâmicas, páginas de pagamento ou conteúdos personalizados.

Sempre teste seu site depois de modificar as Cache Rules.

## **Etapa 9: Limpar o cache do Cloudflare**

Quando você atualiza seu site, mas os visitantes continuam vendo conteúdo antigo, o problema pode estar relacionado ao cache.

Você pode limpar o cache diretamente no Cloudflare.

1. Abra o painel do Cloudflare.
2. Selecione seu domínio.
3. Acesse a seção de cache.
4. Localize a opção de limpeza do cache.
5. Escolha o método de limpeza adequado.

O Cloudflare oferece diferentes opções para remover conteúdos armazenados em cache. Dependendo das suas necessidades, você pode limpar URLs específicas ou remover um conjunto maior de conteúdos.

Para atualizações comuns do site, geralmente é melhor limpar apenas o cache das URLs afetadas em vez de apagar todo o cache.

## **Etapa 10: Testar o Cloudflare CDN**

Depois de configurar o Cloudflare, verifique se seu site está funcionando corretamente.

Confira os seguintes pontos:

- Seu site abre normalmente.
- O HTTPS funciona sem avisos do navegador.
- Os registros DNS são resolvidos corretamente.
- As versões com www e sem www funcionam como esperado.
- Os serviços de e-mail continuam funcionando.
- Os recursos estáticos estão sendo armazenados em cache quando apropriado.

Você também pode verificar os cabeçalhos HTTP das respostas.

Por exemplo, o seguinte cabeçalho pode aparecer:

cf-cache-status

Os valores mais comuns incluem:

- HIT: o recurso solicitado foi entregue a partir do cache.
- MISS: o recurso não estava no cache e foi buscado no servidor de origem.
- BYPASS: o cache foi ignorado.
- DYNAMIC: o recurso não é considerado adequado para o armazenamento em cache convencional.
- EXPIRED: o recurso armazenado em cache expirou.

Nem todas as solicitações precisam retornar HIT. Páginas dinâmicas e recursos não armazenados em cache podem retornar outros status normalmente.

Você também pode utilizar ferramentas de teste de desempenho, como PageSpeed Insights, GTmetrix ou WebPageTest, para avaliar a velocidade de carregamento e o desempenho do seu site.

## **Problemas comuns do Cloudflare CDN**

### **Erro 521 do Cloudflare**

O erro 521 geralmente indica que o Cloudflare não consegue estabelecer uma conexão com o servidor de origem porque o servidor está recusando a conexão.

Possíveis soluções:

- Verifique se o servidor está funcionando.
- Confirme se o firewall permite o tráfego do Cloudflare.
- Verifique o serviço web do servidor de origem.
- Revise as regras do firewall e dos softwares de segurança.

### **Erro 522 do Cloudflare**

O erro 522 indica um tempo limite de conexão entre o Cloudflare e o servidor de origem.

As possíveis causas incluem:

- Sobrecarga do servidor de origem.
- Regras de firewall bloqueando o Cloudflare.
- Problemas de conectividade de rede.
- Atrasos na resposta do servidor.

Verifique seu servidor de hospedagem e a configuração da rede.

### **Erros de certificado SSL**

Os erros SSL podem ocorrer quando a configuração SSL/TLS do Cloudflare não corresponde à configuração do certificado do servidor de origem.

Verifique os seguintes pontos:

- O certificado SSL do servidor de origem é válido.
- O modo SSL/TLS selecionado é adequado.
- O HTTPS está configurado corretamente no servidor de origem.
- Não existem regras de redirecionamento incompatíveis.

### **O conteúdo do site não é atualizado**

Se seu site continua exibindo conteúdo antigo:

- Limpe o cache correspondente no Cloudflare.
- Limpe o cache do navegador.
- Verifique as Cache Rules.
- Confira se o plugin de cache do seu site está causando o problema.

## **O Cloudflare CDN é gratuito?**

O Cloudflare oferece um plano Free que inclui diversos recursos de DNS, proxy, segurança e cache.

Para muitos sites pessoais, blogs e pequenos sites empresariais, o plano Free é suficiente para começar.

Os planos pagos oferecem recursos e serviços adicionais, dependendo do plano e da disponibilidade atual dos produtos.

A escolha do plano mais adequado depende do tráfego do seu site, das necessidades de segurança, dos requisitos de desempenho e do seu orçamento.

## **Lista de verificação da configuração do Cloudflare CDN**

Antes de concluir a configuração, confira os seguintes itens:

- Seu domínio foi adicionado ao Cloudflare.
- Os registros DNS foram revisados.
- Os principais registros do site estão configurados corretamente.
- O proxy está ativado para os registros de site compatíveis.
- Os nameservers foram atualizados.
- O SSL/TLS está configurado corretamente.
- As configurações de cache foram revisadas.
- As páginas dinâmicas não estão sendo armazenadas em cache incorretamente.
- Seu site carrega corretamente por HTTPS.
- Os registros DNS do serviço de e-mail continuam corretos.
- O desempenho do site foi testado.

## **Conclusão**

Configurar o Cloudflare CDN é uma maneira prática de melhorar a distribuição do conteúdo do seu site, gerenciar DNS e adicionar uma camada extra de proteção.

O processo básico consiste em adicionar seu domínio ao Cloudflare, revisar os registros DNS, ativar o proxy, atualizar os nameservers, configurar SSL/TLS e ajustar as regras de cache.

Embora o Cloudflare ofereça muitos recursos avançados, os iniciantes podem começar com uma configuração básica e otimizar o site gradualmente, conforme suas necessidades.

Ao configurar corretamente o DNS, o proxy, o SSL/TLS e o cache, você pode criar uma infraestrutura web mais eficiente e melhorar a experiência dos visitantes de diferentes regiões.

Recursos oficiais do Cloudflare:

Configuração de domínio no Cloudflare:  
[https://developers.cloudflare.com/fundamentals/manage-domains/add-site/](https://developers.cloudflare.com/fundamentals/manage-domains/add-site/)

Status do proxy do Cloudflare:  
[https://developers.cloudflare.com/dns/proxy-status/](https://developers.cloudflare.com/dns/proxy-status/)

Cache Rules do Cloudflare:  
[https://developers.cloudflare.com/cache/how-to/cache-rules/](https://developers.cloudflare.com/cache/how-to/cache-rules/)

Limpeza do cache do Cloudflare:  
[https://developers.cloudflare.com/cache/how-to/purge-cache/](https://developers.cloudflare.com/cache/how-to/purge-cache/)