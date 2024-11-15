# Projeto SIEM - Documentação
Esse documento serve para explicar o projeto e descrever passo a passo como realizá-lo no seu ambiente.

## Instalação e configuração do homelab
Nessa seção, você irá instalar todos os ambientes necessários para a realização deste projeto.

### VirtualBox
O VirtualBox é um software de virtualização gratuito e de código aberto que permite criar e gerenciar máquinas virtuais(VMs) em um único computador.
Com ele, você pode instalar sistemas operacionais completos(como Windows, Linux ou macOS) em uma "máquina virtual" que roda dentro do sistema operacional principal, conhecido como sistema hospedeiro.

Algumas das principais funcionalidades do VirtualBox:
- **Variedade de sistemas operacionais**: Suporta a criação de VMs para diversos sistemas operacionais.
- **Compartilhamento de pastas e dispositivos**: Permite acessar pastas do sistema hospedeiro e compartilhar dispositivos USB nas máquinas virtuais.
- **Modo de rede variável**: Oferece diversas opções para configurar a rede, como NAT, bridge e host-only, permitindo controlar como a VM se conecta à rede externa e interage com o hospedeiro.
- **Snapshots**: Permite criar "fotos" do estado atual da máquina virtual para facilitar a recuperação em caso de erros.

A melhor maneira de instalar o VirtualBox é através do site oficial [aqui](https://www.virtualbox.org/wiki/Downloads)

Aqui você deve escolher o download que pertence ao seu SO principal.

![virtualboxscreenshot](/screenshots/virtualbox.png)

Feita a instalação, execute o arquivo de setup do VirtualBox.

### Kali Linux
O Kali Linux é uma distribuição Linux voltada para segurança da informação, conhecida por sua ampla coleção de ferramentas para testes de penetração, análise forense digital, e pesquisa em segurança cibernética.
Ele é baseado no Debian e foi desenvolvido pela Offensive Security, uma organização conhecida na área de segurança.

Características Principais do Kali Linux:
- Conjunto de ferramentas: O Kali Linux vem com mais de 600 ferramentas pré-instaladas voltadas para atividades como:
    - Testes de penetração (ex: Nmap, Metasploit).
    - Engenharia reversa.
    - Análise forense.
    - Segurança de rede.
- Facilidade de uso para profissionais de segurança: Ele é projetado para ser uma plataforma fácil de configurar e usar para profissionais de segurança e entusiastas, fornecendo um ambiente otimizado para essas atividades.
- Atualizações constantes: A equipe da Offensive Security mantém o Kali Linux sempre atualizado com as ferramentas e as correções de segurança mais recentes.

O Kali Linux é de suma importância para o projeto porque permite a realização de testes de penetração e segurança de rede para estimular a geração de logs que será abordada mais a frente.

Para a instalação, acesse o site oficial do Kali Linux [aqui](https://www.kali.org/get-kali/#kali-platforms).

Escolha o download do Kali para o **VirtualBox** conforme a arquitetura.

![kali-linux](/screenshots/kali-linux.png)

Após o download, haverá um arquivo compactado que precisará ser extraído. Escolha qualquer local para extrair.

Se não puder extrair, instale o WinRar [aqui](https://www.win-rar.com/start.html?&L=9).

Após isso, uma pasta com dois arquivos é extraída. Clique duas vezes no arquivo que se parece com uma caixa azul para abrir o arquivo no VirtualBox(certifique-se de já ter instalado o VirtualBox).

A tela será algo parecido com isso, clique em iniciar e aguarde a inicialização.

![kalinoVB](/screenshots/kalinoVB.png)

Após aparecer a tela de início, faça o login com o usuário **kali** e senha **kali**.

### Ubuntu

O Ubuntu é uma distribuição Linux popular, conhecida por ser amigável ao usuário e amplamente utilizada para desktops, servidores e até dispositivos IoT. Ele é baseado no Debian e é mantido pela empresa britânica Canonical, que oferece suporte e atualizações de segurança regulares para a plataforma.

Características do Ubuntu

- Fácil de Usar:
    - O Ubuntu foi projetado para ser intuitivo e acessível para iniciantes em Linux, com uma interface gráfica amigável (chamada GNOME no Ubuntu padrão).
    - É bem documentado, e a comunidade de usuários é muito ativa, facilitando a resolução de dúvidas e problemas.

- Lançamentos Regulares:
    - LTS (Long Term Support): As versões LTS, lançadas a cada dois anos, recebem suporte e atualizações por cinco anos, tornando-as ideais para uso em servidores e ambientes de produção.
    - Intermediárias: Versões intermediárias são lançadas a cada seis meses, com suporte de nove meses, e geralmente trazem novos recursos e melhorias.

- Segurança e Suporte de Longo Prazo:
    - A Canonical fornece suporte e atualizações de segurança para o Ubuntu, e as versões LTS são uma escolha comum para servidores pela estabilidade e durabilidade.

Para a instalação, acesse o site oficial do Ubuntu [aqui](https://ubuntu.com/download/desktop).

Escolha a versão LTS para ter o SO mais atual.

Ao obter a ISO do Ubuntu, abra o VirtualBox e clique em **Novo**.

Dê um nome à VM.

No campo que pede a imagem a ser utilizada, escolha o caminho para a ISO do Ubuntu e marque a opção **Pular Instalação Desassistida**.

Abra a aba do Hardware e coloque estas configurações, para ter 2 CPUs e 4 GB de RAM. Após isso clique em finalizar.

![ubuntunovb](/screenshots/ubuntunovb.png)

Após isso, inicialize a VM do Ubuntu.

Haverá uma pequena inicialização em que será necessário criar uma conta com nome e senha. Crie do jeito que achar melhor.

### Metasploitable

O Metasploitable é uma máquina virtual vulnerável projetada para fins educacionais e de teste. Ele é usado principalmente por profissionais de segurança, estudantes e entusiastas para aprender e praticar testes de penetração e outras atividades relacionadas à segurança cibernética.

Características do Metasploitable

- Ambiente Seguro para Testes:
    - Ele é intencionalmente configurado com várias vulnerabilidades conhecidas em sistemas, serviços e softwares, oferecendo um ambiente seguro e controlado para prática.

- Variedade de Vulnerabilidades:
    - Inclui vulnerabilidades em serviços como FTP, SSH, HTTP, bancos de dados, e até sistemas operacionais.
    - Exemplos incluem credenciais padrão, injeção de SQL, vulnerabilidades no PHP, backdoors, entre outros.

- Compatível com Ferramentas de Segurança:
    - Foi projetado para ser explorado usando ferramentas como o Metasploit Framework, Nmap, Nikto, e outros.

**Importante**: O Metasploitable deve nunca ser conectado a uma rede pública ou exposto à internet. Ele foi projetado para ser usado exclusivamente em ambientes fechados, como laboratórios locais ou redes virtuais (homelabs). Sempre execute-o em um ambiente isolado, como em sua máquina virtual no VirtualBox, para evitar que suas vulnerabilidades sejam exploradas acidentalmente.

Para a instalação, acesse o site SourceForge [aqui](https://sourceforge.net/projects/metasploitable/files/Metasploitable2/) e clique em **metasploitable-linux-2.0.0.zip**. Após isso, aguarde aparecer o botão de download e clique nele.

Depois de feito o download, extraia o arquivo zip para gerar a pasta do metasploitable.

Abra o VirtualBox e clique em **Novo**. Siga a imagem abaixo, com foco em **escolher o caminho com a pasta certa que foi extraida**, colocando um nome, escolhendo o tipo **Linux**, e o Subtipo **Outro Linux**. Não há necessidade de alterar o Hardware. **Não finalize ainda**. O metasploitable não utiliza imagem porque o arquivo já vem com a máquina virtual já configurada(indicado pelo arquivo **.vmdk**) que será colocada na aba Disco Rígido.

![metasplnovb](/screenshots/metasplnovb.png)

Abra a aba Disco Rígido e clique na opção **Utilizar um disco rígido virtual existente**. Clique no ícone de pasta ao lado e depois em **Acrescentar**. Vá até a pasta do metasploitable e selecione o arquivo .vmdk que é simbolizado por um ícone de caixa azul. Após acrescentar, clique no disco e depois embaixo da janela em **Escolher**. Clique em finalizar.

![metasplnovb2](/screenshots/metasplnovb2.png)
