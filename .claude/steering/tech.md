# Technical Stack & Development Guidelines

## Core Technology Stack

### Static Site Generator
- **Quarto**: Primary framework for content authoring and site generation
- **Version**: Latest stable version supporting website projects
- **Configuration**: `_quarto.yml` for site-wide settings and navigation

### Frontend Technologies
- **HTML5**: Semantic markup with accessibility considerations
- **CSS3**: Custom styling with modern features (Grid, Flexbox, CSS Variables)
- **Bootstrap CSS**: Framework integration via Quarto's Cosmo theme
- **Font Awesome**: Icon library for social links and UI elements
- **JavaScript**: Minimal client-side scripting for interactivity

### Content Format
- **QMD Files**: Quarto Markdown for all content pages
- **YAML Front Matter**: Metadata and configuration for each page
- **Markdown**: Standard formatting with Quarto extensions

### Styling Architecture
- **Theme Base**: Quarto's built-in Cosmo theme
- **Custom CSS**: `styles.css` for project-specific styling
- **Responsive Design**: Mobile-first approach with breakpoints
- **Design System**: Consistent spacing, typography, and color schemes

## Development Workflow

### File Structure Conventions
```
├── _quarto.yml           # Site configuration and navigation
├── index.qmd            # Homepage content
├── about.qmd            # About page content
├── projects/            # Project showcase directory
│   ├── project-1.qmd    # Individual project pages
│   └── project-*.qmd    # Additional projects
├── images/              # Static assets and media
├── styles.css           # Custom styling overrides
└── _site/              # Generated static site (auto-generated)
```

### Content Development
- **Quarto Markdown**: Use QMD syntax for enhanced features
- **YAML Headers**: Required metadata for title, date, categories
- **Code Blocks**: Syntax highlighting for technical content
- **Cross-References**: Link between pages using relative paths

### Asset Management
- **Images**: Store in `/images/` directory with descriptive names
- **Optimization**: Use appropriate formats (JPG for photos, PNG for graphics)
- **Responsive**: Implement with CSS max-width: 100% for mobile compatibility

## Deployment & Hosting

### GitHub Pages Integration
- **Automatic Deployment**: GitHub Actions workflow in `.github/workflows/`
- **Source Branch**: Main branch triggers automatic builds
- **Build Process**: Quarto render → GitHub Pages deployment
- **Custom Domain**: Support for custom domain configuration

### Build Process
1. **Content Rendering**: Quarto processes QMD files to HTML
2. **Asset Processing**: Images and CSS compiled into `_site/`
3. **Site Generation**: Static HTML pages with navigation and layout
4. **Deployment**: Automatic push to `gh-pages` branch

### Performance Optimization
- **Static Generation**: No server-side processing required
- **CDN Delivery**: GitHub Pages CDN for global distribution
- **Caching**: Browser caching for static assets
- **Minimal JavaScript**: Reduce load times with minimal client-side code

## Code Quality Standards

### HTML Standards
- **Semantic Markup**: Use appropriate HTML5 elements
- **Accessibility**: Include alt text, ARIA labels, and keyboard navigation
- **Validation**: Valid HTML5 syntax
- **SEO**: Proper heading hierarchy and meta descriptions

### CSS Best Practices
- **Mobile-First**: Design for mobile devices first
- **Progressive Enhancement**: Enhance for larger screens
- **Performance**: Minimize CSS file size and complexity
- **Maintainability**: Use clear class naming conventions

### Content Guidelines
- **Professional Tone**: Business-appropriate language and imagery
- **Consistency**: Uniform formatting and style across pages
- **Accuracy**: Verify all links, especially to external resources
- **Updates**: Regular content refresh with new projects

## Development Environment

### Required Tools
- **Quarto CLI**: Latest version for local development and rendering
- **Git**: Version control and GitHub integration
- **Code Editor**: VS Code, Vim, or preferred editor with Markdown support
- **Browser**: Modern browser for testing and preview

### Local Development
```bash
# Install Quarto (macOS)
brew install quarto

# Preview locally
quarto preview

# Render for production
quarto render
```

### Testing Checklist
- [ ] Mobile responsiveness across devices
- [ ] Link validation (internal and external)
- [ ] Image loading and optimization
- [ ] Cross-browser compatibility
- [ ] Accessibility compliance
- [ ] Performance metrics (loading speed)

## Security & Privacy

### Data Protection
- **No Personal Data Collection**: Static site with no backend
- **External Links**: Target="_blank" for external navigation
- **Third-Party Content**: Minimal external dependencies

### Content Security
- **Public Repository**: All content is publicly visible
- **Professional Content Only**: No sensitive or private information
- **Regular Updates**: Keep dependencies and themes current

## Integration Points

### External Services
- **Vercel**: For embedding live application demos
- **GitHub**: Source code repositories and version control
- **LinkedIn**: Professional networking integration
- **Font Awesome CDN**: Icon library hosting

### Analytics & Monitoring
- **GitHub Insights**: Repository traffic and engagement data
- **Web Analytics**: Optional integration with Google Analytics
- **Performance Monitoring**: Browser dev tools for optimization

## Maintenance Guidelines

### Regular Tasks
- **Content Updates**: Add new projects and achievements
- **Link Verification**: Check for broken or outdated links
- **Dependency Updates**: Keep Quarto and themes current
- **Performance Review**: Monitor site speed and user experience

### Version Control
- **Commit Messages**: Clear, descriptive commit messages
- **Branching**: Use feature branches for major updates
- **Backup**: GitHub serves as primary backup system
- **Documentation**: Update README for significant changes