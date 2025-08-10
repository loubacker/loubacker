<h1>

# [![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&size=20&pause=1000&color=2476F7&width=435&lines=Ol%C3%A1%2C+Me+chamo+Gabriel+Loubacker!%F0%9F%91%8B%F0%9F%8F%BB;Sou+Desenvolvedor+Full-Stack;Especialista+em+Infraestrutura+%F0%9F%96%A5%EF%B8%8F;Arquiteturas+Distribuidas;Microservices%2C+Cloud+Computing+%E2%98%81%EF%B8%8F)](https://git.io/typing-svg)
</h1>

<img align="right" alt="coding gif" width="400" src="https://media2.giphy.com/media/v1.Y2lkPTc5MGI3NjExN3V5eTA4N2N1dHdxeHlyazU4NXgyOWR6eDV5YzI0YXRpcWFkcXJndyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9cw/UmWpVKOvNEv6CHVtl7/giphy.gif">
<br>
&nbsp;
<p align="left">Sou Desenvolvedor Back-End e Especialista em Infraestrutura, proficiente em Java e ecossistema Spring. Possuo uma forte base de conhecimento em arquiteturas de software robustas e padrões de SAGA para arquiteturas distribuídas, com foco em construir soluções eficientes, escaláveis e observáveis. Atualmente trabalho e atuo como desenvolvedor em 2 empresas, foco em aprimoramento de sistemas, performance e segurança da infraestrutura.</p>

<h3>Áreas de especialização:</h3>

- Especialista em infraestrutura
- Especialização em Microserviços e Arquitetura de Software
- Engenharia de Soluções com Foco em Arquitetura Distribuída e Cloud Computing

<br>
<p>
📬 Conecte-se comigo:
</p>
<p>
  <a href="https://www.instagram.com/loubacker">
    <img loading="lazy" src="https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white" alt="Instagram Badge">
  </a>
  <a href="https://www.linkedin.com/in/loubacker">
    <img loading="lazy" src="https://custom-icon-badges.demolab.com/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn Badge">
  </a>
</p>

<p>
  <img align="center" height="180em" src="https://github-readme-stats-lyart-chi-67.vercel.app/api?username=loubacker&show_icons=true&theme=dracula"/>
  <img align="center" height="180em" src="https://github-readme-stats-lyart-chi-67.vercel.app/api/top-langs/?username=loubacker&layout=compact&theme=dracula"/>
</p>

<br>

## 💻 Tecnologias e Ferramentas:
<h3>Desenvolvedor Full-Stack</h3>
<p>Minha base tecnológica é formada pelo ecossistema Java, mas também possuo uma vasta experiência em infraestrutura de serviços Cloud e Linux, que são as bases para construir sistemas sólidos, escaláveis, resilientes e eficientes. Tenho um forte domínio em ambientes de produção, com expertise em migração de dados, refatoração de código e entidades, e modificação de tabelas diretamente via SQL. Além disso, possuo ampla experiência em mapear servidores e serviço Cloud, fazer backup de aplicações via Git e backup do bancos de dados em produção. Tenho amplo conhecimento da sintaxe no uso e na administração do NGINX, para balanceamento de carga, reverse proxy, cache management, e configuração de firewall em VPS e serviços Cloud, utilizando Gateway. Esses elementos são fundamentais na minha abordagem para garantir a robustez, segurança e alta disponibilidade dos sistemas.</p>

<img loading="lazy" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/nginx/nginx-original.svg" width="100" height="100"/>
<h5> Exp: Reverse Proxy com Gateway e SSL </h5>

```nginx
server {
    servername service.domínio.com.br ;
    
    location / {

        auth_request /gateway-auth;

        proxy_pass http://localhost:X;
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
        proxy_set_header Authorization $http_authorization;
        proxy_set_header Cookie $http_cookie;
    }

    location = /gateway-auth {
        internal;
        proxy_pass https://gateway.dominio.com.br/auth-check;
        proxy_pass_request_body off;
        proxy_set_header Content-Length "";
        proxy_set_header X-Original-URI $request_uri;
        proxy_set_header Authorization $http_authorization;
        proxy_set_header Cookie $http_cookie;
    }

    error_page 401 403 = @auth_redirect;
    location @auth_redirect {
        return 302 https://gateway.dominio.com.br/auth?redirect_uri=$scheme://$host$request_uri;
    }

    listen 443 ssl;
    ssl_certificate /etc/letsencrypt/live/service.dominio.com.br/fullchain.pem;
    ssl_certificate_key /etc/letsencrypt/live/service.dominio.com.br/privkey.pem;
    include /etc/letsencrypt/options-ssl-nginx.conf;
    ssl_dhparam /etc/letsencrypt/ssl-dhparams.pem;

}

server {
    if ($host = service.dominio.com.br) {
        return 301 https://$host$request_uri;
    }

    server_name service.dominio.com.br;
    listen 80;
    return 404;

}
```

<p>Além disso, tenho proficiência em Docker, tanto para aplicações backend como frontend, incluindo frameworks como React e Angular. Também gerencio aplicações Spring diretamente na máquina via systemd e unit/service. Sou capaz de configurar e integrar variáveis de ambiente através de arquivos .env, configurar certificados SSL via Let's Encrypt para domínios e subdomínios, sem custo com wildcards, e implementar monitoramento para escalabilidade vertical e horizontal, garantindo alta disponibilidade. Em cenários de alta demanda, consigo escalar e separar servidores de forma isolada para Banco de Dados, Cacheamento Redis, e realizar duplicação de servidores para aumentar o fluxo de clientes, tudo configurado manualmente na unha, minimizando ao máximo os custos, e sem a dependência de serviços como AWS.</p>

<h4> 🛠 Backend & Tecnologias:</h4> 
<p>
  <img loading="lazy" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/java/java-original-wordmark.svg" width="50" height="50"/>
  &nbsp;
  <img loading="lazy" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/spring/spring-original-wordmark.svg" width="50" height="50"/>
  &nbsp;
  <img loading="lazy" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/linux/linux-original.svg" width="50" height="50"/>
  &nbsp;
  <img loading="lazy" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/docker/docker-original-wordmark.svg" width="50" height="50"/>
  &nbsp;
  <img loading="lazy" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/amazonwebservices/amazonwebservices-plain-wordmark.svg" width="50" height="50"/>
  &nbsp;
  <img loading="lazy" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/postgresql/postgresql-original-wordmark.svg" width="50" height="50"/>
  &nbsp;
  <img loading="lazy" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/redis/redis-original.svg" width="50" height="50"/>
  &nbsp;
  <img loading="lazy" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/mongodb/mongodb-original.svg" width="50" height="50"/>
</p>
<br>
          
## 👁️ Infraestrutura, Performance & Observabilidade:
<h3> Especialista em Observabilidade </h3>
<p>Tenho um foco dedicado em observabilidade, garantindo que as aplicações sejam transparentes, resilientes e de alto desempenho. Meu fluxo de trabalho segue o padrão OTLP (OpenTelemetry Protocol), a cada serviço e aplicação Spring utilizo o Actuator, Micrometer e o Cloud Sleuth para coleta e envio de métricas, logs e tracing. Essas dependências integradas ao OTLP tornam a implementação rápida, eficiente e de baixo custo, sem a necessidade de sistemas de mensageria com brokers. Além disso, como muitas dessas ferramentas são escritas em GO e rodam em código de máquina, e o consumo de memória e processamento é minimizado, proporcionando uma solução leve e escalável. A implementação pode ser realizada tanto via gRPC quanto REST, garantindo flexibilidade no ambiente de produção.</p>
<p>
<img loading="lazy" src="https://img.shields.io/badge/OpenTelemetry-109010?style=for-the-badge&logo=opentelemetry&logoColor=white" />
<img loading="lazy" src="https://img.shields.io/badge/Cloudflare-F38020?style=for-the-badge&logo=Cloudflare&logoColor=white" />
</p>
<table bg=ffffff>
  <tr>
    <td valign="top"><img loading="lazy" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/grafana/grafana-plain-wordmark.svg" width="40" height="40"/></td>
    <td valign="top"><img loading="lazy" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/prometheus/prometheus-plain-wordmark.svg" width="45" height="45"/></td>
    <td valign="top"><img loading="lazy" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/jaegertracing/jaegertracing-plain-wordmark.svg" width="45" height="45"/></td>
  </tr>
</table>
<br>

## <img width="23" height="23" alt="image" src="https://github.com/user-attachments/assets/ef2905a8-3bab-478b-b920-9b7ce2cf96c7" />&nbsp;Frontend:
<h3> Segurança, SPA's Distribuidos e Orquestração </h3>
<p>
  <tr>
    <td valign="top"><img loading="lazy" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/thymeleaf/thymeleaf-original.svg" width="40" height="40"/></td>
    <td valign="top"><img loading="lazy" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/html5/html5-original.svg" width="40" height="40"/></td>
    <td valign="top"><img loading="lazy" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/css3/css3-original.svg" width="40" height="40"/></td>
    <td valign="top"><img loading="lazy" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/tailwindcss/tailwindcss-original.svg" width="40" height="40"/></td>
    <td valign="top"><img loading="lazy" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/javascript/javascript-original.svg" width="40" height="40"/></td>
    <td valign="top"><img loading="lazy" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/typescript/typescript-original.svg" width="40" height="40"/></td>
    <td valign="top"><img loading="lazy" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/angularjs/angularjs-original.svg" width="40" height="40"/></td>
    <td valign="top"><img loading="lazy" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/react/react-original.svg" width="40" height="40"/></td>
  </tr>
</p>
<p>No meu desenvolvimento front-end com Spring, utilizo principalmente HTML, CSS e Thymeleaf para renderizar templates dinâmicos, como páginas de autenticação, envio de e-mails, reset de senhas e páginas estáticas. Essa abordagem é simples e prática, especialmente para implementações rápidas no servidor de autenticação. No entanto, para sites institucionais, que funcionam como a vitrine da empresa, prefiro usar React, pois ele oferece uma gama mais ampla de bibliotecas que me permitem focar na experiência do usuário (UX) e na interface (UI), proporcionando interações mais ricas e dinâmicas.</p>

<p>Para dashboards e sistemas robustos, como os utilizados em clínicas, hospitais, escritórios de advocacia ou até mesmo em e-commerce, o Angular é minha escolha. Isso porque ele oferece uma tipagem forte e um acoplamento mais eficiente, essenciais quando lidamos com sistemas complexos, onde múltiplos painéis de acesso são controlados por diferentes roles e permissões. O Angular se destaca em termos de performance, especialmente em aplicações com grande quantidade de componentes interativos.</p>

<p><img width="400" alt="image" src="https://github.com/user-attachments/assets/6380d57a-a95d-4aac-b171-03e6e8afea5e"/></p>

<p>Ao falar sobre frontend para grandes serviços administrativos, aplico a mesma lógica de microserviços. No caso de SPAs, que atuam como orquestradores, temos diferentes dashboards interconectados, liberados conforme o role do usuário. Cada acesso à rota do serviço SPA ou dos dashboards, independentemente do orquestrador, sempre passa por um gateway, configurado diretamente no serviço da VPS ou da cloud, utilizando NGINX para o proxy. Isso garante a segurança e a resiliência das aplicações, pois o gateway filtra o tráfego, protegendo os SPAs. Além disso, o BFF (Backend For Frontend), que atua como porta de entrada, se comunica com os serviços distribuídos no backend, e é o único ponto de comunicação com o frontend. A segurança é reforçada através de autenticação com cookies HttpOnly e secure, além de CSRF com Double Submit.</p>

<table>
  <tr>
    <td valign="top">
      <h5>Configuração dos Cookies, adiciona e limpa os cookies</h5>
      <img loading="lazy" align="left" width="400" alt="image" src="https://github.com/user-attachments/assets/ec58b238-d7ad-4909-b9f9-529a7b7150a5"/>
    </td>
    <td valign="top">
      <h5>Interceptador adiciona os headers de segurança (CSRF e Fingerprint) nas requisições</h5>
      <img loading="lazy" align="right" width="500" alt="image" src="https://github.com/user-attachments/assets/b7e24252-2f49-4cda-b35e-1c94b3a09bc1"/>
    </td>
  </tr>
</table>

<p>No que diz respeito ao CSS, em todos os SPAs, mesmo utilizando Angular, sempre opto por TailwindCSS em vez de CSS tradicional. Embora o Angular não compile o Tailwind nativamente, então sempre faço uso de uma abordagem híbrida, utilizando Tailwind para a maior parte do design e completando com CSS customizado quando necessário. No entanto, o objetivo é sempre usar Tailwind para garantir a consistência no desenvolvimento visual.</p>

<!-- ![Logo](https://images.weserv.nl/?url=URL_AQUI&bg=ffffff) -->

<h5> Fluxo de Autenticação e Vida dos Tokens para Front-End </h5>
<td valign="top"><img align="center" width="800" alt="image" src="https://github.com/user-attachments/assets/c2f26a51-41cf-4948-bd21-a1111d3c99e6"/></td>


