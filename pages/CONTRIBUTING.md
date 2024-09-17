# CONTRIBUTING

## Code

Your code MUST follow the repository's eslint configuration (run nx lint before committing)

## Commit messages

MUST be in english

MUST describe what has been done in the code briefly

MUST be in imperative mood (ie: Add contributing guidelines)

## Structure

### Controller structure (example with DemoController)
- Controller file location: libs/demo.controller/demo.controller.ts
- Test file location: libs/demo.controller/demo.controller.spec.ts

### Service structure (example with VideoEditorService)
- Service file location: libs/video-editor.service/video-editor.service.ts
- Test file location: libs/video-editor.service/video-editor.service.spec.ts

## Testing

Unit tests are located in a .spec.ts file in their component or service folder

e2e tests are located in the apps/*app*-e2e folder

## API Routes

MUST be in a controller

MUST be stateless

MUST use the correct http verb for its action
https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods

MUST reply with the most accurate HTTP code
https://developer.mozilla.org/en-US/docs/Web/HTTP/Status

## Pull Requests

MUST only add ONE feature

SHOULD be as small as possible

MUST be approved by at least one of the code owners

SHOULD be approved by at least two developers
