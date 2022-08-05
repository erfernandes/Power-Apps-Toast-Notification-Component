# Power Apps Toast Notification Component
Componente criado para notificações estilo "Toast notification" para uso em aplicações do tipo Canvas.

## Conteúdo

- [Importando o componente](https://github.com/eduardoreisfernandes/Power-Apps-Toast-Notification-Component/blob/main/Importando%20o%20componente.md)
- [Propriedades de entrada](#propriedades-de-entrada)
- [Propriedades de saída](#propriedades-de-saída)

### Propriedades de entrada

| Nome de exibição | Propriedade | Descrição | Tipo de Dados | Default |
| - | - | - | - | - | - |
| Notification Width | NotificationWidth | Largura da notificação | Número | 300 |
| Notification Height | NotificationHeight | ALtura da notificação | Número | 80 |
| Duration (ms) | Duration | Tempo de exibição da notificação (em milissegundos) | Número | 2000 |
| Styles | Styles | Registro de estilização do componente (cores) | Registro | [ver](https://github.com/eduardoreisfernandes/Power-Apps-Toast-Notification-Component/blob/main/Importando%20o%20componente.md) |

### Propriedades de saída

| Nome de exibição | Propriedade | Descrição | Tipo de Dados | Default |
| - | - | - | - | - |
| Notification Types | NotificationTypes | Enum para ser usado na propriedade de entrada "Notification Type" | Registro | [ver](https://github.com/eduardoreisfernandes/Power-Apps-Toast-Notification-Component/blob/main/Importando%20o%20componente.md) |
| IsShowNotification | OutIsShowNotification | Propriedade com a variável que controla a exibição do componente | Booleano | IsVisible (variável interna do componente) |
| Out Notification Height | OutNotificationHeight | Propriedade que controla a altura do container do componente | Número | Max('Toast Notification'.NotificationHeight; lblNotificationMessage.Height + 43) |
