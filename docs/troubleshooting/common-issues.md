## Common Issues

This page lists fake issues you can use to test search and troubleshooting navigation.

### “Link not found” errors

- Confirm the file exists under `docs/`
- Check the path casing (macOS is often case-insensitive, CI might not be)
- Prefer relative links

### TOC entry doesn’t open

- Ensure the markdown link target matches the file path
- Verify there are no extra spaces in the link URL

### Headings don’t appear in the sidebar

- Ensure headings use `##` / `###` (some renderers ignore `#` inside nested layouts)

## Related

- [Linking & Navigation](../basics/linking-and-navigation.md)
- [Maintaining the TOC](../guides/maintaining-the-toc.md)

