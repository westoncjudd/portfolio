# Project Structure & Architecture

## Directory Architecture

### Root Level Structure
```
portfolio/
├── .claude/                 # Claude Code configuration and steering docs
│   └── steering/           # Project steering documents
├── .github/                # GitHub Actions and repository configuration
│   └── workflows/          # Automated deployment workflows
├── .git/                   # Git version control
├── .quarto/                # Quarto build cache and temporary files
├── _site/                  # Generated static website (build output)
├── projects/               # Individual project showcase pages
├── images/                 # Static assets and media files
├── _quarto.yml            # Main Quarto configuration
├── index.qmd              # Homepage content
├── about.qmd              # About page content
├── styles.css             # Custom CSS styling
├── README.md              # Repository documentation
└── .gitignore             # Git ignore patterns
```

## File Organization Patterns

### Content Structure
- **QMD Files**: All content pages use Quarto Markdown format
- **YAML Front Matter**: Consistent metadata structure across all pages
- **Hierarchical Navigation**: Organized menu structure in `_quarto.yml`

### Asset Management
- **Centralized Images**: All media in `/images/` with descriptive naming
- **Modular CSS**: Single `styles.css` file with organized sections
- **Project Resources**: Each project may reference specific assets

### Configuration Architecture
- **Site Configuration**: `_quarto.yml` contains all site-wide settings
- **Build Configuration**: Quarto handles rendering and output generation
- **Deployment Configuration**: GitHub Actions in `.github/workflows/`

## Content Architecture

### Page Hierarchy
```
Website Structure:
├── Home (index.qmd)
│   ├── Hero Section
│   ├── Featured Projects Grid
│   └── Social Links
├── About (about.qmd)
│   ├── Professional Background
│   ├── Education & Experience
│   ├── Skills & Capabilities
│   └── Career Objectives
└── Projects Menu
    ├── Project 1 (project-1.qmd)
    ├── Project 2 (project-2.qmd)
    └── Additional Projects...
```

### Content Patterns
- **Consistent Layout**: All pages follow similar structural patterns
- **Responsive Design**: Mobile-first approach with progressive enhancement
- **Cross-References**: Internal linking between related content
- **External Integration**: Links to live demos and source repositories

## Component Architecture

### Reusable Elements
- **Hero Banner**: Standardized profile section across pages
- **Social Links**: Consistent button styling and functionality
- **Project Cards**: Uniform project presentation format
- **Navigation**: Dropdown menu system for project organization

### Styling System
- **CSS Variables**: Consistent color scheme and spacing
- **Component Classes**: Reusable styling for common elements
- **Responsive Breakpoints**: Mobile, tablet, and desktop optimizations
- **Theme Integration**: Bootstrap classes combined with custom styling

## Data Flow Architecture

### Content Processing
1. **Source**: QMD files with YAML metadata
2. **Processing**: Quarto rendering engine
3. **Output**: Static HTML pages in `_site/`
4. **Deployment**: GitHub Pages hosting

### Navigation Generation
- **Configuration**: Menu structure defined in `_quarto.yml`
- **Dynamic**: Quarto generates navigation from configuration
- **Responsive**: Mobile-friendly dropdown menus
- **Accessible**: Keyboard navigation and screen reader support

## Build Architecture

### Development Workflow
1. **Local Development**: `quarto preview` for real-time editing
2. **Content Creation**: Write/edit QMD files with metadata
3. **Asset Management**: Add images and update references
4. **Testing**: Local preview and responsive testing
5. **Deployment**: Git push triggers automatic build

### Production Pipeline
```
Git Push → GitHub Actions → Quarto Render → Static Site → GitHub Pages
```

### Output Structure
```
_site/
├── index.html              # Generated homepage
├── about.html              # Generated about page
├── projects/               # Generated project pages
│   ├── project-1.html
│   └── project-2.html
├── images/                 # Copied static assets
├── styles.css              # Processed CSS
└── site_libs/              # Quarto dependencies and libraries
```

## Design Patterns

### Layout Patterns
- **Grid System**: Bootstrap-based responsive grid
- **Card Components**: Project showcase cards with hover effects
- **Hero Sections**: Prominent profile and introduction areas
- **Content Blocks**: Structured sections for readability

### Navigation Patterns
- **Top Navigation**: Horizontal navbar with brand and menu items
- **Dropdown Menus**: Organized project listings
- **Breadcrumbs**: Implicit navigation through clear page titles
- **Call-to-Action**: Strategic placement of contact and demo links

### Content Patterns
- **Progressive Disclosure**: Summary cards leading to detailed pages
- **Embedded Demos**: Live application previews via iframes
- **External Links**: Clear indication of external navigation
- **Contact Integration**: Multiple touchpoints for professional contact

## Scalability Architecture

### Content Expansion
- **Modular Projects**: Easy addition of new project pages
- **Template Consistency**: Standardized project page format
- **Navigation Updates**: Simple configuration changes in `_quarto.yml`
- **Asset Organization**: Scalable image and media management

### Performance Considerations
- **Static Generation**: No server-side processing required
- **Optimized Assets**: Compressed images and minimal CSS/JS
- **CDN Delivery**: GitHub Pages global content delivery
- **Caching Strategy**: Browser caching for static resources

## Integration Architecture

### External Services
- **GitHub**: Source code hosting and version control
- **Vercel**: Live application demo hosting
- **LinkedIn**: Professional networking integration
- **Font Awesome**: Icon library via CDN

### Development Tools Integration
- **VS Code**: Recommended editor with Quarto extension
- **Git**: Version control with GitHub integration
- **Quarto CLI**: Local development and build tools
- **Browser DevTools**: Testing and optimization

## Maintenance Architecture

### Update Patterns
- **Content Updates**: Regular addition of new projects and achievements
- **Configuration Changes**: Navigation and site settings updates
- **Theme Updates**: Quarto and Bootstrap version management
- **Asset Management**: Image optimization and organization

### Quality Assurance
- **Link Validation**: Regular checking of internal and external links
- **Responsive Testing**: Multi-device compatibility verification
- **Performance Monitoring**: Load time and user experience optimization
- **Accessibility Review**: Screen reader and keyboard navigation testing

## Security & Privacy Architecture

### Data Protection
- **Static Content**: No server-side data processing
- **Public Repository**: All source code publicly visible
- **No Analytics**: Minimal third-party tracking
- **Professional Content**: No personal or sensitive information

### Access Control
- **GitHub Permissions**: Repository access through GitHub
- **Deployment Control**: Automatic from main branch only
- **Content Review**: Git workflow for change management
- **Public Visibility**: Website accessible to all users