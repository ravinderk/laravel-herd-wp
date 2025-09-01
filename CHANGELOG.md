# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [2.3.0] - 2025-09-01

### ✨ Added
- **🖥️ Terminal Error Detection** - PHP error template now automatically detects terminal/CLI environments
- **📋 Copy Error Button** - New copy button in web error pages for easy debugging with GitHub Copilot
- **🎯 Environment-Specific Formatting** - Clean terminal output for CLI, beautiful HTML for web browsers
- **⚡ Smart Error Display** - Automatic switching between terminal and web error formats

### 🔄 Changed
- **💥 Enhanced PHP Error Template** - Improved `.php-error-template` with dual-mode error display
- **🎨 Terminal-Friendly Output** - Clean, formatted error messages for command-line environments
- **📱 Better Web Interface** - Added copy functionality to existing beautiful HTML error pages

### 🎨 Improved
- **🔍 Developer Experience** - Easy error sharing with GitHub Copilot via copy button
- **⌨️ CLI Compatibility** - Terminal errors display without colors or formatting codes
- **🎭 User Experience** - Seamless error handling across different environments
- **📊 Error Information** - Consistent error details across terminal and web formats

### 🐛 Fixed
- **🖥️ Terminal Display Issues** - Proper error formatting for CLI environments
- **📋 Copy Functionality** - Cross-browser clipboard support with fallback methods
- **🔄 Environment Detection** - Reliable detection of CLI vs web environments

## [2.2.0] - 2025-07-07

### ✨ Added
- **📖 Help Command** - New `help` script to display all available commands and usage
- **📚 Organized Documentation** - Restructured docs into focused, topic-specific files
- **🔗 Better Navigation** - Updated README with clear documentation links and structure
- **💡 Command Discovery** - Easy-to-use help system for better user experience

### 🔄 Changed
- **📛 Documentation Structure** - Merged WordPress tools into main WordPress documentation
- **📝 README Simplification** - Streamlined README for quick start and better usability
- **🎯 User-Focused Content** - Improved language and examples for end users
- **📋 File Organization** - Renamed documentation files to use capital letters (COMMANDS.md, etc.)

### 🎨 Improved
- **🔍 Command Reference** - Comprehensive command overview with examples
- **📖 Documentation Quality** - Better organization and more practical examples
- **🆘 Help System** - Instant access to all commands with `./help`
- **🎭 User Experience** - More intuitive documentation structure and navigation

### 🐛 Fixed
- **📁 Git Tracking** - Fixed .gitignore to properly include docs directory and files
- **🔗 Documentation Links** - Updated all internal documentation references
- **📝 Duplicate Content** - Removed redundant sections from README

## [2.1.0] - 2025-07-07

### ✨ Added
- **🔍 Dry Run Mode** - Added `--dry-run` support to all scripts for previewing changes
- **🐘 herd.php** - New PHP settings management script for FPM configuration
- **📊 PHP Logging Control** - Enable/disable PHP error logging across all versions
- **💻 Enhanced CLI Interface** - Consistent `show_usage()` functions across all scripts
- **🎯 Smart State Detection** - Scripts now detect current state and skip unnecessary changes
- **📝 Improved Error Handling** - Better validation and error messages throughout

### 🔄 Changed
- **📛 Script Renaming** - `php-error.manage` renamed to `wp.php` with new syntax
- **🎨 Command Structure** - `wp.php` now uses `error-template on/off` syntax
- **📚 Enhanced Documentation** - Updated README with comprehensive command examples
- **🔧 Better CLI Experience** - All scripts now support `--help` and provide usage information

### 🐛 Fixed
- **🔢 Integer Expression Errors** - Fixed bash comparison issues in herd.php
- **📁 Template Path Issues** - Corrected relative path handling in wp.php
- **🔄 Idempotent Operations** - All scripts now properly handle repeated execution
- **💾 Memory Management** - Improved handling of WP-CLI memory limits

### 🎨 Improved
- **🎭 Bash Compatibility** - Fixed bash substitution issues for broader compatibility
- **📊 Status Reporting** - Better progress indication and result summaries
- **🔍 State Validation** - Enhanced checking of current configuration states
- **⚡ Performance** - Optimized script execution and reduced unnecessary operations

## [2.0.0] - 2025-01-XX

### ✨ Added
- **🐛 herd.xdebug** - Unified Xdebug management script replacing separate on/off scripts
- **🛠️ php-error.manage** - Script to manage custom PHP error templates across sites
- **💥 Custom PHP Error Templates** - Beautiful, styled error pages with stack trace formatting
- **📄 Template System** - `.php-error-template` file for consistent error page deployment
- **🔧 Multi-PHP Version Support** - Xdebug configuration across all Herd PHP versions
- **🔄 Auto-restart Functionality** - Herd automatically restarts after Xdebug configuration changes

### 🔄 Changed
- **📚 Improved Documentation** - Updated README with comprehensive script documentation
- **⚠️ Enhanced Error Handling** - Better error messages and validation across all scripts
- **🎯 Unified Script Interface** - Consistent command-line arguments across scripts

### 🐛 Fixed
- **💾 Memory Issues** - Resolved WP-CLI memory exhaustion during WordPress downloads
- **🔑 Database Password Handling** - Fixed empty password handling in MySQL commands
- **📁 Template File Paths** - Corrected relative path handling in management scripts

### 🗑️ Removed
- **❌ herd.xdebug.on** - Merged into unified herd.xdebug script
- **❌ herd.xdebug.off** - Merged into unified herd.xdebug script

## [1.0.0] - 2025-07-01

### ✨ Added
- **🆕 wp.new** - WordPress site creation script with smart setup
- **🗑️ wp.delete** - Safe WordPress site deletion script
- **🐛 herd.xdebug.on** - Enable Xdebug for debugging
- **🚫 herd.xdebug.off** - Disable Xdebug for performance
- **🗄️ Database Management** - Automatic creation of main and test databases
- **🔒 HTTPS Support** - Automatic SSL certificate generation via Herd
- **🔌 Plugin Installation** - Pre-installed development plugins (WP Mail Logging, Query Monitor, WP Crontrol)
- **🔄 Idempotent Operations** - Safe re-running of scripts without conflicts
- **✅ Smart Validation** - Comprehensive checks for prerequisites and existing installations

### 🔌 WordPress Plugins Included
- **📧 WP Mail Logging** - Email debugging and capture
- **🔍 Query Monitor** - Performance and database query debugging
- **⏰ WP Crontrol** - WordPress cron job management

### 📚 Documentation
- **📖 README.md** - Comprehensive setup and usage guide
- **🤝 CONTRIBUTING.md** - Contribution guidelines and project philosophy
- **📄 LICENSE** - MIT license for open source usage
- **🙈 .gitignore** - Proper git ignore configuration for development files

### ⚙️ Configuration
- **👤 Default Credentials** - Admin/password for quick development setup
- **🦌 Herd Integration** - Sites created in ~/Herd/ directory
- **🗄️ Database Defaults** - UTF8MB4 charset and collation
- **⚡ Memory Optimization** - Unlimited memory for WP-CLI operations

### 🧪 Testing Environment
- **🖥️ Platform Support** - Tested on macOS Sonoma (14.x)
- **💻 Hardware Compatibility** - Verified on MacBook Pro 2019
- **🔗 Tool Integration** - DBngin and TablePlus recommendations

## [0.1.0] - Initial Development

### ✨ Added
- **🌱 Basic WordPress installation automation**
- **🗄️ Simple database creation**
- **🦌 Initial Herd integration concepts**

---

## 📖 Legend

- **✨ Added** for new features
- **🔄 Changed** for changes in existing functionality  
- **⚠️ Deprecated** for soon-to-be removed features
- **🗑️ Removed** for now removed features
- **🐛 Fixed** for any bug fixes
- **🔒 Security** for vulnerability fixes
- **🎨 Improved** for enhancements and optimizations
