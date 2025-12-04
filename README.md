# Roadmap de Estudos - React

## 1. Fundamentos JavaScript

### 1.1 Revisão de Conceitos Essenciais
- **Manipulação de strings**: Métodos como toUpperCase(), toLowerCase(), trim(), split() - essenciais para processamento de texto
- **Métodos de arrays**: filter(), map(), reduce() - fundamentais para transformação de dados no React
- **Filtragem de arrays e objetos**: Técnicas para buscar e filtrar dados baseados em condições - usado constantemente em renderização de listas

### 1.2 Closures
- **Conceito de closures**: Funções que "lembram" do escopo onde foram criadas - crucial para entender hooks
- **Aplicação prática**: Como closures afetam event handlers e callbacks no React
- **Escopo léxico**: Entender como variáveis são capturadas e mantidas em memória

### 1.3 Desestruturação
- **Desestruturação de arrays**: Extrair valores de arrays de forma concisa `const [a, b] = array`
- **Desestruturação de objetos**: Extrair propriedades `const {name, age} = user`
- **Desestruturação avançada**: Valores padrão, renomeação, nested destructuring
- **Desestruturação em funções**: Parâmetros de função desestruturados - padrão comum em props

## 2. Introdução ao React

### 2.1 Conceitos Fundamentais
- **O que é React?**: Biblioteca JavaScript para construir interfaces de usuário declarativas e baseadas em componentes
- **React vs JavaScript puro**: Comparação entre manipulação direta do DOM e abordagem declarativa
- **Versão do React**: Entender diferenças entre versões e breaking changes importantes
- **Paradigma declarativo**: Descrever "o que" queremos ver, não "como" manipular o DOM

### 2.2 Instalação e Configuração
- **Configuração do ambiente**: Node.js, npm/yarn, editor de código
- **Estrutura de projetos**: Organização de pastas e arquivos
- **Bundlers e transpilers**: Papel do Babel e Webpack/Vite no ecossistema

## 3. DOM e React

### 3.1 Document API
- **Document.createElement**: Método tradicional para criar elementos no DOM
- **Manipulação do DOM tradicional**: appendChild, innerHTML, setAttribute - entender para comparar com React
- **Limitações da abordagem imperativa**: Por que manipulação direta é complexa em apps grandes

### 3.2 React.createElement
- **Sintaxe e utilização**: `React.createElement(type, props, children)` - fundação do React
- **React Elements**: Objetos JavaScript que descrevem elementos da UI
- **Diferenças entre DOM e React Elements**: React elements são leves e imutáveis
- **Virtual DOM**: Conceito de representação em memória da UI

### 3.3 ReactDOM
- **Introdução ao ReactDOM**: Biblioteca para renderizar React na web
- **Renderização de elementos**: `ReactDOM.render()` ou `createRoot().render()` (React 18+)
- **Elemento Root**: Ponto de montagem da aplicação no HTML
- **Reconciliation**: Como React atualiza o DOM de forma eficiente

## 4. JSX Básico

### 4.1 Fundamentos do JSX
- **O que é JSX?**: Extensão de sintaxe que parece HTML mas é JavaScript
- **Sintaxe básica**: Regras de escrita, diferenças com HTML
- **Tags de fechamento automático**: `<img />`, `<input />` - obrigatório no JSX
- **Transpilação**: Como JSX é convertido para React.createElement

### 4.2 Atributos em JSX
- **Atributos estáticos**: Valores fixos passados para elementos
- **Atributos dinâmicos**: Usar {} para valores JavaScript
- **Classes e estilos**: className vs class, style como objeto
- **Diferenças de nomenclatura**: camelCase (onClick, onChange) vs HTML tradicional

### 4.3 Expressões JSX
- **Interpolação de variáveis**: Usar {variavel} para inserir valores dinâmicos
- **Expressões JavaScript**: Qualquer expressão JS válida dentro de {}
- **Expressões em atributos**: `src={url}`, `className={classe}`
- **Operadores**: Ternários, lógicos, aritméticos dentro de JSX

### 4.4 Estrutura do JSX
- **Elementos filhos**: Aninhamento de elementos, children
- **Fragmentos JSX**: `<>...</>` ou `<Fragment>` para agrupar sem div extra
- **Aninhamento de elementos**: Hierarquia e composição de componentes
- **Whitespace e formatação**: Como espaços e quebras de linha são tratados

### 4.5 Pegadinhas do JSX
- **Diferenças entre HTML e JSX**: class → className, for → htmlFor
- **Nomenclatura de atributos**: camelCase obrigatório
- **Casos especiais**: Comentários em JSX, return de múltiplos elementos
- **Reserved words**: Evitar palavras reservadas do JavaScript

## 5. Componentes

### 5.1 Conceitos de Componentes
- **Introdução aos componentes**: Blocos de construção reutilizáveis da UI
- **Anatomia de um componente**: Estrutura, props, retorno de JSX
- **Componentes como funções**: Function components - padrão moderno do React
- **Composição**: Construir UIs complexas combinando componentes simples

### 5.2 Organização de Componentes
- **Um componente por arquivo**: Convenção para manutenibilidade
- **Múltiplos componentes**: Quando usar vários componentes em um arquivo
- **Estrutura de pastas**: Organização por feature, por tipo, ou híbrida
- **Naming conventions**: PascalCase para componentes, camelCase para funções auxiliares

### 5.3 Props
- **Passagem de props**: Passar dados de pai para filho
- **Props.children**: Conteúdo aninhado entre tags de abertura e fechamento
- **Desestruturação de props**: `function Button({ text, onClick })` - padrão comum
- **Spread de props**: `{...props}` para passar múltiplas props
- **Valores padrão**: defaultProps ou parâmetros padrão

### 5.4 Funções Puras
- **Conceito de funções puras**: Mesma entrada → mesma saída, sem side effects
- **Componentes puros**: Não modificam variáveis externas, previsíveis
- **Boas práticas**: Evitar mutações, manter componentes determinísticos
- **Benefícios**: Testabilidade, previsibilidade, otimização do React

## 6. JSX Avançado

### 6.1 Renderização Condicional
- **Operadores ternários**: `{condition ? <A /> : <B />}` - escolha entre dois elementos
- **Operador lógico &&**: `{condition && <Component />}` - renderizar ou não
- **Renderização condicional complexa**: Múltiplas condições, switch statements
- **Early returns**: Retornar null ou elementos diferentes baseado em condições

### 6.2 Classes Condicionais
- **Classes dinâmicas**: Adicionar/remover classes baseado em estado
- **Biblioteca clsx**: Utilitário para construir strings de className condicionalmente
- **Gerenciamento de classes**: Combinar classes estáticas e dinâmicas
- **Template literals**: Alternativa para concatenar classes

## 7. Listas e Renderização

### 7.1 Renderização de Arrays
- **Arrays em JSX**: Usar map() para renderizar listas de elementos
- **Método map()**: Transformar array de dados em array de componentes
- **Propriedade key**: Identificador único para cada elemento - crucial para performance
- **Por que keys são importantes**: Reconciliation eficiente, manter estado correto

### 7.2 Imutabilidade de Arrays
- **Conceito de imutabilidade**: Não modificar dados originais, criar novos
- **Adição imutável**: `[...array, newItem]` ou `array.concat(newItem)`
- **Atualização imutável**: `array.map(item => item.id === id ? updated : item)`
- **Remoção imutável**: `array.filter(item => item.id !== id)`
- **Métodos mutáveis vs imutáveis**: push/pop/splice vs concat/slice/map/filter

## 8. State e Hooks

### 8.1 Introdução ao State
- **Conceito de state**: Dados que mudam ao longo do tempo e causam re-renderização
- **useState hook**: `const [state, setState] = useState(initialValue)`
- **Importação de hooks**: `import { useState } from 'react'`
- **Regras dos hooks**: Chamá-los no top level, apenas em componentes/hooks

### 8.2 Mudança de State
- **Função set do useState**: Atualizar estado e triggar re-render
- **Estado anterior**: Acessar valor anterior para calcular novo valor
- **Desmembramento do useState**: Entender o array retornado `[valor, função]`
- **Batching de atualizações**: React agrupa múltiplas atualizações

### 8.3 State com Events
- **Event handlers**: Funções que respondem a interações do usuário
- **Manipuladores nomeados**: `onClick={handleClick}` - boa prática para legibilidade
- **Events, State e Closures**: Como closures capturam valores de estado
- **Synthetic events**: Sistema de eventos cross-browser do React

### 8.4 Mudança de Estado Condicional
- **Atualizações condicionais**: Atualizar state apenas sob certas condições
- **Mudança com base em props**: Derivar estado de props quando apropriado
- **Validações de estado**: Verificar condições antes de atualizar
- **Guards**: Prevenir atualizações inválidas

### 8.5 Múltiplos States
- **Gerenciamento de múltiplos states**: Quando usar múltiplos useState vs objeto único
- **Regras dos hooks**: Ordem consistente de chamadas de hooks
- **Estados relacionados**: Quando agrupar em objeto vs separar
- **Performance**: Múltiplas atualizações e re-renders

## 9. Imutabilidade Avançada

### 9.1 Conceitos de Imutabilidade
- **Arrays e objetos**: Estruturas de dados mutáveis em JavaScript
- **Mutações e suas consequências**: Por que mutações causam bugs no React
- **Por que React requer imutabilidade**: Comparação rasa para detectar mudanças
- **Referências vs valores**: Entender igualdade de referência

### 9.2 State de Arrays
- **Gerenciamento de listas**: Padrões para trabalhar com arrays no state
- **Adicionar itens**: Spread operator, concat
- **Remover itens**: filter
- **Atualizar itens**: map para criar novo array com item modificado
- **Reordenar**: Criar novo array com ordem diferente

### 9.3 Imutabilidade de Objetos
- **Adicionar e substituir propriedades**: `{...obj, newProp: value}`
- **Remover pares chave/valor**: Destructuring com rest operator
- **Spread operator em objetos**: Copiar e modificar objetos
- **Nested updates**: Atualizar objetos aninhados mantendo imutabilidade
- **Immer library**: Alternativa para facilitar atualizações imutáveis

### 9.4 State de Objetos
- **Gerenciamento de objetos complexos**: State com múltiplas propriedades
- **Atualização de propriedades aninhadas**: Spread em múltiplos níveis
- **Boas práticas**: Quando usar objeto único vs múltiplos states
- **Normalização de dados**: Estruturar state para facilitar atualizações

## 10. Kit de UI e Boas Práticas

### 10.1 Componentização
- **Criação de biblioteca de componentes**: Design system básico
- **Componentes reutilizáveis**: Botões, inputs, cards genéricos
- **Padrões de design**: Composition, render props, compound components
- **API de componentes**: Props bem definidas e documentadas

### 10.2 Interface do Usuário
- **Composição de componentes**: Combinar componentes para criar interfaces complexas
- **Temas (claro/escuro)**: Implementar sistema de temas
- **Acessibilidade básica**: ARIA labels, keyboard navigation
- **Responsive design**: Componentes que se adaptam a diferentes telas

## 11. Formulários

### 11.1 Formulários Básicos
- **Valor padrão de inputs**: defaultValue vs value
- **Captura de valores**: event.target.value para pegar input do usuário
- **Event handlers em formulários**: onChange, onSubmit, onBlur
- **Uncontrolled inputs**: Inputs sem state (usar refs)

### 11.2 Componentes Controlados
- **Conceito de componentes controlados**: Input cujo valor é controlado por state
- **Inputs controlados**: `<input value={state} onChange={handler} />`
- **Sincronização de state com inputs**: State como source of truth
- **Two-way binding**: Estado sincronizado com valor do input
- **Validação em tempo real**: Validar enquanto usuário digita

### 11.3 Envio de Formulários
- **Manipulação de submit**: event.preventDefault() para evitar reload da página
- **Prevenção de comportamento padrão**: Controlar envio do formulário
- **Processamento de dados**: Coletar e validar dados antes de enviar
- **Reset de formulário**: Limpar campos após envio
- **Loading states**: Mostrar feedback durante envio

### 11.4 Acessibilidade em Formulários
- **O que é acessibilidade**: Tornar formulários usáveis para todos
- **Labels e inputs**: Associar labels com inputs corretamente
- **Formulários acessíveis**: ARIA attributes, error messages, focus management
- **Boas práticas**: Keyboard navigation, mensagens de erro claras
- **Screen readers**: Garantir que formulários sejam navegáveis por leitores de tela

## 12. Arquitetura de Projetos React

### 12.1 Ferramentas de Build
- **Create React App vs Vite**: Comparação de ferramentas de setup
- **Scripts de desenvolvimento e produção**: npm start, npm run build
- **Estrutura de arquivos**: src/, public/, package.json
- **Ambiente de desenvolvimento vs produção**: Diferenças de otimização e debugging
- **Hot Module Replacement**: Atualização instantânea durante desenvolvimento

### 12.2 React DevTools
- **Ferramentas de desenvolvimento**: Extensão do navegador para inspecionar React
- **Inspeção de componentes**: Ver props, state, hierarquia de componentes
- **Profiler de performance**: Identificar componentes lentos e re-renders desnecessários
- **Time travel debugging**: Ver histórico de mudanças de state

## 13. Comunicação entre Componentes

### 13.1 Componentes com e sem Estado
- **Stateless components**: Componentes que apenas recebem props e renderizam
- **Stateful components**: Componentes que gerenciam state
- **Quando usar cada tipo**: Separação de responsabilidades
- **Presentational vs Container**: Padrão de design para organizar componentes

### 13.2 Passagem de Funções
- **Funções como props**: Passar comportamento de pai para filho
- **Callback functions**: Filho notifica pai sobre eventos
- **Chamada de funções passadas**: Invocar funções recebidas via props
- **Event bubbling**: Propagar eventos através da árvore de componentes

### 13.3 Elevação de Estado
- **Conceito de lifting state up**: Mover state para componente pai comum
- **Compartilhamento de estado**: Múltiplos componentes acessando mesmo estado
- **Gerenciamento de estado entre componentes**: Coordenar estado entre siblings
- **Estado centralizado**: Quando e como centralizar state na árvore
- **Single source of truth**: Um lugar para cada pedaço de estado

### 13.4 Refatoração de Componentes
- **Divisão de componentes**: Quebrar componentes grandes em menores
- **Extração de lógica**: Separar lógica de negócio de apresentação
- **Melhoria de estrutura**: Reorganizar para melhor manutenibilidade
- **Responsabilidades únicas**: Cada componente deve ter um propósito claro
- **DRY (Don't Repeat Yourself)**: Identificar e eliminar duplicação

## 14. State Avançado

### 14.1 Atualizações Funcionais de State
- **Atualizações assíncronas de estado**: Entenda como o React processa atualizações de estado de forma assíncrona e batch updates
- **Functional updates**: Use funções callback no setState para garantir acesso ao estado mais recente
- **Uso de função no setState**: Padrão `setState(prevState => newState)` para atualizações baseadas no estado anterior
- **Garantia de estado mais recente**: Evite bugs causados por closures e estado desatualizado

## 15. Effects e Side Effects

### 15.1 Introdução ao useEffect
- **Conceito de side effects**: Operações que afetam o mundo externo ao componente (API calls, timers, DOM manipulation)
- **Sintaxe do useEffect**: Estrutura básica `useEffect(() => {}, [])`
- **Execução do effect**: Quando e como os effects são executados no ciclo de vida
- **Mode de desenvolvimento**: Comportamento diferente em dev mode (strict mode executa effects duas vezes)
- **Casos de uso comuns**: Atualização de título da página, logs, sincronização com sistemas externos

### 15.2 Cleanup de Effects
- **Função de cleanup**: Retornar uma função do effect para limpar recursos
- **Quando fazer cleanup**: Event listeners, timers, subscriptions, conexões
- **Prevenção de memory leaks**: Identificar e corrigir vazamentos de memória
- **Padrão de cleanup**: `useEffect(() => { /* setup */; return () => { /* cleanup */ }; }, [])`
- **Componentes desmontados**: Limpeza quando componente sai da tela

### 15.3 Array de Dependências
- **Conceito de dependências**: Variáveis que o effect "observa" para re-executar
- **Array vazio []**: Effect executa apenas uma vez (mount)
- **Sem array**: Effect executa em toda renderização (evitar)
- **Com dependências**: Effect executa quando dependências mudam
- **Regras de dependências**: Incluir todas as variáveis usadas dentro do effect
- **ESLint e exhaustive-deps**: Ferramenta para garantir dependências corretas

### 15.4 Ciclo de Vida com Effects
- **Montagem (mount)**: Effect executa após primeira renderização
- **Atualização (update)**: Effect re-executa quando dependências mudam
- **Desmontagem (unmount)**: Cleanup executa antes de componente desmontar
- **Comparação com class components**: componentDidMount, componentDidUpdate, componentWillUnmount
- **Mental model**: Pensar em sincronização, não em ciclo de vida

## 16. Padrões Avançados com Effects

### 16.1 Effects e State Combinados
- **Mudança de estado dentro de effects**: Quando e como atualizar state em effects
- **Evitar loops infinitos**: Estado como dependência que é atualizado no effect
- **Flags e condicionais**: Usar variáveis de controle para evitar re-execuções desnecessárias
- **Timers e intervals**: setInterval, setTimeout com state e cleanup
- **Sincronização de dados**: Buscar dados quando estado muda

### 16.2 Effects com Events
- **Event listeners em effects**: Adicionar e remover listeners corretamente
- **Combinação effect + state + events**: Padrões complexos de interação
- **Scroll, resize, keyboard events**: Casos de uso comuns
- **Debounce e throttle**: Otimização de event handlers custosos
- **Referências atualizadas**: Garantir que event handlers usem state mais recente

### 16.3 Performance de Effects
- **Otimização de execução**: Evitar re-execuções desnecessárias
- **Dependências pesadas**: Como lidar com objetos e arrays como dependências
- **useMemo e useCallback**: Memoização para otimizar dependências
- **Profiling de effects**: Identificar effects que causam problemas de performance
- **Boas práticas**: Manter effects simples e focados, dividir effects grandes

### 16.4 Integração com APIs Externas
- **Bibliotecas externas**: Integração com libs de terceiros (mapas, charts, etc)
- **Lifecycle de bibliotecas**: Inicialização e destruição de instâncias externas
- **Refs para DOM**: Usar useRef para acessar elementos DOM em effects
- **Sincronização bidirecional**: Manter React e biblioteca externa sincronizados
- **Error handling**: Tratamento de erros em operações assíncronas
