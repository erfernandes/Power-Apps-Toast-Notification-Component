# Power Apps Toast Notification Component
Componente criado para notificações estilo "Toast notification" para uso em aplicações do tipo Canvas.

## Conteúdo

- [Importando o componente](https://github.com/eduardoreisfernandes/Power-Apps-Toast-Notification-Component/blob/main/Importando%20o%20componente.md)
- [Propriedades de entrada](#propriedades-de-entrada)
- [Propriedades de saída](#propriedades-de-saída)

### Propriedades de entrada

| Nome de exibição | Propriedade | Descrição | Tipo de Dados | Default |
| - | - | - | - | - |
| Notification Width | NotificationWidth | Largura da notificação | Número | 300 |
| Notification Height | NotificationHeight | ALtura da notificação | Número | 80 |
| Duration (ms) | Duration | Tempo de exibição da notificação (em milissegundos) | Número | 2000 |
| Styles | Styles | Registro de estilização do componente (cores) | Registro | [ver](https://github.com/eduardoreisfernandes/Power-Apps-Toast-Notification-Component/blob/main/Importando%20o%20componente.md) |
| Icons | Icons | Ícones utilizados no componente (formato texto/svg) | Registro | [ver](https://github.com/eduardoreisfernandes/Power-Apps-Toast-Notification-Component/blob/main/Importando%20o%20componente.md) |
| Notification Message | NotificationMessage | Mensagem a ser exibida na notificação | Texto | "Your notification message" |
| Notification Type | NotificationType | Tipo da notificação a ser exibida (enum da propriedade de saída NotificationTypes) | Texto | 'Toast Notification'.NotificationTypes.Success |
| Font Size | FontSize | Tamanho da fonte da mensagem da notificação | Número | 9 |
| Font | Font | Tipo de fonte da mensagem da notificação (enum das fontes padrão) | Texto | Font.'Segoe UI' |
| Navigate to Screen When Notification Closes | NavigateToScreenWhenNotificationCloses | Tela de redirecionamento quando a notificação fechar | Tela | App.ActiveScreen |

### Propriedades de saída

| Nome de exibição | Propriedade | Descrição | Tipo de Dados | Default |
| - | - | - | - | - |
| Notification Types | NotificationTypes | Enum para ser usado na propriedade de entrada "Notification Type" | Registro | [ver](https://github.com/eduardoreisfernandes/Power-Apps-Toast-Notification-Component/blob/main/Importando%20o%20componente.md) |
| IsShowNotification | OutIsShowNotification | Propriedade com a variável que controla a exibição do componente | Booleano | IsVisible (variável interna do componente) |
| Out Notification Height | OutNotificationHeight | Propriedade que controla a altura do container do componente | Número | Max('Toast Notification'.NotificationHeight; lblNotificationMessage.Height + 43) |
