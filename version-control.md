# Landing Page Version Control

## Quick Commands

**Save current version:**
```bash
cp index.html versions/v[number]-[description].html
```

**Restore a version:**
```bash
cp versions/v[number]-[description].html index.html
```

**List all versions:**
```bash
ls -la versions/
```

## Version History

- **v0-base-warm-design.html** - Clean warm beige design with Crimson Text font, distributed testimonials
- **v1-testimonial-avatars.html** - Added circular avatars to testimonials (experiment)

## Backup Workflow

1. Before making changes: `cp index.html versions/v[X]-current-backup.html`
2. Make changes to `index.html`
3. Test changes: `open index.html`
4. If satisfied: `cp index.html versions/v[X+1]-[description].html`
5. If not satisfied: `cp versions/v[X]-current-backup.html index.html`

## Git Integration

```bash
# Stage and commit versions
git add versions/
git commit -m "Add version v[X]-[description]"

# Stage main file
git add index.html
git commit -m "[description of changes]"
```