# Tips & Pitfalls

- Cognitive Search:
	- Use the .NET SDK and follow the tutorial sequence (data source → skillset → index → indexer).
	- Indexer errors are common—check indexer execution status and skill outputs for failures.
	- Be explicit with field attributes (searchable/filterable/facetable) to match queries.
- AI Vision:
	- Use the v4.0 Image Analysis client; verify region and API version.
	- Large images can slow responses; start with smaller samples.
- Configuration:
	- Keep keys and endpoints in environment variables or user-secrets; do not commit secrets.
	- Consider local stubs when cloud access isn’t available; save sample outputs under results/ to keep the workflow consistent.
