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

Para a instalação, acesse o site oficial do Kali Linux [aqui](https://www.kali.org/get-kali/#kali-platforms)

Escolha o download do Kali para o **VirtualBox** conforme a arquitetura.

![kali-linux](/screenshots/kali-linux.png)

Após o download, haverá um arquivo compactado que precisará ser extraído. Escolha qualquer local para extrair.

Se não puder extrair, instale o WinRar [aqui](https://www.win-rar.com/start.html?&L=9)

Após isso, uma pasta com dois arquivos é extraída. Clique duas vezes no arquivo que se parece com uma caixa azul para abrir o arquivo no VirtualBox(Certifique-se de já ter instalado o VirtualBox).

A tela será algo parecido com isso, clique em iniciar e aguarde a inicialização.

Após aparecer a tela de início, faça o login com o usuário **kali** e senha **kali** e pronto. 
