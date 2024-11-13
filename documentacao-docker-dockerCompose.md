# Sumário

- [O que é Docker?](#o-que-e-docker)
- [Para que serve o Docker?](#para-que-serve-o-docker)
- [Como funciona o Docker?](#como-funciona-o-docker)

# O que é Docker?

Docker é uma ferramenta que permite criar e gerenciar containers, que são como "caixinhas" onde colocamos aplicativos e tudo o que eles precisam para rodar. Com Docker, você pode empacotar seu código junto com todas as dependências, como bibliotecas, configurações, e até o sistema operacional, em uma única "imagem" que pode ser executada em qualquer lugar.

Imagine que você é um chef de cozinha, e cada prato que você faz depende de ingredientes específicos. Em vez de arrumar uma nova cozinha com todos os ingredientes e equipamentos certos em cada lugar onde você vai cozinhar, você coloca tudo numa caixa — ingredientes, utensílios, receita, tudo! Aí, quando você precisa preparar o prato, basta pegar a caixa e abrir em qualquer cozinha, e tudo estará lá para funcionar exatamente do mesmo jeito.

Docker faz a mesma coisa, mas para aplicativos. Ele cria um "container", que é uma versão leve de uma máquina virtual, para isolar o aplicativo do resto do sistema operacional. Assim, você consegue garantir que o seu aplicativo vai rodar sempre do mesmo jeito, independente do ambiente (seja no seu computador, no servidor de produção ou no servidor de outra empresa).

# Para que serve o Docker?

Docker é muito útil para:

1. **Padronizar Ambientes:** Com Docker, você consegue garantir que seu aplicativo vai rodar de maneira idêntica no seu ambiente de desenvolvimento, no ambiente de testes, e em produção. Isso evita o famoso problema de "funciona na minha máquina, mas não funciona no servidor".

2. **Portabilidade:** Você pode rodar os containers Docker em qualquer lugar que tenha o Docker instalado. Isso inclui ambientes de desenvolvimento local, servidores de produção, e até provedores de nuvem como AWS, Azure, e Google Cloud.

3. **Escalabilidade:** No Docker, você consegue criar vários containers idênticos de forma rápida para lidar com mais tráfego, o que é muito útil para sistemas que precisam escalar horizontalmente.

4. **Isolamento:** Cada container roda de forma isolada dos outros, então você pode ter múltiplos containers com versões diferentes de uma mesma aplicação ou biblioteca, sem conflito.

5. **Automação e CI/CD:** Docker é ótimo para pipelines de integração contínua e entrega contínua (CI/CD), porque facilita a automatização da criação, teste, e implementação de versões do software.

# Como funciona o Docker?

No Docker, você cria imagens, que são como um "molde" para os containers. A imagem define o que o container precisa para rodar, incluindo o código, dependências, e o sistema operacional. Com base nessa imagem, o Docker consegue "construir" e rodar os containers, que são instâncias executáveis dessa imagem.

Para criar uma imagem, você escreve um Dockerfile, que é um arquivo de texto onde você define cada etapa para construir o ambiente do container.