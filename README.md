# STAC Catalogs for FESOM - Presentation

A Slidev presentation introducing STAC catalogs and comparing two organizational strategies for FESOM climate model output.

## Contents

This presentation covers:

1. **Introduction to STAC** - What is SpatioTemporal Asset Catalog?
2. **STAC Hierarchy** - Catalog → Collection → Item structure
3. **Why STAC for FESOM** - Benefits for climate model data
4. **Two Catalog Strategies**:
   - Single Collection: All variables in one collection
   - Per-Variable Collections: One collection per variable type
5. **Code Examples** - Reading catalogs with intake-stac
6. **Comparison** - Advantages and disadvantages of each approach
7. **Recommendations** - When to use each strategy

## Setup

### Prerequisites

- Node.js (v16 or higher)
- npm or yarn

### Installation

```bash
npm install
```

### Running the Presentation

```bash
# Start development server
npm run dev
```

This will open the presentation in your browser at `http://localhost:3030`

### Navigation

- **Space** or **→**: Next slide
- **←**: Previous slide
- **Esc**: Overview mode
- **F**: Fullscreen
- **O**: Toggle overview
- **D**: Toggle dark mode

### Building for Production

```bash
# Build static HTML
npm run build

# Export to PDF
npm run export
```

The built presentation will be in the `dist/` folder.

## GitHub Pages Hosting

This presentation is configured for automatic deployment to GitHub Pages.

### Initial Setup

1. **Enable GitHub Pages** in your repository:
   - Go to repository Settings → Pages
   - Under "Build and deployment", select **Source**: GitHub Actions

2. **Push to GitHub**:
   ```bash
   git add .
   git commit -m "Add GitHub Pages deployment"
   git push origin main
   ```

3. **Automatic Deployment**:
   - The GitHub Actions workflow will automatically build and deploy on every push to `main`
   - You can also trigger deployment manually from the Actions tab

4. **Access Your Presentation**:
   - Once deployed, your presentation will be available at:
   - `https://<your-username>.github.io/fesom_stac_presentation/`

### Manual Deployment Trigger

You can manually trigger a deployment from the GitHub Actions tab by clicking "Run workflow" on the "Deploy to GitHub Pages" workflow.

### Base Path Configuration

The presentation is configured with base path `/fesom_stac_presentation/` in `package.json`. If you rename your repository, update the `--base` flag in the build script accordingly.

## Presentation Structure

- **slides.md** - Main presentation file with frontmatter and page imports
- **pages/** - Directory containing individual slide markdown files
  - `02-what-is-stac.md` - Introduction to STAC
  - `03-stac-hierarchy.md` - Catalog → Collection → Item structure
  - `04-stac-for-fesom.md` - Why STAC for FESOM
  - `05-section-strategies.md` - Section divider
  - `06-strategy1-single.md` - Single collection strategy
  - `07-reading-strategy1.md` - Reading single collection
  - `08-strategy2-per-variable.md` - Per-variable collection strategy
  - `09-reading-strategy2.md` - Reading per-variable collections
  - `10-reading-example.md` - Reading catalog example
  - `11-catalog-structure.md` - Directory structure
  - `12-comparison-advantages.md` - Advantages comparison
  - `13-comparison-disadvantages.md` - Disadvantages comparison
  - `14-recommendations.md` - FESOM-specific recommendations
  - `15-metadata-preserved.md` - CF metadata preservation
  - `16-multi_level_catalog.md` - Multi-level catalog organization
  - `17-stac-browser.md` - STAC Browser visualization
  - `18-questions.md` - Q&A slide
- **package.json** - Node.js dependencies
- **README.md** - This file

The title slide is embedded in slides.md. Each subsequent slide is in its own markdown file for easier editing and maintenance.

## Customization

The presentation uses Slidev's default theme. You can customize:

- **Theme**: Change `theme:` in the frontmatter of slides.md
- **Background**: Modify `background:` URL in the frontmatter
- **Colors**: Add custom CSS in slides.md or separate style files

## Tips for Presenting

1. **Practice navigation** - Use overview mode (Esc) to jump between sections
2. **Use presenter mode** - Click the presenter icon to see notes and next slide
3. **Code highlighting** - Code blocks have line numbers and syntax highlighting
4. **Animations** - Use `v-click` for progressive disclosure
5. **Dark mode** - Toggle with 'D' key for different lighting conditions

## Related Files

The presentation references these files in the repository:

- `builder.py` - Single collection catalog builder
- `builder_per_variable_collection.py` - Per-variable collection builder
- `reading_intake.py` - Example reading single collection
- `reading_intake_per_variable.py` - Example reading per-variable collections
- `example.py` - Build single collection catalog
- `example_per_variable.py` - Build per-variable catalog

## Resources

- [Slidev Documentation](https://sli.dev/)
- [STAC Specification](https://stacspec.org/)
- [intake-stac](https://github.com/intake/intake-stac)
- [PySTAC](https://github.com/stac-utils/pystac)

## License

Same as the parent repository.
