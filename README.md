## 🧠 O que estou aprendendo com o estudo de Flutter?

### 1. Fundamentos do Framework & Dart
* **Manipulação de Estados:** Compreender a diferença prática e o ciclo de vida de `StatelessWidget` e `StatefulWidget`.
* **Consumo de APIs assíncronas:** Utilizar `Future`, `Stream` e programação assíncrona (`async/await`) para lidar com dados externos e requisições HTTP.
* **Lógica de Programação com Dart:** Aplicação de POO (Programação Orientada a Objetos), coleções (Listas, Mapas) e controle de fluxo avançado.

### 2. UI/UX & Design System (Figma to Code)
* **Componentização:** Como quebrar telas complexas em micro-widgets reutilizáveis, mantendo o código limpo e legível.
* **Estilização Avançada:** Implementação de layouts complexos usando `Flexbox` (Rows/Columns), gerenciamento de cores (HEX/RGB), gradientes personalizados e transições fluidas.
* **Responsividade:** Adaptar a interface para diferentes tamanhos de tela e densidades de pixels.

### 3. Arquitetura & Gerenciamento de Estado
* **Padrões de Projetos:** Organização do código seguindo boas práticas de mercado (como *Clean Architecture* ou *MVVM*), separando a lógica de negócio da camada de apresentação (UI).
* **Gerenciamento de Estado Profissional:** Implementação de ferramentas para gerenciar o estado global da aplicação (ex: *Bloc, Provider, Riverpod ou GetX*).
* **Injeção de Dependências:** Desacoplamento de código e gerenciamento de instâncias de forma eficiente.

---

## 🛠️ Tecnologias e Conceitos Praticados

* **Linguagem:** Dart 3.x
* **Framework:** Flutter 3.x
* **Persistência de Dados Local:** *(Ex: Shared Preferences, Hive ou SQLite)*
* **Ferramenta de Design de Apoio:** Figma (para o mapeamento de jornadas e prototipagem)

---

## 📂 Estrutura de Pastas do Aprendizado

A estrutura foi desenhada para separar as responsabilidades e facilitar a manutenção do código à medida que o app cresce:

```text
lib/
│
├── core/                  # Tudo o que é compartilhado (Temas, Cores, Utilitários)
│   ├── theme/             # Paleta de cores, tipografia e estilos visuais
│   └── utils/             # Funções utilitárias e constantes
│
├── data/                  # Camada de Dados (Modelos de dados e chamadas de API)
│   ├── models/            # Conversão de JSON para objetos Dart
│   └── repositories/      # Implementação da busca de dados
│
└── presentation/          # Camada de Interface (O que o usuário vê)
    ├── screens/           # Telas completas do fluxo do app
    └── widgets/           # Componentes visuais menores e reutilizáveis
