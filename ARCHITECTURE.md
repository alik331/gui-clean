# Architecture Overview

This document provides a high-level overview of the Moorph GUI Clean architecture, designed to help developers understand the codebase structure and key components.

## Technology Stack

- **Frontend**: React 18 + TypeScript + Vite
- **3D Engine**: Babylon.js for WebGL rendering
- **State Management**: Zustand for global state
- **AI Integration**: OpenAI API for natural language processing
- **Styling**: Modern CSS with custom design system

## Project Structure

```
src/
├── ai/              # AI service integration
├── babylon/         # 3D engine management
├── components/      # React UI components
├── hooks/          # Custom React hooks
├── state/          # Global state management
├── types/          # TypeScript definitions
├── App.tsx         # Main application component
└── main.tsx        # Application entry point
```

## Core Architecture

### Data Flow
1. **User Input** → UI Components → State Store → Scene Manager → Babylon.js
2. **AI Commands** → AI Service → Parsed Actions → State Store → Scene Updates
3. **3D Interactions** → Babylon.js → Scene Manager → State Store → UI Updates

### Key Components

#### State Management (`src/state/`)
- **`sceneStore.ts`**: Zustand store managing all application state
- Central source of truth for 3D objects, UI state, and user interactions
- Provides actions for CRUD operations on scene objects

#### 3D Engine (`src/babylon/`)
- **`sceneManager.ts`**: Low-level Babylon.js scene management
- **`objectFactory.ts`**: Factory functions for creating 3D primitives
- **`gizmoManager.ts`**: Transform gizmo controls for object manipulation
- **`hooks/useBabylonScene.ts`**: React hook bridging 3D scene with React state

#### AI Integration (`src/ai/`)
- **`ai.service.ts`**: OpenAI API integration for natural language processing
- Translates user commands into structured scene operations
- Maintains conversation context for intelligent interactions

#### UI Components (`src/components/`)
- **`sidebar/AISidebar.tsx`**: AI command interface and controls
- **`sidebar/SceneGraph.tsx`**: Scene object hierarchy viewer
- **`sidebar/PropertiesPanel.tsx`**: Object property editor
- **`App.tsx`**: Main application layout and toolbar

#### Hooks (`src/hooks/`)
- **`useKeyboardShortcuts.tsx`**: Global keyboard shortcut management
- Custom hooks for reusable logic across components

## Key Patterns

### React-Babylon Integration
The application uses a custom hook pattern to bridge React's declarative model with Babylon.js's imperative API:

```typescript
// React State (Declarative)
const { sceneObjects, selectedObjectId } = useSceneStore()

// Babylon.js Scene (Imperative)
const { sceneAPI } = useBabylonScene(canvasRef)
```

### State-First Architecture
All 3D operations flow through the Zustand store, ensuring:
- Single source of truth
- Predictable state updates
- Easy debugging and testing
- Seamless UI synchronization

### AI Command Processing
Natural language commands are processed through a structured pipeline:
1. User input → AI Service
2. AI Service → Structured commands
3. Commands → Store actions
4. Store actions → 3D scene updates

## Development Workflow

### Adding New 3D Objects
1. Define type in `src/types/types.ts`
2. Add factory function in `src/babylon/objectFactory.ts`
3. Update UI creation controls in `App.tsx`

### Extending AI Commands
1. Add command type to `src/ai/ai.service.ts`
2. Update system prompt with new capabilities
3. Implement command handler in scene store

### UI Component Development
1. Create component in appropriate `src/components/` subdirectory
2. Connect to store using `useSceneStore()`
3. Follow existing patterns for consistent styling

## Clean Architecture Benefits

This "clean" version maintains:
- **No Authentication**: Direct access to all features
- **No Database**: Browser-only state management
- **No Server**: Pure client-side application
- **Open Source**: MIT licensed for community development

The architecture is designed to be:
- **Learnable**: Clear separation of concerns
- **Extensible**: Easy to add new features
- **Maintainable**: Well-structured codebase
- **Performant**: Efficient state management and 3D rendering 