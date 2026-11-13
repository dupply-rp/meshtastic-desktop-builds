# Guia de instalação do Meshtastic Desktop

Rascunho. Os textos marcados com [CONFIRMAR] e as capturas marcadas com [CAPTURA] dependem do teste em máquina real.

## Antes de começar

Você vai receber um link para uma página com vários arquivos. Baixe apenas o arquivo do seu sistema:

| Seu computador | Arquivo para baixar |
| --- | --- |
| Windows 10 ou 11 | o que termina em `.msi` |
| Mac com chip Apple (M1, M2, M3, M4) | o que termina em `.dmg` |
| Linux Ubuntu ou Debian | o que termina em `.deb` |
| Linux Fedora | o que termina em `.rpm` |
| Outro Linux | o que termina em `.AppImage` |

O programa é o Meshtastic oficial, sem nenhuma alteração. Como ele não tem assinatura digital paga, o computador vai mostrar um aviso de segurança na primeira vez. Isso é normal e o guia mostra como passar por ele.

## Windows

1. Dê dois cliques no arquivo `.msi` que você baixou.
2. Vai aparecer uma tela azul dizendo "O Windows protegeu o computador". [CAPTURA]
3. Clique em **Mais informações**. [CAPTURA]
4. Clique em **Executar assim mesmo**. [CAPTURA]
5. Siga as telas do instalador clicando em **Avançar** até terminar. [CAPTURA] [CONFIRMAR]
6. Abra o **Meshtastic Desktop** pelo menu Iniciar.

Se o antivírus bloquear o arquivo, ele pode ser liberado na própria tela do antivírus. [CONFIRMAR]

## Mac

1. Dê dois cliques no arquivo `.dmg` que você baixou.
2. Arraste o ícone do Meshtastic Desktop para a pasta **Aplicativos**. [CAPTURA]
3. Abra a pasta Aplicativos e dê dois cliques no Meshtastic Desktop.
4. O Mac vai avisar que não pode verificar o programa. Clique em **OK**. [CAPTURA] [CONFIRMAR]
5. Abra **Ajustes do Sistema**, depois **Privacidade e Segurança**.
6. Desça a tela até a mensagem sobre o Meshtastic Desktop e clique em **Abrir Mesmo Assim**. [CAPTURA]
7. Digite a senha do Mac, se pedir, e confirme em **Abrir**.

Se o Mac disser que o programa "está danificado", abra o aplicativo **Terminal**, cole a linha abaixo e aperte Enter:

```
xattr -dr com.apple.quarantine "/Applications/Meshtastic Desktop.app"
```

Depois disso, abra o programa normalmente. [CONFIRMAR qual mensagem aparece]

## Linux

**Ubuntu ou Debian:** dê dois cliques no arquivo `.deb` e clique em **Instalar**. [CAPTURA]

**Fedora:** dê dois cliques no arquivo `.rpm` e clique em **Instalar**.

**Outros:** clique com o botão direito no arquivo `.AppImage`, abra **Propriedades**, marque **Permitir executar como programa** e depois dê dois cliques nele. [CAPTURA]

## Primeira conexão com o rádio

1. Ligue o rádio no computador pelo cabo USB.
2. Abra o Meshtastic Desktop.
3. Na tela de conexão, escolha a porta USB do rádio. [CAPTURA] [CONFIRMAR nome do menu]
4. Aguarde a lista de nós aparecer.

## Aviso de mensagem na tela

Quando chega uma mensagem, o programa mostra um aviso no canto da tela. Para o aviso ficar mais tempo visível:

**Windows:** abra Configurações, Acessibilidade, Efeitos visuais, e em "Ignorar notificações após este período" escolha **5 minutos**. As mensagens também ficam guardadas na Central de Notificações, no canto inferior direito. [CONFIRMAR]

**Mac:** abra Ajustes do Sistema, Notificações, Meshtastic Desktop, e escolha o estilo **Alertas**. Assim o aviso fica na tela até você fechar. [CONFIRMAR]

## Quando aparecer "versão nova"

O programa avisa quando o projeto oficial lança uma versão nova. Quando isso acontecer, é só pedir para a Dupply que enviamos o novo instalador.
