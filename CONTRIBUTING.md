# Contributing

1. Fork the repo at https://github.com/neardaniel-pls/near-work-analysis
2. Create a feature branch: `git checkout -b feature/your-feature`
3. Make your changes
4. Push and open a pull request

## Code Style

- Keep analysis in the Jupyter notebook
- Document new sections with markdown cells
- Use clear variable names
- Add comments for complex calculations

## Adding New Roles

To add a new career role, update the `data` dictionary in the "Data Definition" section with:
- Role name
- All 9 attribute scores (1-10 scale)
- Average junior salary
- Required tools in `tools_data`

## Commit Messages

Use conventional commits: `feat`, `fix`, `docs`, `refactor`, `chore`
