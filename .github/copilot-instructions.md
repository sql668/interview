# Copilot Instructions for Interview Knowledge Repository

## Project Overview
This is an interview preparation knowledge repository organized by topics (JavaScript, React, Vue, TypeScript, CSS, HTML, Network, Algorithms, Design Patterns, etc.). It contains curated learning materials, code examples, and practical implementations for interview preparation.

## Directory Structure & Patterns

### Core Knowledge Areas
- **js/** - JavaScript fundamentals, async patterns, hand-written implementations (Promise, instanceof, deepClone)
- **案例/** (Examples) - Practical implementations:
  - `订阅发布/` - Pub/Sub pattern with message queues, history replay, ACK mechanisms
  - `文档中心/` - Icon font management with iconfont.js assets
  - `async-await/` - Modern async/await examples
- **demo/** - Cross-browser communication patterns (SharedWorker, Service Worker, IndexedDB, LocalStorage, BroadcastChannel)
- **场景演练/** (Scenarios) - Real-world patterns (design patterns, file uploads, forms, watermarks, virtual scrolling)
- **高频面试300问/** - Common interview Q&A organized by language
- **test/** - Implementation tests (Promise, KMP algorithm, utilities)

### Content Format Convention
- Markdown files (`.md`) contain:
  - Conceptual explanations with examples
  - Code snippets embedded in triple-backtick blocks
  - Use `js`, `ts`, `html`, `css`, `go` language tags for code blocks
- Standalone JavaScript files contain:
  - Class implementations (e.g., PubSub, MyPromise)
  - Utility functions and helpers
  - Often used for testing and demonstration

## Key Implementation Patterns

### 1. Pub/Sub Pattern Implementation
[案例/订阅发布/pubsub.js](案例/订阅发布/pubsub.js) demonstrates:
- Topic-based message routing with Map storage
- History replay with configurable limits
- Subscriber lifecycle management (ID generation, registration)
- Global config + per-topic config override pattern
- Acknowledgment callbacks for async operations

### 2. Promise Implementation
[js/手写代码/promise/promise.js](js/手写代码/promise/promise.js) shows:
- Private field usage (#) for state isolation
- Microtask queueing for async resolution
- State machine pattern (PENDING → FULFILLED/REJECTED - immutable)
- Thenable detection and chaining
- Error handling within executor and callbacks

### 3. Cross-Tab Communication
[demo/cross-tab-communication/](demo/cross-tab-communication/) illustrates multiple patterns:
- **SharedWorker** - For persistent, shared state across tabs
- **Service Worker** - For background processing and caching
- **BroadcastChannel** - For simple pub/sub between tabs
- Each pattern isolated in separate files for comparison

### 4. Design Pattern Examples
[场景演练/设计模式.md](场景演练/设计模式.md) documents:
- **Strategy Pattern** - Object mapping to eliminate if-else chains
- **Form validation patterns** - Mini validator implementations
- Practical refactoring examples showing before/after

## Common Workflows

### Adding New Interview Topics
1. Create new `.md` file in appropriate language folder (js/, css/, html/, etc.)
2. Use template: Problem statement → Code example → Explanation
3. Include code blocks with language tags for syntax highlighting
4. Cross-reference related patterns in other sections

### Testing Implementations
- Run tests via `npm test` (currently echo placeholder)
- Test files in [test/](test/) can be run with Node.js directly
- Promise tests: `node test/promise.js`
- Algorithm tests: `node test/kmp.js`

### Code Examples in Documentation
- Always wrap implementations in markdown code blocks with language tag
- Provide context comments explaining the "why" not just "what"
- Link to practical use cases in [案例/](案例/) or [demo/](demo/)

## Dependencies & External Libraries
- **bluebird** - Promise utilities (for learning Promise patterns)
- **p-limit** - Concurrency control (demonstrated in `js/异步专题.md`)
- No build process - files run directly in Node/Browser environments

## Important Conventions

### Naming Patterns
- Private class fields use `#` prefix (not underscore)
- Test utilities use `util.` prefix pattern (util.db.js, util.shared.js)
- Subscriber IDs: `sub-{timestamp}-{random}` format for uniqueness

### State Management in Classes
- Use immutable state transitions (state machine pattern)
- Store callbacks in Map structures for O(1) lookup
- Implement internal `#` methods for complex logic isolation

### Async Pattern Preferences
- Favor `async/await` over promise chains for readability
- Demonstrate callback-based patterns for learning purposes
- Show concurrent control techniques (p-limit, manual queue management)

## Areas to Avoid
- Do not suggest adding automated tests/CI - not part of project scope
- Do not recommend large refactoring of organizational structure
- Focus on explaining existing patterns, not reshaping them
- Avoid overfitting to modern best practices - this is a learning repository with historical implementations
