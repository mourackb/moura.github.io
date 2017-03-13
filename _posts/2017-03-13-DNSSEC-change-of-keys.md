---
layout: post
title: Fellow Report ICANN 57
---

## Troca de chaves no DNSSEC
### Não tenha seu acesso para a Internet comprometido

Ao contrário de ser uma caixa preta com um botão vermelho como é retratada em "The it crowd", a Internet, também conhecida como a redes das redes, é uma conjunção de diversos atores que concordaram ou adotaram os mesmos protocolos para que todos os dispositivos dentro dessa "rede" pudessem se comunicar ( e futuramente se espionar, se atacar e se duplicar). Dentro destes arranjos entre os operadores da rede está um acordo (um modelo "opt-in") para todos usarem o mesmo sistema de endereçamento de nomes e domínios(também conhecido como DNS).

Quando você está conectado a esta imensa rede de dispositvos você começa a conexão na rede pelo seu ISP ( Internet Service Provider | Provedor de Internet)	que terá rotas para chegar a quaisquer outro dispositivo da rede que você queira alcançar. A adoção deste modelo é tema para teses de mestrado e doutorado e eu não acredito ter capacidade (por enquanto) para explicar em apenas um texto.

Este ISP lhe entregará as requisições de rede que você solicitar ( quer seja elas um site do sua loja favorita ou uma foto de um gatinho fofo). Quando você quer, por exemplo, saber as últimas do Projeto Tamar. Você só precisa lembrar do domínio tamar.org.br e não o endereço IP completo (um conjunto decimal e no caso do Ipv6 um conjunto hexadecimal).
No início todos os atores da rede se conheciam, contudo com a constante expansão e sucesso da rede (é estimado que hoje 3 bilhões de pessoas estejam conectadas) entrou em jogo um novo ator, alguém com intenções maliciosas. Esta pessoa mal intencionada pode se fazer passar por um domínio que não é ela. Este tipo de alteração não é relvante para gatinhos fofos, mas para operações que envolvem dinheiro a ação lesa o usuário final. Para resolver este problema a comunidade técnica criou e está adotando o DNSSEC. 

O DNSSec é um conjunto de extensões que são inseridas no DNS que consultamos. Através de assinaturas digitais a tarefa de se passar por outro site se torna inviável. Estas assinaturas são assinadas por chaves criptográficas e uma boa prática é trocar de tempos em tempos as chaves para que não seja possível falsificar chaves identicas. Algo parecido ocorre quando alugamos um apartamento e trocamos as chaves e fechaduras de entrada do apartamento.

Talvez para um usuário final de Internet todas essas informações podem não ser relevantes, mas o que contece se seu ISP não tiver atualizado para as chaves novas? O que acontece se você trocar as fechaduras da sua casa e não pegar as chaves novas? A resposta para as perguntas anteriores são semelhantes, você fica sem acesso!(adeus gatinhos fofos!) Se seu ISP utiliza DNSSEC e não sincronizar as novas chaves você pode ter seu acesso comprometido (mesmo que temporariamente).

Antes de gerar um alarde e anunciar o caos,  saiba o que fazer. A sua ação se resume a contatar o seu ISP e perguntar se ele utiliza o DNSSEC (Pois deveria para a segurança de seus usuários!) e se ele já está ciente da trocas das chaves (o termo técnico é Root Zone Key Signing Key (KSK)).

Não sabe qual o seu ISP? Recomendo o site https://www.whoismyisp.org/

*Nem ly e nem lerey*
Você pode ter o seu acesos a Internet comprometido, consulte seu ISP e veja se ele utiliza DNSSEC e caso positivo se ele está ciente da troca das chaves.

### Referências
https://www.icann.org/resources/pages/ksk-rollover
https://tools.ietf.org/html/rfc5011
https://www.ietf.org/rfc/rfc4033.txt
https://tools.ietf.org/html/rfc4035
