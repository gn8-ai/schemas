# Gn8 schemas

Public JSON schemas for Gn8 tools. This repository hosts schema files that editors and other JSON Schema consumers can reference directly.

## Available schemas

| Schema | File | Reference URL |
| --- | --- | --- |
| AIM manifest, v1 | [`aim/manifest/v1.json`](./aim/manifest/v1.json) | [`https://raw.githubusercontent.com/gn8-ai/schemas/main/aim/manifest/v1.json`](https://raw.githubusercontent.com/gn8-ai/schemas/main/aim/manifest/v1.json) |

The AIM manifest schema uses JSON Schema Draft 7. It describes manifest fields such as packages, dependencies, artifacts, and targets.

## Reference the AIM manifest schema

For a JSON manifest, set `$schema` to the published URL:

```json
{
  "$schema": "https://raw.githubusercontent.com/gn8-ai/schemas/main/aim/manifest/v1.json"
}
```

For a YAML manifest, editors that support a YAML language-server schema directive can use:

```yaml
# yaml-language-server: $schema=https://raw.githubusercontent.com/gn8-ai/schemas/main/aim/manifest/v1.json
$schema: https://raw.githubusercontent.com/gn8-ai/schemas/main/aim/manifest/v1.json
```

Schema validation checks document structure. It does not replace AIM's runtime checks, including glob compilation.

## Updates

The reference URL tracks `main`. For reproducible validation, replace `main` in the raw URL with a specific commit SHA in your editor's schema configuration. Keep the manifest's `$schema` value above: this schema requires that exact value.

## About Gn8

[Gn8](https://gn8.ai/) develops and maintains open-source development platforms, libraries, and CLIs. See the [GitHub organization](https://github.com/gn8-ai) for public repositories.

## License

[MIT](./LICENSE).
