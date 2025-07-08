# Contributing to Moorph GUI Clean

Thank you for your interest in contributing to Moorph GUI Clean! This document provides guidelines and information for contributors.

## 🌟 Ways to Contribute

- **Bug Reports**: Found a bug? Report it!
- **Feature Requests**: Have an idea? Share it!
- **Code Contributions**: Submit pull requests
- **Documentation**: Improve docs and examples
- **Testing**: Help test new features
- **Community**: Answer questions and help others

## 🚀 Getting Started

### Prerequisites
- Node.js 18 or higher
- Git
- Basic knowledge of React, TypeScript, and 3D graphics
- OpenAI API key (for AI features)

### Setup
1. Fork the repository
2. Clone your fork: `git clone https://github.com/YOUR_USERNAME/gui-clean.git`
3. Install dependencies: `npm install`
4. Start development server: `npm run dev`
5. Open `http://localhost:5173` in your browser

## 📋 Development Workflow

### Before You Start
1. Check existing issues to avoid duplicates
2. Create an issue for new features or major changes
3. Fork the repository and create a feature branch
4. Follow the coding standards below

### Making Changes
1. Create a feature branch: `git checkout -b feature/your-feature-name`
2. Make your changes following our coding standards
3. Test your changes thoroughly
4. Run linting: `npm run lint`
5. Build the project: `npm run build`
6. Commit with clear messages

### Submitting Pull Requests
1. Push your branch to your fork
2. Create a pull request from your fork to the main repository
3. Provide a clear description of changes
4. Link to any related issues
5. Be responsive to feedback during review

## 🎯 Areas for Contribution

### High Priority
- **3D Primitives**: Add new geometric shapes and housing elements
- **AI Commands**: Extend natural language processing capabilities
- **UI/UX**: Improve user interface and interactions
- **Performance**: Optimize 3D rendering and state management

### Medium Priority
- **Testing**: Add unit and integration tests
- **Documentation**: Improve inline documentation
- **Accessibility**: Enhance keyboard navigation and screen reader support
- **Mobile**: Improve responsive design for tablets

### Future Enhancements
- **Export/Import**: Add file format support (STL, OBJ, etc.)
- **Plugins**: Create plugin architecture
- **Collaboration**: Real-time collaborative editing
- **Advanced Materials**: PBR materials and textures

## 📝 Coding Standards

### TypeScript
- Use TypeScript for all new code
- Provide proper type definitions
- Avoid `any` types when possible
- Use interfaces for object structures

### React
- Use functional components with hooks
- Follow React best practices
- Use custom hooks for reusable logic
- Implement proper error boundaries

### 3D/Babylon.js
- Use the existing `sceneManager` pattern
- Follow imperative-to-declarative bridging patterns
- Properly dispose of 3D resources
- Use the established object factory pattern

### State Management
- Use Zustand store for global state
- Keep state minimal and normalized
- Use actions for state mutations
- Implement proper getters for derived state

### Styling
- Use the existing CSS patterns
- Follow responsive design principles
- Maintain consistent spacing and typography
- Use CSS variables for theming

## 🧪 Testing

### Manual Testing
- Test all 3D interactions (create, select, transform)
- Verify AI command processing
- Check responsive design on different screen sizes
- Test keyboard shortcuts and accessibility

### Automated Testing
- Add unit tests for utility functions
- Test React components with React Testing Library
- Mock 3D scene interactions appropriately
- Test state management logic

## 📚 Documentation

### Code Documentation
- Document all public functions and classes
- Use JSDoc for TypeScript documentation
- Include examples for complex functions
- Document architectural decisions

### User Documentation
- Update README.md for new features
- Add examples to ARCHITECTURE.md
- Create tutorials for complex workflows
- Update keyboard shortcuts list

## 🐛 Bug Reports

When reporting bugs, please include:
- **Environment**: OS, browser, Node.js version
- **Steps to Reproduce**: Detailed reproduction steps
- **Expected Behavior**: What should happen
- **Actual Behavior**: What actually happens
- **Screenshots**: Visual evidence if applicable
- **Console Logs**: Any error messages

## 💡 Feature Requests

For feature requests, please provide:
- **Use Case**: Why is this feature needed?
- **Proposed Solution**: How should it work?
- **Alternatives**: Other approaches considered
- **Implementation**: Technical approach if known

## 🔧 Architecture Guidelines

### Adding New 3D Objects
1. Define type in `src/types/types.ts`
2. Add factory function in `src/babylon/objectFactory.ts`
3. Update UI controls in `App.tsx`
4. Add to housing factory if applicable

### Extending AI Commands
1. Add command type to `src/ai/ai.service.ts`
2. Update system prompt with new capabilities
3. Implement command handler in scene store
4. Add error handling and validation

### UI Component Development
1. Create in appropriate `src/components/` directory
2. Connect to store using `useSceneStore()`
3. Follow existing styling patterns
4. Add proper accessibility attributes

## 🤝 Community

### Code of Conduct
Please read and follow our [Code of Conduct](CODE_OF_CONDUCT.md).

### Getting Help
- **Issues**: Use GitHub issues for bugs and features
- **Discussions**: Use GitHub discussions for questions
- **Architecture**: Review [ARCHITECTURE.md](ARCHITECTURE.md)
- **Support**: See [SUPPORT.md](SUPPORT.md)

## 📄 License

By contributing, you agree that your contributions will be licensed under the MIT License.

---

**Thank you for contributing to Moorph GUI Clean!** 🎉

Your contributions help make 3D modeling more accessible and powerful for everyone. 