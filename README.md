# Power Apps Toast Notification Component
Componente criado para notificações estilo "Toast notification" para uso em aplicações do tipo Canvas.

![image](https://user-images.githubusercontent.com/47257185/183076234-093002a4-0d9d-4040-8727-87b202f202af.png)


## Conteúdo

- [Importando o componente](https://github.com/eduardoreisfernandes/Power-Apps-Toast-Notification-Component/blob/main/Importando%20o%20componente.md)
- [Propriedades de entrada](#propriedades-de-entrada)
- [Propriedades de saída](#propriedades-de-saída)
- [Configuração inicial](#configuração-inicial)

### Propriedades de entrada

| Nome de exibição | Propriedade | Descrição | Tipo de Dados | Default |
| - | - | - | - | - |
| Notification Width | NotificationWidth | Largura da notificação | Número | 300 |
| Notification Height | NotificationHeight | ALtura da notificação | Número | 80 |
| Duration (ms) | Duration | Tempo de exibição da notificação (em milissegundos) | Número | 2000 |
| Styles | Styles | Registro de estilização do componente (cores) | Registro | [ver registro](https://github.com/eduardoreisfernandes/Power-Apps-Toast-Notification-Component/blob/main/Registros/Styles.md) |
| Icons | Icons | Ícones utilizados no componente (formato texto/svg) | Registro | [ver registro](https://github.com/eduardoreisfernandes/Power-Apps-Toast-Notification-Component/blob/main/Registros/Icons.md) |
| Notification Message | NotificationMessage | Mensagem a ser exibida na notificação | Texto | "Your notification message" |
| Notification Type | NotificationType | Tipo da notificação a ser exibida (enum da propriedade de saída NotificationTypes) | Texto | 'Toast Notification'.NotificationTypes.Success |
| Font Size | FontSize | Tamanho da fonte da mensagem da notificação | Número | 9 |
| Font | Font | Tipo de fonte da mensagem da notificação (enum das fontes padrão) | Texto | Font.'Segoe UI' |
| Navigate to Screen When Notification Closes | NavigateToScreenWhenNotificationCloses | Tela de redirecionamento quando a notificação fechar | Tela | App.ActiveScreen |

### Propriedades de saída

| Nome de exibição | Propriedade | Descrição | Tipo de Dados | Default |
| - | - | - | - | - |
| Notification Types | NotificationTypes | Enum para ser usado na propriedade de entrada "Notification Type" | Registro | [ver registro](https://github.com/eduardoreisfernandes/Power-Apps-Toast-Notification-Component/blob/main/Registros/NotificationTypes.md) |
| IsShowNotification | OutIsShowNotification | Propriedade com a variável que controla a exibição do componente | Booleano | IsVisible (variável interna do componente) |
| Out Notification Height | OutNotificationHeight | Propriedade que controla a altura do container do componente | Número | Max('Toast Notification'.NotificationHeight; lblNotificationMessage.Height + 43) |

### Configuração inicial

1. O componente inicialmente deverá ficar oculto até ser acionado no momento da notificação. Para isso, navegue até a propriedade **_Visible_** e coloque o valor 
```
Self.OutIsShowNotification
```
![image](https://user-images.githubusercontent.com/47257185/182984850-70c5eba9-f118-43d3-9583-f217f98c91cc.png)

2. Configure as propriedades como desejar. As principais são:
  - **Notification Width:** controla a largura do componente. Por padrão vem com valor **_300_**.
  - **Notification Height:** controla a altura do componente. Por padrão vem com valor **_80_**. **OBS.: a altura do componente é automática, se ajustando conforme o tamanho do texto, caso este seja maior que a altura padrão definida**.
  - **Duration (ms):** controla o tempo que a notificação é exibida em tela. Por padrão vem com valor **_2000_**. Este valor é em milissegundos.
  - **Notification Message:** é a mensagem a ser exibida no componente.
  - **Notification Type:** é o tipo de notificação a ser exibido. Esse parâmetro vai definir as cores e os ícones exibidos com o componente. Por padrão vem com valor **_'Toast Notification'.NotificationTypes.Success_**, onde **_'Toast Notification'_** é o nome do componente na árvore de elementos da tela. **OBS.: esse valor é baseado num Enum que é referenciado através de uma _propriedade de saída_ chamada _NotificationTypes_**.
  - **Navigate to Screen When Notification Closes:** é a tela para onde o usuário será redirecionado quando a exibição do componente finalizar. **OBS.: caso você queira permanecer na mesma tela, basta manter o padrão configurado que é _App.ActiveScreen_**.

3. O componente de notificação é acionado quando ele é resetado. Para exibir, execute o comando:
```
Reset('Toast Notification')
```

![image](https://user-images.githubusercontent.com/47257185/182986541-77994ac4-975c-4103-b426-b767ac21d284.png)

4. O ícone ![image](https://user-images.githubusercontent.com/47257185/182986637-97694a24-d56e-4716-b0c2-a396bd4781b4.png) apenas fecha o componente antes da duração configurada. Clicando nele, o usuário **não** será redirecionado.


