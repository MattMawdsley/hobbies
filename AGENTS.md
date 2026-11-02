# Hobbies Web Applications

This repository contains web-based calculators and tools for various hobbies and games.

## Repository Information

- **Location**: `/Users/mattmawdsley/Documents/src`
- **GitHub**: https://github.com/MattMawdsley/hobbies.git
- **Git Remote**: `git@github.com:MattMawdsley/hobbies.git` (SSH)
- **Authentication**: SSH key at `~/.ssh/github_ed25519`

## Projects

### oathsworn
Oathsworn: Into the Deepwood dice probability calculator.

**Location**: `oathsworn/OathswornDieCalc.html`

**Features**:
- Defense selection (1-6) with button interface
- Dice pool management (White/Yellow/Red/Black dice)
- Reroll and empower token support
- Loadout save/load functionality (localStorage)
- Probability calculations for hits, misses, crits, and wound distribution
- Monte Carlo simulation for large dice pools (8+ dice)
- Exact enumeration for small dice pools (<8 dice)

**To run locally**:
```bash
cd oathsworn
python3 -m http.server 8080
# Open http://localhost:8080
```

**Technical Notes**:
- Single-file HTML/CSS/JS application
- Uses localStorage for loadout persistence
- Recursive crit calculation: EV_actual = EV_base × 1.2 (6/5 for 1/6 crit chance)
- Reroll optimization: Minimizes miss probability, then maximizes expected damage
- Empower logic: Can add new white dice when all existing dice are at max tier (Black)

### dnd
(Coming soon - D&D tools)

## Development Workflow

1. Make changes locally
2. Test with local server
3. Commit changes:
   ```bash
   git add .
   git commit -m "Description of changes"
   ```
4. Push to GitHub:
   ```bash
   git push
   ```

## Git Configuration

- Git is initialized in the `src` folder
- Main branch: `main`
- SSH authentication configured for GitHub
