# 🌿 Budsy

**Your bud tracking buddy** - Track, analyze, and optimize your medical marijuana usage with smart algorithms and beautiful insights.

[![Live Site](https://img.shields.io/badge/Visit-budsyapp.com-89b153?style=for-the-badge)](https://www.budsyapp.com)
[![GitHub Pages](https://img.shields.io/badge/Powered_by-GitHub_Pages-181717?style=for-the-badge&logo=github)](https://pages.github.com/)

## About Budsy

Budsy is a comprehensive medical marijuana tracking application designed to help patients monitor, analyze, and optimize their cannabis usage. Our app provides intelligent insights through smart algorithms while maintaining the highest standards of privacy and data security.

## Key Features

🌱 **Smart Tracking** - Effortlessly log your cannabis consumption with detailed strain and dosage information

📊 **Intelligent Analytics** - Advanced algorithms analyze your usage patterns and provide personalized insights

🔒 **Privacy First** - Your medical data stays secure with local storage and privacy-focused design

📱 **Beautiful Interface** - Clean, intuitive design that makes tracking simple and enjoyable

🎯 **Personalized Recommendations** - Get tailored suggestions based on your unique usage patterns and preferences

## Website

This repository contains the official Budsy website built with Jekyll and deployed via GitHub Pages. The site showcases the app's features and provides information for potential users.

## Contributors

- **hrcassels** - Lead Developer
- **Severswoed** - Co-Developer

## Contact

- **Website**: [budsyapp.com](https://www.budsyapp.com)
- **Email**: budsyapp@gmail.com

---

*Budsy - Making medical cannabis tracking simple, smart, and secure.*

The landing page highlights Budsy's core features:

### 🔢 Track Your Units
- Log MMJ units by day, time, and quantity
- Smart 30-day rolling algorithm for expected returns
- Easy editing of previous logs

### 📅 Unit History View  
- Visual calendar with color-coded usage
- List view for quick browsing and edits
- Pattern recognition and insights

### 🧪 Strain Journal
- Record strain details (name, THC %, terpenes)
- Rate experiences and note reactions
- Filter by terpene, THC, rating, or alphabetically

### ⚙️ Personalize Settings
- Rename "units" to your terminology
- Customize allotment and rolling periods
- Tailor to your medical needs

## 🛠️ Local Development

### 🚀 Quick Setup (Automated)

Choose your preferred setup method:

**🐍 Python (Recommended - Cross-platform)**
```bash
# Basic setup (checks dependencies, prompts if missing)
python scripts/setup.py

# Auto-install dependencies (Windows only - installs Ruby/Chocolatey if needed)
python scripts/setup.py --install-deps

# Setup and start server immediately
python scripts/setup.py --serve

# Check system requirements only
python scripts/setup.py --check
```

**🪟 Windows PowerShell**
```powershell
cd scripts
.\setup.ps1
```

**🪟 Windows Batch**
```cmd
cd scripts
setup.bat
```

The automated setup scripts will:
- ✅ Check for Ruby and Bundler
- 🍫 Install Chocolatey (Windows, if using --install-deps)
- � Install Ruby automatically (Windows, if using --install-deps)
- �📦 Install Jekyll and dependencies  
- 🚀 Start the development server
- 🌐 Open your browser to `http://localhost:4000`

### 🔧 Manual Setup

If you prefer manual control or are on a non-Windows system:

```bash
# 📦 Install dependencies
bundle install

# 🚀 Launch development server
bundle exec jekyll serve

# 🌐 Visit your local site
open http://localhost:4000
```

### 🔧 Development Tips

```bash
# 🔄 Auto-rebuild on changes
bundle exec jekyll serve --livereload

# 🎯 Specific port
bundle exec jekyll serve --port 4001

# 🌍 Allow external connections  
bundle exec jekyll serve --host 0.0.0.0
```

## 🚀 Deployment

**Automated deployment** via GitHub Pages:

- ✅ **Auto-deploy** on `main` branch pushes
- 🔄 **GitHub Actions** handles the build process
- 🌐 **Custom domain** configured at [budsyapp.com](https://budsyapp.com)
- 📊 **Build status** visible in repository Actions tab

## 💖 Support the Project

Help us build the best cannabis tracking app!

**Ways to support:**
- ⭐ Star this repository
- 🐛 Report bugs or suggest features
- 🔄 Share Budsy with other medical cannabis patients
- 💡 Contribute code improvements
- 📢 Spread awareness about responsible medical usage

## 🤝 Contributing

We welcome contributions! Here's how to get involved:

### 🎯 Quick Start

1. **🍴 Fork** the repository
2. **🌿 Branch** your feature (`git checkout -b feature/amazing-feature`)
3. **💫 Commit** your changes (`git commit -m 'Add amazing feature'`)
4. **🚀 Push** to branch (`git push origin feature/amazing-feature`)
5. **🎉 Open** a Pull Request

### 🎨 Areas for Contribution

- 🎭 **Design improvements** and animations
- 📱 **Mobile responsiveness** enhancements  
- ♿ **Accessibility** improvements
- 🌍 **Internationalization** support
- 📖 **Documentation** updates
- 🐛 **Bug fixes** and optimizations
- 🌿 **Cannabis-specific** features and content

---

<div align="center">

### 🌟 Made with 💚 by [Severswoed](https://github.com/Severswoed)

**Track responsibly with Budsy!** 🌿

[![GitHub](https://img.shields.io/badge/Follow-@Severswoed-181717?style=social&logo=github)](https://github.com/Severswoed)

</div>
