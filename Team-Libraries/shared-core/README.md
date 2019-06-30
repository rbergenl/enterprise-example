Team Shared Core
---

# Shared components
- Routing
- Session Management
- Events Bus

# Guidelines
- Do not use a framework, also no jQuery. Provide vanilla javascript components.
- Do not initialise components automatically. Provide a `custom element` to initialise the components.
- Do not introduce side-effects (like API calls), instead trigger events, or provide a public api.
- Keep this library as thing as possible.
