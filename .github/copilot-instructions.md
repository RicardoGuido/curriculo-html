# AI Coding Agent Instructions for CurriculoHTML

## Project Overview
This is a **HTML/CSS learning project** organized by progressive lessons for SENAC-SP technical school students. Each folder represents a class session with growing complexity in layout techniques.

## Project Structure

### Folder Organization
- **HTML- aula1/**: Foundational HTML - basic tags, forms, links, lists, text formatting
- **aula02/**: Introductory HTML and CSS
- **aula03/**: Layout fundamentals - Flexbox and card components (`flexbox.html`, `atividadecard.html`, `flexcardreal.html`)
- **aula04-landingPage/**: Professional landing page project (main deliverable) - uses CSS variables and responsive design
- **curriculo/**: Curriculum vitae page with gradient backgrounds and custom styling
- **Imagem/**: Image assets used across projects

### Key Files
- **aula04-landingPage/index.html** + **style.css**: The primary production example - modern landing page for "EduTrack" platform with:
  - CSS custom properties (variables) for consistent theming
  - Mobile-responsive design
  - Component-based structure (navbar, hero, sections)
  - Google Fonts integration

- **curriculo/curriculo.html**: Portfolio example using inline styles and gradient backgrounds

## Code Patterns & Conventions

### CSS Organization
1. **CSS Variables (Custom Properties)**: The landing page uses `:root` variables for:
   - Colors (primary, hover states, text colors, backgrounds)
   - Spacing scale (--espaco-xs through --espaco-xxl using rem units)
   - Border radius variants (sm, md, lg)
   
   Example from `aula04-landingPage/style.css`:
   ```css
   :root {
       --cor-principal: #004ac6;
       --espaco-sm: 1rem; /* 16px */
       --raio-md: 0.75rem;
   }
   ```

2. **Box Model**: Universal reset applied consistently:
   ```css
   * {
       margin: 0;
       padding: 0;
       box-sizing: border-box;
   }
   ```

3. **Layout Methods**: Projects progress through:
   - **Early lessons**: Inline styles + basic positioning
   - **aula03**: Flexbox layouts (see `atividadecard.html`, `flexbox.html`)
   - **aula04**: Production-grade CSS with grid/flexbox combinations

### HTML Conventions
- Portuguese language (`lang="pt-br"`) throughout
- Mobile viewport meta tag: `<meta name="viewport" content="width=device-width, initial-scale=1.0">`
- Google Fonts preconnect for performance
- Semantic HTML structure (header, main, nav, section tags)

### Component Patterns
**Landing Page Components** (`aula04-landingPage/index.html`):
- Navbar with navigation links and CTA buttons
- Hero section with headline hierarchy
- Feature/section areas with consistent spacing

## Development Workflow

### No Build System
This is a **static HTML/CSS** project - no compilation, bundlers, or dependencies. Open any `.html` file directly in a browser to preview.

### Testing/Validation
- Open files directly in browser (File → Open or drag into browser)
- Check responsive design by resizing browser or using DevTools
- Verify CSS variable values in browser DevTools (Inspect → Styles → :root)

## Common Tasks

### Adding New Components
1. Use existing CSS variables from `:root` - don't hardcode colors/spacing
2. Follow the spacing scale (--espaco-xs to --espaco-xxl)
3. Use `display: flex` or `display: grid` for layouts
4. Apply `border-radius` using variable (--raio-sm/md/lg)

### Updating Landing Page
- Main CSS in `aula04-landingPage/style.css` (376 lines)
- Main HTML in `aula04-landingPage/index.html` (190 lines)
- Maintain semantic HTML structure with section wrappers

### Styling Curriculum Page
- Uses inline styles + embedded `<style>` tags in `curriculo/curriculo.html`
- Gradient backgrounds pattern: `linear-gradient(90deg, ...)`
- Centered layouts with `display: flexbox; text-align: center;`

## Important Notes
- **Portuguese Documentation**: In-code comments are in Portuguese (e.g., `/* Reset universal */`)
- **No External Dependencies**: All fonts from Google Fonts CDN, no Node/npm required
- **Learning Project**: Code may include commented-out explanations and experimental approaches
- **Responsive First**: Mobile viewport meta tag present; designs should support mobile/tablet/desktop
