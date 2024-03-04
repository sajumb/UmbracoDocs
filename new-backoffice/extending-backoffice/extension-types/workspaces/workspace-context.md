---
description: >-
  A Workspace context is a container for the data of a workspace. It is a
  wrapper around the data of the entity that the workspace is working on.
---

# Workspace Context

TODO: Extend the description of a workspace

(rough notes)

* A workspace context knows about its entity type (for example content, media, member, etc.) and holds its unique string (e.g.: key).
* Most workspaces contexts hold a draft state of its entity data. It is a copy of the entity data that can be modified at runtime and sent to the server to be saved.

If a workspace wants to utilize Property Editor UIs, then it must provide a variant context for the property editors. The variant-context is the generic interface between workspace and property editors. See variant contexts for more info.

TODO: More points and examples:

```ts
// TODO: get typescript interface
interface UmbWorkspaceContext {}
```

### Examples of workspaces

TODO: link to all workspaces in storybook. Can we somehow auto-generate this list?