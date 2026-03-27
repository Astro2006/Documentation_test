## Adding a New Page

This guide walks through adding a new Markdown page to the fake docs set.

## Steps

1. Create a new file under `docs/` (use kebab-case)
2. Add a `## Title` at the top
3. Link it from `docs/table_of_content.md`
4. Add at least one cross-link from an existing page

## Example

If you create `docs/guides/my-new-guide.md`, add an entry under the “Guides” section in the TOC:

```md
1. My New Guide (order: 3) - `docs/guides/my-new-guide.md` - [Open](docs/guides/my-new-guide.md)
```

## Related

- [Maintaining the TOC](maintaining-the-toc.md)
- [Writing Pages](../basics/writing-pages.md)

