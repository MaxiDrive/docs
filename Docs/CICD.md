# CI/CD

```mermaid
mindmap
((Repository))
	[Push]
		[main]
			Deploy Production
			Release
		[dev]
			Deploy Development
	[Pull Request]
		[dev]
			Run tests
```

## Continuous integration

```mermaid
mindmap
((Repository))
	[Push]
		[main]
			Release
		[dev]
	[Pull request]
		[dev]
			Test
```

### Test

| Feature     | Value                             |
| ----------- | --------------------------------- |
| Executes    | On **PR** to `dev`                |
| Permissions | **Read only** repository contents |

### Release

| Feature     | Value                                                        |
| ----------- | ------------------------------------------------------------ |
| Executes    | On **Pushes** to `main`                                      |
| Permissions | **Read only** repository contents, **Read/Write** releases, **Read/Write** packages |


## Continuous deployment

```mermaid
mindmap
((Repository))
	[Push]
        [dev]
        	Deploy Development
        [main]
        	Deploy Production
```