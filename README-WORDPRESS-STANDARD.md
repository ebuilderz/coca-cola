# WordPress Standard Installation - Honoring and Remembering NM Veterans

## Overview

This branch contains the **standard WordPress installation** with all WordPress issues fixed and optimizations applied. This is the state of the website **before** the headless/Next.js conversion was implemented.

## What's Included

✅ **Fully Functional WordPress Site**
- Complete WordPress installation with all core files
- Custom theme: GeneratePress Child Theme
- All plugins installed and configured
- Database with content and settings
- Optimized CSS and JavaScript assets

✅ **WordPress Optimizations Applied**
- Database credentials updated for security
- Custom fonts (Inter & Onest) with font-display: swap
- Fixed asset versioning for better caching
- Improved script dependencies and loading
- Spectra plugin errors resolved
- Performance enhancements applied

✅ **Content & Database**
- `hrnmv.sql` - Main database export
- `git-hrnmv.sql` - Alternative database export
- All WordPress content, pages, posts, and settings

## Setup Instructions

### 1. Clone This Branch
```bash
git clone -b wordpress-standard-installation [your-repo-url]
cd Honoring-and-Remembering
```

### 2. Database Setup
```bash
# Import the database (choose one):
mysql -u your_username -p your_database_name < hrnmv.sql
# OR
mysql -u your_username -p your_database_name < git-hrnmv.sql
```

### 3. WordPress Configuration
1. Copy `wp-config-sample.php` to `wp-config.php`
2. Update database credentials in `wp-config.php`:
   ```php
   define('DB_NAME', 'your_database_name');
   define('DB_USER', 'your_username');
   define('DB_PASSWORD', 'your_password');
   define('DB_HOST', 'localhost');
   ```

### 4. File Permissions
```bash
chmod 755 wp-content/
chmod 755 wp-content/themes/
chmod 755 wp-content/plugins/
chmod 644 wp-config.php
```

### 5. WordPress Admin Access
- URL: `http://your-domain.com/wp-admin`
- Default admin credentials should be in the database
- Reset password if needed through WordPress

## Key Features

### Theme & Styling
- **GeneratePress Child Theme** with custom modifications
- Custom CSS in `wp-content/themes/generatepress-child/assets/css/`
- Responsive design optimized for veterans memorial content

### Plugins Included
- **Spectra (Ultimate Addons for Gutenberg)** - Page builder blocks
- **GeneratePress Premium** - Theme extensions
- Other essential WordPress plugins

### Content Structure
- Homepage with hero sections
- About Us page
- Contact page with forms
- Blog/News section
- Custom post types for veterans content

## Development Notes

### This Branch Contains:
- ✅ Standard WordPress installation
- ✅ All WordPress core files
- ✅ Custom theme and plugins
- ✅ Database with content
- ✅ Optimized assets and performance fixes

### This Branch Does NOT Contain:
- ❌ Next.js headless frontend
- ❌ Headless API configurations
- ❌ React components
- ❌ Node.js dependencies

## Working with This Installation

This is a **standard WordPress installation** that works like any traditional WordPress site:

1. **Content Management**: Use WordPress admin panel
2. **Theme Customization**: Edit theme files in `wp-content/themes/generatepress-child/`
3. **Plugin Management**: Install/configure through WordPress admin
4. **Database**: Standard WordPress database structure

## Support

This branch represents the WordPress site in its optimized state before headless conversion. All WordPress-specific issues have been resolved, and the site is ready for standard WordPress development.

For questions about the headless/Next.js version, refer to the main branch (`isha/7/23/2025`).

---

**Branch Created**: July 24, 2025  
**Commit**: 985ed8b - WordPress Site Optimization & Bug Fixes  
**Purpose**: Standard WordPress development without headless architecture