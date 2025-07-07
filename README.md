<!-- markdownlint-disable-next-line -->
<div align="center">

  <!-- markdownlint-disable-next-line -->
  # Chirpy Jekyll Theme

  A minimal, responsive, and feature-rich Jekyll theme for technical writing.

  [![CI](https://img.shields.io/github/actions/workflow/status/cotes2020/jekyll-theme-chirpy/ci.yml?logo=github)][ci]&nbsp;
  [![Codacy Badge](https://img.shields.io/codacy/grade/4e556876a3c54d5e8f2d2857c4f43894?logo=codacy)][codacy]&nbsp;
  [![GitHub license](https://img.shields.io/github/license/cotes2020/jekyll-theme-chirpy?color=goldenrod)][license]&nbsp;
  [![Gem Version](https://img.shields.io/gem/v/jekyll-theme-chirpy?&logo=RubyGems&logoColor=ghostwhite&label=gem&color=orange)][gem]&nbsp;
  [![Open in Dev Containers](https://img.shields.io/badge/Dev_Containers-Open-deepskyblue?logo=linuxcontainers)][open-container]

  [**Live Demo** →][demo]

  [![Devices Mockup](https://chirpy-img.netlify.app/commons/devices-mockup.png)][demo]

</div>

# Robotics Engineer Portfolio

A Jekyll-based portfolio website built with the Chirpy theme, showcasing robotics projects, computer vision systems, and mechatronics engineering work.

## Features

### 🚀 **Projects Section**
- **Project Collection**: Organized projects in `_projects/` directory
- **Project Cards**: Beautiful card layout with thumbnails, tech stack, and descriptions
- **Individual Project Pages**: Detailed project pages with full content
- **Responsive Design**: Mobile-friendly project grid layout

### 🛠 **Skills Section**
- **Categorized Skills**: Grouped by Programming, Robotics, Tools, Hardware, and Software Development
- **Progress Bars**: Visual skill level indicators with animations
- **Clean Design**: Minimal, professional appearance matching Chirpy's aesthetic

### 🎓 **Education Section**
- **Academic Background**: Master's and Bachelor's degrees in robotics and mechatronics
- **Certifications**: Professional certifications in ROS, Computer Vision, and Embedded Systems
- **Academic Projects**: Research and capstone projects with detailed descriptions

### 📱 **Navigation**
- **Simplified Sidebar**: Clean navigation with Home, Projects, Education, Skills, and Blog
- **Integrated About**: About section merged into the homepage for better user experience
- **Mobile Responsive**: Optimized for all device sizes
- **Dark/Light Theme**: Automatic theme switching support

## Project Structure

```
├── _projects/           # Project collection
│   ├── autonomous-robot.md
│   └── computer-vision-system.md
├── _tabs/              # Navigation tabs
│   ├── projects.md     # Projects redirect
│   ├── education.md    # Education page (renamed from archives)
│   ├── skills.md       # Skills page
│   └── blog.md         # Blog redirect
├── _layouts/           # Custom layouts
│   ├── project.html    # Individual project layout
│   └── home.html       # Updated home layout with about section
├── _sass/pages/        # Custom styles
│   ├── _projects.scss  # Project page styles
│   ├── _skills.scss    # Skills page styles
│   └── _home.scss      # Home page styles
└── projects.html       # Projects index page
```

## Navigation Structure

The site now features a streamlined navigation:

1. **Home** 🏠 - About section + latest blog posts
2. **Projects** 📊 - Portfolio of robotics and mechatronics projects
3. **Education** 🎓 - Academic background and certifications
4. **Skills** 🛠️ - Technical skills with progress indicators
5. **Blog** 📝 - Technical articles and tutorials

## Adding New Projects

1. Create a new markdown file in `_projects/`
2. Use this front matter structure:
   ```yaml
   ---
   layout: project
   title: "Project Title"
   description: "Brief project description"
   tech_stack: ["Technology 1", "Technology 2"]
   thumbnail: "/assets/img/projects/your-image.jpg"
   link: "/projects/your-project"
   date: 2023-12-01
   ---
   ```

## Customization

### Colors and Styling
- All styles use Chirpy's CSS variables for consistent theming
- Supports both light and dark modes automatically
- Mobile-responsive design

### Skills Categories
- Edit `_tabs/skills.md` to modify skill categories and levels
- Progress bar percentages can be adjusted (0-100%)
- Add new categories by following the existing structure

### Education Content
- Update `_tabs/education.md` with your academic background
- Add certifications, degrees, and academic projects
- Customize the content to match your experience

## Development

### Prerequisites
- Ruby 3.0+
- Node.js 16+
- Jekyll 4.0+

### Setup
```bash
# Install Ruby dependencies
bundle install

# Install Node.js dependencies
npm install

# Build assets
npm run build:js
npm run build:css

# Start development server
bundle exec jekyll serve --livereload
```

### Building for Production
```bash
# Build all assets
npm run build

# Build Jekyll site
bundle exec jekyll build
```

## License

This project is based on the [Chirpy Jekyll Theme](https://github.com/cotes2020/jekyll-theme-chirpy) and is licensed under the MIT License.

## Documentation

To learn how to use, develop, and upgrade the project, please refer to the [Wiki][wiki].

## Contributing

Contributions (_pull requests_, _issues_, and _discussions_) are what make the open-source community such an amazing place
to learn, inspire, and create. Any contributions you make are greatly appreciated.
For details, see the "[Contributing Guidelines][contribute-guide]".

## Credits

### Contributors

Thanks to [all the contributors][contributors] involved in the development of the project!

[![all-contributors](https://contrib.rocks/image?repo=cotes2020/jekyll-theme-chirpy&columns=16)][contributors]
<sub> — Made with [contrib.rocks](https://contrib.rocks)</sub>

### Third-Party Assets

This project is built on the [Jekyll][jekyllrb] ecosystem and some [great libraries][lib], and is developed using [VS Code][vscode] as well as tools provided by [JetBrains][jetbrains] under a non-commercial open-source software license.

The avatar and favicon for the project's website are from [ClipartMAX][clipartmax].

## License

This project is published under [MIT License][license].

[gem]: https://rubygems.org/gems/jekyll-theme-chirpy
[ci]: https://github.com/cotes2020/jekyll-theme-chirpy/actions/workflows/ci.yml?query=event%3Apush+branch%3Amaster
[codacy]: https://app.codacy.com/gh/cotes2020/jekyll-theme-chirpy/dashboard?utm_source=gh&utm_medium=referral&utm_content=&utm_campaign=Badge_grade
[license]: https://github.com/cotes2020/jekyll-theme-chirpy/blob/master/LICENSE
[open-container]: https://vscode.dev/redirect?url=vscode://ms-vscode-remote.remote-containers/cloneInVolume?url=https://github.com/cotes2020/jekyll-theme-chirpy
[jekyllrb]: https://jekyllrb.com/
[clipartmax]: https://www.clipartmax.com/middle/m2i8b1m2K9Z5m2K9_ant-clipart-childrens-ant-cute/
[demo]: https://cotes2020.github.io/chirpy-demo/
[wiki]: https://github.com/cotes2020/jekyll-theme-chirpy/wiki
[contribute-guide]: https://github.com/cotes2020/jekyll-theme-chirpy/blob/master/docs/CONTRIBUTING.md
[contributors]: https://github.com/cotes2020/jekyll-theme-chirpy/graphs/contributors
[lib]: https://github.com/cotes2020/chirpy-static-assets
[vscode]: https://code.visualstudio.com/
[jetbrains]: https://www.jetbrains.com/?from=jekyll-theme-chirpy
