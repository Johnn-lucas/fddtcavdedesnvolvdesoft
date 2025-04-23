# fddtcavdedesnvolvdesoft
💬 Fórum de Discussão do Módulo 3 - Desenvolvimento baseado em componentes


Componente de Estoque (Sujeito)
O Componente de Estoque é o sujeito que é observado pelos outros componentes. Ele tem as seguintes características:
observers: uma lista de observadores que estão registrados para receber notificações.
adicionarObserver: um método que permite adicionar um novo observador à lista.
removerObserver: um método que permite remover um observador da lista.
notificarObservers: um método que notifica todos os observadores registrados.
atualizarEstoque: um método que atualiza o estoque de um produto e notifica os observadores se o estoque atingir um nível crítico.

Componente de Notificação (Observador)
O Componente de Notificação é o observador que está registrado para receber notificações do Componente de Estoque. Ele tem as seguintes características:
estoque: uma referência ao Componente de Estoque que está sendo observado.
notificar: um método que é chamado quando o Componente de Estoque notifica os observadores.

Funcionamento
Aqui está como o exemplo funciona:
O Componente de Estoque é criado e inicializado com uma lista de produtos.
O Componente de Notificação é criado e registrado como observador do Componente de Estoque.
Quando o estoque de um produto é atualizado, o Componente de Estoque verifica se o estoque atingiu um nível crítico (neste caso, 5 ou menos unidades).
Se o estoque atingiu um nível crítico, o Componente de Estoque notifica todos os observadores registrados, incluindo o Componente de Notificação.
O Componente de Notificação recebe a notificação e envia uma notificação para os usuários.

Vantagens
O padrão Observer oferece várias vantagens, incluindo:
Desacoplamento: o Componente de Estoque e o Componente de Notificação estão desacoplados, o que significa que mudanças em um componente não afetam diretamente o outro.
Flexibilidade: é fácil adicionar ou remover observadores, o que permite que o sistema seja escalado e adaptado às necessidades.
Reutilização: o Componente de Notificação pode ser reutilizado em outros contextos, desde que seja registrado como observador de outro sujeito
