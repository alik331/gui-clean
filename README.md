# Moorph GUI Clean

A powerful, browser-based 3D CAD application that enables users to create and manipulate 3D objects with AI assistance. Built with React, TypeScript, Babylon.js, and powered by OpenAI's API through an MCP (Model Context Protocol) server.

## 🚀 Getting Started

### Prerequisites
- Node.js 18+ 
- npm or yarn
- OpenAI API key (for AI features)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/VibeCAD/gui-clean.git
   cd gui-clean
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start the development server**
   ```bash
   npm run dev
   ```

4. **Open your browser**
   Navigate to `http://localhost:5173`

### Configuration

When you first launch the application, you'll be prompted to enter your OpenAI API key. This enables the AI-powered scene manipulation features.

> **Note**: Your API key is stored locally in your browser and never sent to external servers.

## ✨ Features

**🎯 3D Creation**: Primitives (cube, sphere, cylinder, etc.) and housing elements with full transform controls  
**🤖 AI Integration**: Natural language commands for scene manipulation via OpenAI API  
**🛠️ Professional Tools**: Multi-select, snap-to-grid, camera controls, wireframe mode  
**🎨 Modern UI**: Dropdown toolbar, real-time status, keyboard shortcuts, responsive design  

## 🏗️ Architecture

### Core Technologies
- **Frontend**: React 18 + TypeScript + Vite
- **3D Engine**: Babylon.js for WebGL rendering
- **State Management**: Zustand for application state
- **AI Integration**: OpenAI API with MCP Server
- **Styling**: Custom CSS with modern design system

### Key Components
- **`useBabylonScene`**: Main hook managing 3D scene lifecycle
- **`SceneStore`**: Centralized state management for 3D objects
- **`AISidebar`**: AI-powered natural language interface
- **`GizmoManager`**: Interactive 3D transform controls
- **`ObjectFactory`**: 3D primitive and housing creation system

## 🎮 Usage

### Creating Objects
1. Click **Create** in the toolbar
2. Select from Primitives or Housing elements
3. Object appears in the 3D scene at a random position
4. Use transform tools to position and modify

### AI Commands
1. Open the AI sidebar (right panel)
2. Enter natural language commands like:
   - "Create a red cube next to the sphere"
   - "Make all objects blue"
   - "Arrange objects in a circle"
   - "Delete everything except the house"

### Transform Operations
1. Select an object in the 3D scene
2. Choose transform mode: Select, Move, Rotate, or Scale
3. Use gizmo handles for precise manipulation
4. Hold Ctrl for multi-select operations

### Camera Navigation
- **Mouse**: Left-click and drag to rotate
- **Wheel**: Zoom in/out
- **Toolbar**: Quick camera positions (Front, Top, etc.)

## 🔧 Development

### Project Structure
```
src/
├── babylon/          # Babylon.js integration
│   ├── hooks/       # React hooks for 3D scene
│   ├── objectFactory.ts
│   ├── sceneManager.ts
│   └── gizmoManager.ts
├── components/       # React components
│   └── sidebar/     # AI and properties panels
├── state/           # State management
│   └── sceneStore.ts
├── types/           # TypeScript definitions
└── ai/              # AI service integration
```

### Key Scripts
```bash
npm run dev          # Start development server
npm run build        # Build for production
npm run preview      # Preview production build
npm run lint         # Run ESLint
```

## 🌟 Why "Clean"?

This repository represents a **clean**, open-source version of the Moorph GUI platform:

- ❌ **No Authentication**: No login/signup required
- ❌ **No Database**: No server-side data persistence
- ❌ **No Cloud Services**: Runs entirely in the browser
- ✅ **Pure 3D Creation**: Focus on core 3D manipulation features
- ✅ **AI Integration**: Full OpenAI API support
- ✅ **Open Source**: MIT licensed for community development

Perfect for developers who want to:
- Learn 3D web development with Babylon.js
- Integrate AI into 3D applications
- Build upon a solid CAD foundation
- Contribute to open-source 3D tools

## 🤝 Contributing

We welcome contributions! This clean version is designed for community development:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## 📝 License

MIT License - see [LICENSE](LICENSE) file for details.

---

**Built with ❤️ by Moorph Labs**

> Transform your 3D ideas into reality with the power of AI and modern web technologies.
